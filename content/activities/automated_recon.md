---
title: Automated Reconnaisance
approaches:
  - Technical
authors:
  - SAFETAG
remote_options:
  - Complete
skills_required:
  - OSINT Tools
skills_trained: []
organization_size_under: 1000
time_required_minutes: 240
summary: >+
  This component allows the auditor to quickly identify publicly available
  resources (such as websites, extranets, email servers, but also social media
  information) connected to the organization and remotely gather information
  about those resources.


  While much of SAFETAG focuses on digital security challenges within and around
  the office, remote attacks on the organization's website, extranets, and
  unintended information available from "open sources" all pose real threats and
  deserve significant attention.  SAFETAG takes great care to take a very
  passive approach to this work, especially when done off-site, so as not to
  have unintended consequences on the organization's infrastructure or undermine
  operational security concerns.


  This remote work also feeds in to the Auditor's understanding of the
  organization's digital presence (and their own understanding thereof), and
  will guide specific vulnerabilities to investigate once on site.

overview: |2+
    * Passive Reconnaissance
      * Identify availability of staff, partner, beneficiary, and current project information online. [^PETS_logical_intel]
      * Search "paste-bin" sites for leaked internal information or existing exploitation of their infrastructure.
      * Create API keys for Recon-ng services to be used. [^recon-ng_API_keys]
      * Use recon-ng to do automated web-based open source reconnaissance. [^recon-ng_data_flow]

  **Expected Outputs**

    * Dossier of organizational, partner, and beneficiary "open sources" information exposed online.
      * A list of e-mail address for members of the organization.
    * Identification and mapping of externally facing services and unintentionally exposed internal services.
      * Possible vulnerabilities in the websites and externally facing servers of the organization.
      * Existing information about earlier breaches identified in the paste-bin search.
    * Follow the proper incident response plan if high risk problems are identified.


materials_needed: ''
considerations: |2

    * Use VPNs to do automated searching. The automated process can be misconstrued by various services as malicious and cause your local network to get blocked, filtered, or surveilled. Tor is often blocked by the tools you will be using.
walk_through: >

  Both Recon-ng and Foca are open source reconnaissance tools with many
  available plugins. Foca is, out-of-the-box, more aimed at extracting metadata
  from documents and images, whereas Recon is slightly more focused on finding
  digging into domains, subdomains, contacts, and the more network-level
  information.  Both tools are best used in addition to critical thinking and
  manual exploration, and require "seed" inputs to get started and careful
  curation to remove false leads.


  ___
recommendations: ''
---

