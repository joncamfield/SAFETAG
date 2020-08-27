---
title: Network Access
approaches:
  - Technical
authors:
  - SAFETAG
remote_options:
  - None
skills_required:
  - password cracking
  - wireless network monitoring
skills_trained: []
summary: >
  This activity helps auditors to test the strength of defenses the
  organizations' network has in place to protect their local area network.

  This component consists of gaining access to the local area network through a
  wireless access point and unsecured physical channels (such as an ethernet
  jack).
overview: >2+

    * Determine the security of the wireless access point (WAP).
    * Gain access to the organizations Wireless network access.
    * Test unused ethernet ports for live network connectivity.
    * Find out how guest access is managed

  **Expected Outputs**

    * Un-authorized access to the Wireless access point (WAP)
    * List of unused ethernet jacks with network connectivity.


  *Note*:

  Cracking wireless passwords often take a huge amount of time performing, and
  the same results for the audit and organizational buy-in can be had simply by
  showing how password cracking works, and how far outside of the office the
  wireless network can be seen. Once an organization is using vulnerable
  authentication method, you can flag it right away as "finding". Given that the
  recommendations are often the same (move to WPA2 (and WPA3 as available),
  disable WEP and WPS access, provide a separate guest network, etc.), this
  should rarely be used during an audit (but is a useful skill to practice and
  understand how it works). If you do choose to use this during an audit, be
  aware that many of the stps disrupt network traffic, and success with WPA2
  password cracking is by no means guaranteed, so can backfire.


  By walking organizations through the vulnerabilities of wireless networks, you
  have the opportunity to discuss password strength, and the power that having
  "offline" access to a password means in terms of brute forcing it, as well as
  the importance of defense in depth even within their trusted work network -
  reducing the services computers and servers are sharing, setting up local
  firewalls on computers, and requiring authentication to access files.


  Even a few minutes of network "sniffing" by an adversary can enable them to
  work offline to reveal the network password.  Knowing this password would let
  someone then access the entire internal network, files shared internally, and
  even change network settings to enable remote access.  While in an ideal
  setup, this would give no further access to sensitive documents, it is not
  uncommon to find shared file folders, or to gain access to the firewall or
  network routers (often set to the default password, because they're only
  accessible from inside the network...).


materials_needed: ''
considerations: >+

  *Note:* This section is one of the few sections where the SAFETAG audit does
  go through attack scenarios, from attempting to "break in" to the wireless
  network to testing exposed ethernet jacks for connectivity.


  The reasons for this are threefold.  First, access to an organization's
  internal network tends to reveal sensitive data and "shadow" infrastructures
  (such as dropbox usage) that lead to many recommendations to improve access
  control and discussions of the value of defense in depth.  Second, the
  specific act of breaking the wifi password allows for a discussion on password
  security without attacking any specific user's password. Finally, with
  wireless networks treated as equivalent to wired networks in many offices,
  reminding the organization that wireless networks extend beyond the physical
  walls of the office is useful in discussing password rotation and guest
  network policies.


  Once you have access to the network, you need to first document how you
  managed that and share it with the hosts.  This is a great moment to discuss
  passwords in many cases.

    * Confirm that all devices you are accessing/scanning belong to the organization.
    * Clarify timing and seek permission with staff - some activities can tax the network or cause disruptions.


walk_through: >
  Breaking into network requires specialized tools as well as a significant
  amount of time in capturing authentication packets, and replaying those
  packets back to the wireless access point.


  MAC filtering is a common, but easy to bypass security measure.


  WEP (Wired Equivalent Privacy) has been found with several vulnerabilities.
  The RC4 algorithm that it uses to generate the keystream for encryption is
  subject to [two separate
  weaknesses](https://pdfs.semanticscholar.org/8aeb/2a27abc2a1d0a8b71047606fbeec0f711e03.pdf).


  On the other hand, WPA/WPA2 (Wi-Fi Protected Access) is also found to be
  vulnerable to attack known as [KRACK](https://www.krackattacks.com/)(Key
  Reinstallation Attacks) as well as offline (high speed) attacks against the
  password itself. WPS, a common "feature" that is on by default on WPA
  networks, has significant vulnerabilities.


  [WPA3](https://www.schneier.com/blog/archives/2018/07/wpa3.html), a new
  standard, is built to disallow offline password attacks, making it
  significantly harder to break in to that WPA2 networks. As it becomes
  available and devices support it, it should be a priority upgrade if wifi
  network security is a concern.


  ___
recommendations: >
  Transitioning to WPA networks with strong passwords, even for guest networks,
  is recommended.


  MAC filtering and WEP provide no effective protection for a wifi network. Most
  wifi routers offer WPA encryption as an option, and if this is available it
  should be immediately implemented. Some older routers (and wifi devices) do
  not support WPA. It is highly recommended to upgrade immediately to hardware
  that supports WPA and to eliminate all WEP network access. Very few devices
  still functional do not support WPA2. As WPA3 becomes an option, upgrade to
  that.



  WPS Pin entry should be disabled on the wireless router, or only enabled
  temporarily to add new devices to the network.


  Choosing a strong WPA key is one of the most important steps toward defending
  an organization’s network perimeter from an adversary with the ability to
  spend some time in the vicinity of the offices. By extension, mitigating this
  vulnerability is critical to the protection of employees and partners (and
  confidential data) from the sort of persistent exposure that eventually brings
  down even the most well-secured information systems.


  The WPA password should be long enough and complex enough to prevent both
  standard dictionary attacks and “brute-force attacks” in which clusters of
  powerful computers work in parallel to test every possible character
  combination. (We recommend 12 or more completely random characters or a
  passphrase that contains four or five—or more—relatively uncommon words.) The
  password should not contain common words, including number sequences,
  especially if they are related to the organization, its employees or its work.


  A guest network, with no local network access and a distinct (possibly easier
  to communicate) password should be available if guests are ever given wifi
  access. Because passwords for guest networks inevitably end up being written
  on whiteboards, given to office visitors and emailed to partners, the guest
  password should also be changed periodically. This does not have to happen
  frequently, but anything less than three or four times per year may be unsafe.
organization_size_under: 1000
time_required_minutes: 240
---

