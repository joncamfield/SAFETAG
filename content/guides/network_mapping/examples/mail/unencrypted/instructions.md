If the attacker wishes to observe the victim’s email traffic (most likely because she failed to capture an unencrypted password, which would have allowed her to log in as the victim himself and read his email directly), she may need to carry out a second, slightly more complex attack.

To capture outgoing (SMTP) messages, the attack is nearly identical to the password attack described above.


**Step 1:** The attacker tricks the victim into routing all of his traffic through the attacker’s machine. This involves making a simple request to the victim’s IP address, which is not difficult to do. Computers are rarely configured to ignore such requests.

`` $ sudo sh -c 'echo 1 > /proc/sys/net/ipv4/ip_forward'
`` $ sudo arpspoof -i wlan0 -t 192.168.1.99 192.168.1.1

``
00:11:22:33:44:55 aa:bb:cc:dd:ee:ff 0806 42: arp reply 192.168.1.1 is-at 00:11:22:33:44:55
00:11:22:33:44:55 aa:bb:cc:dd:ee:ff 0806 42: arp reply 192.168.1.1 is-at 00:11:22:33:44:55
00:11:22:33:44:55 aa:bb:cc:dd:ee:ff 0806 42: arp reply 192.168.1.1 is-at 00:11:22:33:44:55
00:11:22:33:44:55 aa:bb:cc:dd:ee:ff 0806 42: arp reply 192.168.1.1 is-at 00:11:22:33:44:55
...
00:11:22:33:44:55 aa:bb:cc:dd:ee:ff 0806 42: arp reply 192.168.1.1 is-at 00:11:22:33:44:55
``

In the example above, only a single victim (192.168.1.99) is being targeted, but the attack works fine against multiple victims, or even against the entire network. In other words, the attacker does not need to know which IP address (on the office or Internet cafe LAN, for example) belongs to her target. Furthermore, the victim is extremely unlikely to notice any sign that this phase of the attack is taking place.

EtterCap provides a powerful frontend to managing this process with multiple potential targets.  In EtterCap:

* Under the "Sniff" menu, select "Unified sniffing" (for most cases where you are using one interface to both intercept and forward traffic), and select the relevant interface (wlan0)
* Under the Hosts menu, select the systems on the network you will target, or leave blank to target all systems
* Under Mitm, select "arp spoofing" for this example
* Select "Start" under the Sniffing menu

<Ettercap Screenshot>

**Step 2:** At this point, if the attacker is looking for outgoing email, all she needs to do is launch a packet-sniffer, such as Wireshark, and scan through the SMTP traffic for email messages, which will appear as soon as they are sent:

<wireshark screenshot>

Figure 1: Wireshark filtered by smtp, displaying an email message sent by the victim

**Step 3:** In order to monitor incoming (POP3 or IMAP) messages, the attacker must use other technique to ensure that responses to the victim actually pass through her machine before they arrive at their intended recipient. The most straightforward tool for this sort of thing is designed to attack Web traffic, but the same techniques works on POP3 and IMAP traffic. (This tool, SSLStrip, was written to facilitate more advanced testing of Web services that do implement encryption, but that do so incorrectly. In any case, it works fine for our purposes here.)

``$ sslstrip -a -l 12345 -w sslstrip.log

**Step 4:** The attacker then uses iptables to route a portion of the victim’s traffic (in this case, IMAP traffic destined for port 143) through the SSLStrip tool, which rewrites headers such that responses come to her first, before continuing along to the victim. She then monitors the tool’s output for email messages:

``$ iptables -t nat -A PREROUTING -p tcp --destination-port 143 –j REDIRECT --to-port 12345
``$ tail -f sslstrip.log

(For POP3, the attacker would use port 110 instead of port 143, but the attack is otherwise identical.) At this point, the contents of the sslstrip.log file contains a copy of incoming IMAP traffic, including any email messages the victim might read while he is being observed.

<message snippet from sslstrip.log>

Figure 2: Attacker viewing an incoming email message intended for the victim

Again, this same technique, with minor modifications, would work to monitor incoming email messages downloaded through Webmail
