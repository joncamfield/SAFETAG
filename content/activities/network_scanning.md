---
title: Network Scanning
approaches:
  - Technical
authors:
  - SAFETAG
remote_options:
  - with-support
skills_required:
  - Network Mapping
skills_trained: []
summary: >
  Network scanning is a technique used to gather information about devices
  connected on a certain network. It involves enumerating open ports and
  services running to determine the type of device, the operating system it is
  running, the applications that is it running and a lot more. There are a lot
  of open source tools that you can used to perform this technique. Though it
  may look like simple and ordinary technique, it may be used for both good and
  bad intentions.


  The goal for this exercise is to identify, enumerate and categorize all
  devices connected to the network. Any device that has an IP address is our
  target. This may include:

    - Desktop computers
    - Laptop computers
    - Tablet devices
    - Mobile phones
    - Printers
    - Wireless routers
    - VoIP devices
    - Smart TVs and appliances
    - Servers and storage devices
overview: >

  * Confirm what devices and servers are in scope of the audit, and confirm that
  any service providers (website hosts, cloud hosts, etc.) are informed and OK
  with any scanning to be conducted.
    * Enumerate and categorize all devices connected to the organization's network. Note that this could include IoT (Internet of Things) devices, such as IP cameras used for security, "Smart" devices, and personal devices such as mobile phones which may not be in scope. **Discuss the scope of the audit as it applied to devices connected to the work network and ensure the staff understand what you are doing.**
    * In some cases, the audit scope may include external devices. The scanning in these cases will be very targeted. If your auditee agreed to have their public facing machines scanned, keep in mind that you need to consider asking your auditee for whitelisting options for shunning IDS/IPS, firewalls and other blocking mechanisms during your scan. Also make sure that you have verified the target in-scope. This is to avoid scanning out-of-scope targets that may lead you to other problems.
  * Categorize and gather additional detail on the devices that you will
  discover

  * Explore potential vulnerabilities, unexpected devices, and suspicious open
  ports
materials_needed: |

  * Laptop or appliance that can scan the network
  * nmap/zenmap
considerations: >
  * **In Scope Devices** Just always remember that some may not want you to scan
  everything on their network. To avoid this, always ask your auditee if there
  are specific devices that needs exclusion. These machine can be critical to
  their operation or they just don't want to get scanned. If your auditee have
  exclusions, explain the consequences possible if a machine does not undergo
  vulnerability assessment. If scanning public servers, verify that the server
  host (web company, cloud provider, etc.) has approved of the scan, and than
  remote scanning is legal in the jurisdiction you are performing it from and in
  the location of the remote server.
walk_through: >

  Local networks often have a variety of devices connected to them - servers,
  laptops, printers, and user devices such as cellphones and tablets. Scanning
  the connected devices can reveal potential areas for further research such as
  odd ports being open, out of date devices/services, forgotten servers/services
  etc. These information are then reviewed in vulnerability research exercise,
  and then (if required) validated in the penetration testing exercise.


  Using a network scanning tool (**nmap/zenmap** work well), discover the
  devices connected to the organization's network, and explore further
  information such as services, service banners, and operating systems. More
  intense scans can be too time-consuming to run across the entire network, so
  target those to higher value systems. As always, be aware of the scans and
  additional scripts you choose, and focus your exploration (in nmap) on scripts
  categorized as "safe".
recommendations: ''
organization_size_under: 100
time_required_minutes: 120
---

