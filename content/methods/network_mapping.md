---
activities:
  - Network Scanning
  - Network Access
  - Network Traffic Analysis
  - Remote Network and User Device Assessment
  - Router Based Attacks
  - VoIP Security Assessment
  - Wireless Range Mapping
  - Monitor Open Wireless Traffic
authors:
  - SAFETAG
info_provided: []
info_required: []
title: Network Mapping
summary: >

  This component allows the auditor to identify security issues with the host's
  network and map the devices on a host's network, the services that are being
  used by those devices, and any protections in place.
purpose: >
  Mapping an organization's network exposes the multitude of devices connected
  to it -- including mostly forgotten servers -- and provides the baseline for
  later work on device assessment and vulnerability research.


  This process also reveals outside service usage (such as google services,
  dropbox, or others) which serve -- intentionally or not -- as shadow
  infrastructure for the organization. In combination with beacon research from
  the *Monitor Open Wireless Traffic* exercise, many devices can be associated
  with users.
guiding_questions: >

  * What operating systems, and services being hosted or used by an
  organization? Are any hosts running unusual, custom, or outdated operating
  systems and services?

  * Are there unexpected/unusual devices or services on the network?

  * What is the topology of the network? What are the routers and modems 

  managing it?

  * What services (e.g. dropbox, web-mail, etc.) are running on the network that
  have not been mentioned by the organizational staff?

  * What network assets does an attacker have access to once they have gained
  access to the internal network?
approaches: >

  * **Network Mapping:** Map hosts, services, and network hardware by scanning
  network devices.

  * **Monitor Open Wireless Traffic:** Monitor wireless traffic for  handshakes,
  beacons, and MAC addresses.

  * **Wireless Range Mapping:** Map the range of the organizations wireless
  network outside of office space.
preparation: >

  #### Baseline Skills

  * Monitoring and analyzing wireless network traffic

  * Skill with using nmap/zenmap and its scripting options

  * Skill with Wireshark or other packet-capturing tool, as well as possibly
  more advanced traffic interception tools.
---

