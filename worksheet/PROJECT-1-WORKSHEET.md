# Project 1: Technical Troubleshooting Lab

## Project Overview

This project is a practical technical support and troubleshooting lab focused on developing a structured approach to diagnosing and resolving common computer and network issues.

The project involved working through realistic troubleshooting scenarios, identifying symptoms, gathering relevant information, isolating possible causes, testing solutions, verifying results, and documenting the troubleshooting process.

The main focus areas were Windows troubleshooting, basic network connectivity, DNS fundamentals, application troubleshooting, and technical documentation.

## Troubleshooting Methodology

I used a structured troubleshooting process throughout the project:

1. **Identify the problem** – Understand the reported symptom and define what is not working.
2. **Gather information** – Ask relevant questions about when the issue started, what changed, and whether other applications or devices are affected.
3. **Isolate the problem** – Determine whether the issue is related to the device, network, application, user account, or a specific file/service.
4. **Identify possible causes** – Develop reasonable causes based on the symptoms and information collected.
5. **Test possible causes** – Use appropriate tools and controlled checks to confirm or eliminate possible causes.
6. **Apply a solution** – Make the appropriate change based on the confirmed cause.
7. **Verify the result** – Confirm that the original issue has been resolved and that normal functionality has returned.
8. **Document the process** – Record the symptoms, investigation, tests, results, and resolution for future reference.

## Skills & Tools Practiced

### Technical Troubleshooting Skills

- Problem identification and information gathering
- Systematic troubleshooting and problem isolation
- Basic Windows troubleshooting
- Network connectivity troubleshooting
- Application troubleshooting
- DNS fundamentals
- Technical documentation

### Windows Tools

- Command Prompt
- `ipconfig`
- `ping`
- Task Manager
- Device Manager
- Windows Update
- Built-in Windows troubleshooting tools

### Networking Concepts

- IPv4 addressing
- Subnet mask
- Default Gateway
- Local network connectivity
- Internet connectivity
- DNS and name resolution
- Basic network troubleshooting methodology

## Practical Case 1: Wi-Fi Connected but Websites Would Not Open

### Problem

The laptop showed that it was connected to Wi-Fi, but websites were not opening in the browser.

### Initial Information Gathering

Before changing any settings, I considered the following questions:

- When did the problem start?
- Are other websites affected or only one website?
- Do other internet-dependent applications work?
- Are other devices connected to the same Wi-Fi able to access the internet?
- Is the issue limited to the laptop?

The purpose of these questions was to determine whether the problem was related to the website, the local laptop, or the network/internet connection.

### Problem Isolation

I compared the laptop's connectivity with other devices using the same Wi-Fi network.

If other devices could access the internet normally while the laptop could not, this helped isolate the issue to the laptop rather than immediately assuming that the router or internet service was responsible.

### Network Configuration Check

I used Command Prompt and the `ipconfig` command to inspect the laptop's network configuration.

The active Wi-Fi adapter showed:

- IPv4 address
- Subnet mask
- Default Gateway

Other network adapters displayed as disconnected, which was expected because they were not being used for the active Wi-Fi connection.

### Local Connectivity Test

I used `ping` to test connectivity to the Default Gateway.

The test returned:

- Packets sent: 4
- Packets received: 4
- Packet loss: 0%
- Minimum response: 3 ms
- Maximum response: 43 ms
- Average response: 21 ms

### Result

The successful Default Gateway ping showed that the laptop could communicate with the local router over the network.

This helped narrow the problem further. However, a successful gateway ping does not by itself prove that the laptop has full internet access or that DNS name resolution is working.

### Browser Isolation and Resolution

To further isolate the issue, I tested the website using a different browser on the same laptop.

The website opened successfully in the second browser.

Based on the troubleshooting evidence, the laptop had working local network connectivity, external IP connectivity, and successful DNS resolution. Since the website worked in another browser, the issue was isolated to the original browser rather than the Wi-Fi or internet connection.

### Final Outcome

The troubleshooting process demonstrated that the original browser required further application-level investigation, while the laptop's network connection was functioning correctly.

The investigation was considered complete for this case because the problem had been isolated to the browser layer without making unsupported assumptions about the specific browser fault.

### Key Lesson

A device being connected to Wi-Fi does not automatically prove that internet access is working. Effective troubleshooting requires testing connectivity at different layers and using the results to progressively narrow the scope of the problem.

## Practical Case 2: Microsoft Word Document Not Responding

### Problem

A user reported that Microsoft Word was not working.

### Initial Information Gathering

Rather than immediately assuming that Microsoft Word itself was faulty, I asked questions to understand the exact symptoms:

- When did the problem start?
- Had the document worked previously?
- Does Microsoft Word open normally?
- Do other Word documents open successfully?
- Is the issue affecting one document or multiple documents?

### Problem Isolation

The investigation showed that Microsoft Word itself could open and other Word documents could be opened successfully.

The problem was isolated to one specific document that caused Word to freeze.

### Possible Causes

Based on the symptoms, possible causes included:

- Document corruption
- Compatibility issues
- Problems with content or formatting within the specific document

These were treated as possible causes rather than confirmed causes.

### Troubleshooting Approach

A copy of the affected document could be tested separately to avoid modifying the original file.

The document could also be tested using another compatible application or environment to help determine whether the problem was specific to the document.

### Outcome

The issue was isolated from the Microsoft Word application itself to a specific document.

The investigation demonstrated the importance of identifying the exact scope of an application problem before attempting broad repairs or reinstalling software.

### Key Lesson

When a user reports that an application is not working, the first step should be to identify whether the entire application is affected or whether the problem is limited to a specific file, feature, or task.

## Windows Troubleshooting Tools

During the project, I practiced identifying appropriate built-in Windows tools based on the symptoms being reported.

### Device Manager

Device Manager is used to view and manage hardware devices and their drivers.

I identified Device Manager as an appropriate starting point for hardware-related problems such as a sound issue, where a faulty, missing, or outdated device driver could be a possible cause.

Relevant checks include:

- Locating the affected hardware device
- Checking whether Windows reports a device or driver problem
- Reviewing driver status
- Updating or troubleshooting the relevant driver when appropriate

### Task Manager

Task Manager provides information about running applications, processes, and system resource usage.

I identified Task Manager as an appropriate tool when an application such as Chrome becomes unresponsive.

Relevant checks include:

- Whether the application is responding
- CPU usage
- Memory usage
- Disk usage
- Running processes

Task Manager can help identify resource-related symptoms and determine whether an application needs to be closed and restarted.

### Windows Update

Windows Update can be relevant when troubleshooting problems that may be related to outdated Windows components, security updates, compatibility, or system improvements.

Before applying updates as a troubleshooting step, the reported symptoms should still be understood so that the update is relevant to the problem being investigated.

### Built-in Windows Troubleshooters

Windows includes built-in troubleshooting tools designed to help diagnose certain categories of system problems.

These tools can provide guided checks for issues such as network connectivity, audio, and other Windows components.

### Tool Selection

A key lesson from the project was that troubleshooting tools should be selected based on the symptoms and the scope of the problem.

For example:

| Reported symptom | Appropriate starting tool |
|---|---|
| Sound or hardware-related issue | Device Manager |
| Application is frozen/unresponsive | Task Manager |
| Network connectivity issue | Command Prompt / network tools |
| Windows-related update or compatibility issue | Windows Update |
| Supported Windows component problem | Built-in Troubleshooter |

## DNS Fundamentals

### What is DNS?

DNS stands for **Domain Name System**.

It translates human-readable domain names, such as `google.com`, into IP addresses that computers can use to communicate with network services.

### DNS Troubleshooting Test

During the network troubleshooting case, I tested DNS resolution using:

```text
ping google.com

## Learning Outcomes

By completing this project, I developed practical experience in:

- Applying a structured troubleshooting methodology
- Gathering information before attempting a solution
- Isolating problems by testing different components and layers
- Using `ipconfig` to inspect Windows network configuration
- Using `ping` to test local and external connectivity
- Understanding the role of the Default Gateway
- Understanding basic DNS resolution
- Selecting appropriate Windows troubleshooting tools
- Distinguishing application-specific issues from broader system or network issues
- Documenting troubleshooting findings clearly and accurately
- Using evidence and test results to guide the next troubleshooting step

## Project Reflection

This project reinforced the importance of approaching technical problems systematically rather than immediately applying fixes based on assumptions.

The practical scenarios showed how asking the right questions, isolating the scope of a problem, selecting appropriate diagnostic tools, and interpreting test results can progressively narrow down possible causes.

A major lesson from the project was that a successful troubleshooting process does not always mean immediately identifying a single root cause. In some cases, the most important outcome is accurately isolating the affected layer or component and determining the appropriate next step.
