---
title: Monitor Open Wireless Traffic
approaches:
  - Technical
authors:
  - SAFETAG
remote_options:
  - None
skills_required:
  - Wireless
  - Traffic Analysis
skills_trained: []
organization_size_under: 50
time_required_minutes: 60
summary: >
  It can be valuable to to listen to broadcast wireless traffic at  the physical
  office location, even before knowing anything about the organization's network
  itself. This outside, passive information gathering can reveal a surprising
  amount of data on not only what devices are connecting to which networks, but
  also what type of devices they are (based on their unique MAC addresses), and
  what other networks those devices have historically connected to. These probes
  can reveal personal, organizational, locational, and device information that,
  taken in context, can be dangerous or lead to other vulnerabilities.
overview: >

  Each wireless device maintains a "memory" of what networks it has successfully
  connected to. When it is connecting to a network, it sends out "probes" to all
  of the networks it has in this memory. It is important to note that this data
  gets broadcast widely, and can be collected without any network access, only
  proximity to the device.


  These network probes can often contain names (especially from mobile phone
  tethers), organizational affiliations, device manufacturers, and a mixture of
  other potentially valuable data (home network names, recent airports/travel
  locations, cafés and conference networks). If there are many networks in the
  office's vicinity, this activity can also help identify the specific office
  network (if there is any doubt). In many cases, an organization may not want
  the name of their wireless network to be associated with their organization,
  but it may be revealed by this additional meta-data.


  Beacons can "de-anonymize" an obfuscated network name as well as provide rich
  content for social engineering attacks. This provides an only-lightly-invasive
  introduction to discuss the trackability of devices, particularly mobiles and
  laptops.


  * Scan for wireless networks nearby, identify (and confirm) the office
  network(s).

  * Monitor traffic of that network and capture potentially sensitive metadata
  (wireless security settings, beacons, and MAC addresses).

  * Research likely device hardware using MAC addresses.

  * Do the staff devices leak sensitive metadata?

  * What can be determined about the organization based on broadcast wireless
  data?
materials_needed: |

  * Wifi card (and drivers) that can be set to monitor mode.
considerations: >

  * Despite this exercise covering only broadcast data, check the local laws
  which might cover this process before conducting it.

  * Consider how it looks to third parties as you are scanning a network,
  especially from outside an office.

  * Confirm that all devices you are accessing/scanning belong to the
  organization.

  * Delete all devices from your scan that do not belong to the organization.

  * Study outputs for any obviously embarrassing personal information
  (especially network beacon records) before sharing.
walk_through: |+

recommendations: ''
---

