---
title: Website Footprinting
approaches:
  - Technical
  - Research
authors:
  - SAFETAG
remote_options:
  - Complete
skills_required:
  - Website scanning
skills_trained: []
summary: >

  Using online tools as a starting point in assessing the auditee web
  application is a good way to expand online reconnaisance as well as start your
  vulnerability assessment. You can build a profile and a good understanding of
  the web application by identifying what comprises the web application and
  technologies behind. From there you can start your next move by putting
  together different strategies on conducting your vulnerability assessment.


  For example, after discovering accessable web directories, you can then start
  looking for forgotten or abandoned files and applications that might contain
  sensitive information like (Passwords) or an outdated and vulnerable
  applications.  Content management systems, while powerful, require ongoing
  maintenance and updates to stay secure. Quite often these (or specific
  plugins) fall out of date and become increasingly vulnerable to automated as
  well as targeted attacks.


  Online tools offer ways of performing "passive" scans, in which your identity
  is hidden from the target organization, in cases where there are IDS/IPS,
  firewalls deployed. These should be used in conjuction with other outputs from
  reconnaisance to determine platforms and hosts which are out of scope.
overview: >

  * Determine the version of any content management system used by the
  organization

  * Search for potential security vulnerabilities for that version.
materials_needed: ''
considerations: ''
walk_through: >

  Before unleashing more advanced and powerful tools like OpenVAS, a few quick
  steps can help better guide your work. As a general note, surfing using a
  browser with at least
  [NoScript](https://addons.mozilla.org/en-US/firefox/addon/noscript/) enabled
  may help not only protect you, but may also help to reveal malware or adware
  infecting the websites.


  Record core details about the website - determine the hosting provider,
  platform, Content Management Systems, and other baseline data. 
  [BuiltWith](http://builtwith.com/) is a great tool.  There are a few
  alternatives, including an open source tool,
  [SiteLab](https://callmeed.github.io/site-lab/).  *Note that BuiltWith is a
  tool bundled in recon-ng, but the output it provides is not currently stored
  in its data structures.* These tools may also reveal plugins, javascript
  libraries, and DDoS protection systems like CloudFlare.


  **Tools**


  - [BuiltWith](https://builtwith.com)

  - [Online Pentesting Tools](https://pentest-tools.com/)

  - [Hacker Target](https://hackertarget.com/)


  ___
recommendations: ''
organization_size_under: 1000
time_required_minutes: 60
---

