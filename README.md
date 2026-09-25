# Technical Troubleshooting Lab

A hands-on Technical Support project focused on diagnosing, isolating, testing, and documenting common Windows, network, application, and connectivity issues.

## Project Overview

This project demonstrates a structured approach to technical troubleshooting rather than relying on random fixes.

The goal was to investigate realistic support scenarios, identify the likely area of failure, use appropriate Windows tools and commands, test possible causes, and document the findings.

## Objectives

- Apply a systematic troubleshooting methodology.
- Identify and isolate technical problems.
- Troubleshoot basic network connectivity issues.
- Use Windows diagnostic tools and command-line utilities.
- Understand IPv4 addressing, default gateways, ping, and DNS.
- Troubleshoot application and document-related issues.
- Record findings and explain the reasoning behind each troubleshooting step.
- Build interview-defensible practical Technical Support experience.

## Troubleshooting Methodology

The following process was used throughout the project:

1. **Identify the problem** – Understand the user's symptoms and the exact issue.
2. **Gather information** – Ask relevant questions and collect available evidence.
3. **Isolate the problem** – Determine whether the issue affects the device, network, application, or a specific file/service.
4. **Form possible causes** – Identify reasonable causes based on the evidence.
5. **Test** – Use appropriate tools or controlled tests to confirm or eliminate possible causes.
6. **Resolve** – Apply the appropriate fix once the problem area is identified.
7. **Verify** – Confirm that the issue has been resolved.
8. **Document** – Record the symptoms, investigation, findings, and resolution.

## Practical Case 1: Laptop Connected to Wi-Fi but Websites Would Not Open

### Initial Symptoms

A laptop showed that it was connected to Wi-Fi, but websites would not open.

### Initial Investigation

The troubleshooting process included:

- Checking whether other websites were affected.
- Confirming that the internet connection/subscription was active.
- Checking whether other devices connected to the same Wi-Fi could access the internet.
- Checking Windows and browser updates.
- Inspecting the laptop's network configuration.
- Using `ipconfig` to examine the IPv4 address, subnet mask, and default gateway.
- Testing connectivity to the local network gateway using `ping`.

### Network Configuration

The `ipconfig` command was used to inspect the active Wi-Fi adapter.

Important values reviewed included:

- IPv4 Address
- Subnet Mask
- Default Gateway

Sensitive network values are not published in this repository.

### Gateway Connectivity Test

A ping test to the default gateway returned:

- Packets sent: 4
- Packets received: 4
- Packet loss: 0%
- Minimum response: 3 ms
- Maximum response: 43 ms
- Average response: 21 ms

### Interpretation

The successful gateway ping confirmed that the laptop could communicate with the local router over the network.

This result does **not**, by itself, confirm that the laptop has full internet access or that DNS resolution is working.

The next diagnostic step would be to test connectivity to an external IP address, such as:

```text
ping 8.8.8.8

 If the external IP responds but domain names do not resolve that, DNS becomes an area for further investigation.

Practical Case 2: Microsoft Word Document Freezing
Scenario

Microsoft Word was reported as not working.

Instead of immediately assuming that Word itself was the problem, the issue was isolated by asking:

When did the problem begin?
Has the document worked previously?
Does Microsoft Word open normally?
Do other Word documents open successfully?
Findings

Word itself opened successfully and other Word documents could be opened.

The problem was isolated to one specific document.

Possible Causes

Possible causes included:

File corruption
Compatibility issues
Problems contained within the document itself

The appropriate next step would be to test a copy of the document and/or open it using another compatible application to further isolate the cause.

Windows Troubleshooting Tools
Task Manager

Task Manager can be used to investigate application and system performance issues.

Relevant information includes:

CPU usage
Memory usage
Disk usage
Application status
Processes that may be consuming excessive resources
Device Manager

Device Manager is used to view and manage hardware devices and their drivers.

It is useful when investigating issues involving:

Audio devices
Network adapters
Display adapters
Other hardware components
Driver-related problems
Windows Update

Windows Update can be checked when troubleshooting issues that may be related to outdated system components, security updates, or compatibility.

Built-in Windows Troubleshooters

Windows troubleshooting tools can provide automated checks for common hardware, network, audio, and system problems.

DNS Fundamentals

DNS stands for Domain Name System.

DNS translates human-readable domain names into IP addresses so that devices can locate services on a network.

For example:

example.com → IP address

A useful troubleshooting distinction is:

If an external IP address responds to ping but a domain name does not resolve, DNS may be involved.
If the external IP address also cannot be reached, the problem may be related to internet connectivity, routing, firewall settings, or another network issue.
Skills Demonstrated
Systematic troubleshooting
Problem isolation
Basic network troubleshooting
IPv4 fundamentals
Default Gateway
ipconfig
ping
DNS fundamentals
Windows Task Manager
Windows Device Manager
Application troubleshooting
Technical documentation
Evidence-based troubleshooting
Key Lessons

The main lesson from this project was that effective technical support is not about immediately applying random fixes.

A strong troubleshooting process uses evidence to narrow down the problem before making changes.

For example, a successful gateway ping provides evidence of local network connectivity, while a successful external IP ping provides different information about internet reachability.

Project Status

The practical troubleshooting scenarios and core technical concepts have been completed.

GitHub documentation, evidence organization, and portfolio packaging are currently being completed as part of the project.

Evidence

Evidence for the project will include relevant screenshots and supporting documentation.

Sensitive information such as personal IP addresses, account details, passwords, or other private information will not be published.

Interview Defence

This project prepares me to explain:

How I approach a technical support problem.
How I isolate a problem before applying a fix.
What ipconfig is used for.
What a default gateway represents.
What a successful gateway ping tells me.
The difference between local connectivity and internet connectivity.
What DNS does.
When Task Manager is useful.
When Device Manager is useful.
How I would troubleshoot an application or individual document that is not working.

Project: Technical Troubleshooting Lab
Focus: Technical Support / IT Troubleshooting
Status: In Progress – Documentation & Evidence Packaging
