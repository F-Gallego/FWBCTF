# FortiWeb
**FortiWeb** is Fortinet's Web Application and API security platform, enabling enterprise customers to protect web applications no matter where they are deployed. FortiWeb defends web applications and APIs against OWASP Top-10 threats, DDOS attacks, and malicious bot attacks. Advanced ML-powered features improve security and reduce administrative overhead. Capabilities include anomaly detection, API discovery and protection, bot mitigation, and advanced threat analytics to identify the most critical threats across all protected applications.

## Overview
In this lab, you will have an opportunity to configure FortiWeb to protect a Juice Shop server, emulating a very vulnerable e-commerce website. In the interest of time, we will perform relatively simple SQL injection attacks to highlight both signature based and Machine Learning powered Application securtiy.

## Objectives
In this lab:

* You will configure Server objects, Virtual servers, and Server policies on the FortiWeb-VM via the FortiWeb GUI to install and enable webservers (Juice-Shop, DVWA and other applications) hosted in GCP access to the internet and then enable Virtual IPs to protect the web servers against OWASP Top 10 and other web attacks by the FortiWeb.
* You may find some flags... not sure

---
buttons:
  - title: Hands on Lab - Download
    icon: material-file-download-outline
    attributes:
      class: md-content__button md-icon
      href: ../hands-on-labs.pdf
      target: _blank
---