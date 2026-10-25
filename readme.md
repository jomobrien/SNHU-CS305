# SNHU-CS305: Software Security
**Term:** September - October 2026

## Overview
This repository contains coursework from Software Securities, specifically the final project, a security review and recommendations document.

## Essential Questions & Professional Reflection

### Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?
Artemis Financial is a financial advisor wanting to hire a security consultant to review their web portal to ensure they were following best practices.
Given the company handles both personal and financial information, the company must ensure encryption both end-to-end and at rest. They must generate a certificate and should submit that to a Certificate Authority.
Additionally, their existing code needs to be updated to ensure secure practices and that their dependencies have no known security vulnerabilities.

### What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?
Finding all software security vulnerabilities requires a thorough examination of all aspects of the code. The greatest vulnerabilities are present where systems interact with one another, especially where internal and external systems interact.
This is both open API endpoints, as well as when the system interacts with other systems' endpoints. Modern Java code is built on huge libraries of existing code, so it is important to keep those updated to avoid potential security vulnerabilities.
Original code must also be scrutinized, especially where the endpoint receives data. Malicious actors can use erroneous data either to circumvent security or to overload the system with error messages.

As for the value software security adds to a company, the impact is immeasurable. Any modern company uses their computer systems to store and process data, to house systems vital to their workflow, and for any number of other reasons.
To a company like Artemis Financial, poor security could lead to massive fines for negligence, but even for companies that don't handle personal data, malware can cost a company millions of dollars. A single cyber security event could bankrupt many companies.

### Which part of the vulnerability assessment was challenging or helpful to you?
I've always enjoyed puzzles and closely inspecting things to properly understand them. For challenging, I would probably say that modern encryption is much more complicated than I had realized.
While doing research for homework assignments, I learned about how modern encryption uses linear alegebra to simultaneously build a shared secret key without ever transmitting it, which I found to be really fascinating.

### How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?
I would think of security in two ways: One is ensuring the code itself is secure. This isn't just ensuring there are no vulnerabilities at the endpoints. If a future vulnerability is found, proper encapsulation can restrict the malicious actor's ability to effect the system.
After you are reasonably certain the code has no security vulnerabilities, I would closely examine exactly how data flows between server and client. What are the networks and firewalls? Could encryption and transmission be improved to ensure the data is secure even after it has left the system?

### How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
The first steps are compiling the code to ensure there are no compile time errors. The code should be run to search for runtime errors. In this case, the code was limited, but in more complicated code, test cases should be created to limit test edge cases.
Before any release, dependency checks should be run to ensure there are no new vulnerabilities. Even if your code didn't add new ones, it is possible vulnerabilities have been found since your last release.

### What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
We learned about encryption algorithms, like AES-256, and encryption protocols, like TLS 1.3. We learned about how hashing algorithms, like SHA-256, ensure data integrity. Hashing can be used to ensure the data received is the same as the data that was originally sent.
We learned about Maven, an incredible tool for adding and updating Java libraries that add massive tools for security while requiring minimal code from the programmer. We were also shown a security review flowchart emphasizing the different areas of security vulnerabiliites to search for.

### Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?
I think if I wanted to use this assignment to show future employers, I would want to actually update the code to remove the security vulnerabilities from dependencies rather than ignoring them. I would likely also update to TLS 1.3 protocols and include a Diffie-Hellman key exchange.
