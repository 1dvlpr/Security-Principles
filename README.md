# Security Principles

## Introduction
Espionage refers to the covert collection of information, typically concerning national security, military, or corporate affairs, often for a government or organization. Understanding security principles is crucial to mitigating risks and ensuring the safety of sensitive data.

## Objective
The purpose of this guide is to introduce key security concepts and models, including:
- The Security Triad: Confidentiality, Integrity, and Availability (CIA)
- The opposite of CIA: Disclosure, Alteration, and Destruction/Denial (DAD)
- Fundamental security models such as the Bell-LaPadula model, Biba Model, and Clark-Wilson Model
- Security principles including Defense-in-Depth, Zero Trust, and Trust but Verify
- ISO/IEC 19249 standards
- The distinction between Vulnerability, Threat, and Risk

## The CIA Triad
The CIA Triad is the foundation of information security:
- **Confidentiality**: Ensures that only authorized individuals or systems can access data.
- **Integrity**: Protects data from unauthorized alterations and ensures modifications are detectable.
- **Availability**: Ensures systems and services remain accessible when needed.

### Real-World Applications
#### Online Shopping:
- **Confidentiality**: Credit card details should only be shared with the payment processor.
- **Integrity**: Unauthorized modifications to order details can misroute deliveries.
- **Availability**: If an online store is down, customers cannot make purchases.

#### Healthcare:
- **Confidentiality**: Medical records must be protected under legal compliance.
- **Integrity**: Altering patient records can lead to incorrect treatments.
- **Availability**: Doctors need access to records for accurate diagnoses.

## Beyond CIA: Additional Security Principles
### Authenticity & Non-Repudiation
- **Authenticity**: Ensures that data originates from a verified source.
- **Non-repudiation**: Prevents denial of a previously performed action (e.g., an order confirmation).

### The Parkerian Hexad
In 1998, Donn Parker expanded the security model with additional elements:
1. **Availability** - Ensuring uptime and accessibility
2. **Utility** - Ensuring data remains usable
3. **Integrity** - Preventing unauthorized modifications
4. **Authenticity** - Verifying data origins
5. **Confidentiality** - Restricting access to authorized entities
6. **Possession** - Preventing unauthorized control or copying

## The DAD Model
The DAD model represents threats to security:
- **Disclosure**: Unauthorized access to confidential data
- **Alteration**: Unauthorized modification of data
- **Destruction/Denial**: Disrupting access to critical systems

Understanding both CIA and DAD helps in creating robust security strategies to protect against cyber threats and vulnerabilities.

## Fundamental Security Models
### Bell-LaPadula Model
The Bell-LaPadula Model is designed to ensure **confidentiality** through three rules:
- **Simple Security Property ("No Read Up")**: Subjects at a lower security level cannot read objects at a higher security level, preventing unauthorized access.
- **Star Security Property ("No Write Down")**: Subjects at a higher security level cannot write to objects at a lower security level, preventing leaks of sensitive information.
- **Discretionary Security Property**: Uses an access control matrix to define who can read or write specific objects.

This model is commonly used in government and military applications but has limitations, such as difficulty handling file-sharing scenarios.

### Biba Integrity Model
The Biba Model focuses on **integrity** rather than confidentiality. It enforces:
- **Simple Integrity Property ("No Read Down")**: A subject with higher integrity cannot read data from a lower integrity level to prevent contamination.
- **Star Integrity Property ("No Write Up")**: A subject with lower integrity cannot write to higher integrity levels to prevent corruption.

This model is critical for ensuring that data remains trustworthy, particularly in financial and industrial control systems. However, it does not address insider threats effectively.

### Clark-Wilson Model
The Clark-Wilson Model also ensures **integrity** but introduces more granular control mechanisms:
- **Constrained Data Items (CDIs)**: Data that must be protected.
- **Unconstrained Data Items (UDIs)**: General data that does not require strict integrity enforcement.
- **Transformation Procedures (TPs)**: Controlled operations that can modify CDIs while maintaining integrity.
- **Integrity Verification Procedures (IVPs)**: Checks to ensure CDIs remain valid.

This model is widely used in commercial applications, such as financial transactions and database management, ensuring integrity through well-defined workflows.

By understanding these principles and models, we can better assess and improve security measures to protect sensitive information across different domains.


Here's a structured README for your content:

---

# ISO/IEC 19249:2017 - Security Techniques  

## Overview  
The **International Organization for Standardization (ISO)** and the **International Electrotechnical Commission (IEC)** have established **ISO/IEC 19249:2017**, which outlines security principles for designing secure products, systems, and applications.  

This document provides an overview of **five architectural principles** and **five design principles** that help in building secure systems.  

---

## Architectural Principles  

1. **Domain Separation**  
   - Groups related components as single entities with common security attributes.  
   - Example: x86 processor privilege levels (Ring 0 for OS kernel, Ring 3 for user-mode apps).  

2. **Layering**  
   - Structures systems into layers to enforce security policies.  
   - Example: OSI Model in networking, where each layer provides specific services.  

3. **Encapsulation**  
   - Hides low-level implementation details and restricts direct data manipulation.  
   - Example: Object-oriented programming (OOP) using `increment()` instead of direct variable modification.  

4. **Redundancy**  
   - Ensures availability and integrity through duplicate components.  
   - Example: RAID 5 storage, where data remains accessible even if a drive fails.  

5. **Virtualization**  
   - Shares hardware across multiple OS instances, enhancing security and sandboxing.  
   - Example: Cloud services using virtual machines for isolation.  

---

## Design Principles  

1. **Least Privilege**  
   - Restricts access to only what is necessary for a user’s role.  
   - Example: Granting read access without write permissions when unnecessary.  

2. **Attack Surface Minimization**  
   - Reduces vulnerabilities by limiting exposure.  
   - Example: Disabling unnecessary services in a Linux system.  

3. **Centralized Parameter Validation**  
   - Ensures all user inputs are validated centrally to prevent exploits.  
   - Example: Validating form inputs to prevent SQL injection.  

4. **Centralized General Security Services**  
   - Unifies security services to maintain consistency and control.  
   - Example: A centralized authentication server instead of distributed credentials.  

5. **Error and Exception Handling**  
   - Designs systems to handle failures securely.  
   - Example: Firewalls should block all traffic by default when they fail.  

---

## Usage Instructions  

When answering security-related questions, refer to the **ISO/IEC 19249 design principles** and select the appropriate principle:  

| **Principle Number** | **Design Principle** |
|----------------------|----------------------|
| 1 | Least Privilege |
| 2 | Attack Surface Minimization |
| 3 | Centralized Parameter Validation |
| 4 | Centralized General Security Services |
| 5 | Error and Exception Handling |

---

## References  
- [ISO/IEC 19249:2017 Official Documentation](https://www.iso.org/standard/64766.html)  
- Security best practices based on ISO standards.  

---
Here's a cleaner, more structured version of your README:

---

# Zero Trust vs. Trust but Verify

Trust is an essential part of how we function, but in cybersecurity, it must be approached with caution. If we suspect that a laptop vendor has installed spyware, we may rebuild the system. If we mistrust the hardware itself, we might stop using it altogether. In business and cybersecurity, trust becomes even more complex, requiring strong guiding principles.

Two key security models address trust:

1. **Trust but Verify**
2. **Zero Trust**

## Trust but Verify

This principle suggests that even when we trust an entity—whether a user, device, or system—we should always verify its actions. Verification typically involves logging and monitoring mechanisms to ensure expected behavior. 

### Challenges:
- Verifying every action manually is impractical.
- Automated security solutions like **proxy servers, intrusion detection systems (IDS), and intrusion prevention systems (IPS)** are necessary.

## Zero Trust

Zero Trust operates on the idea that **trust itself is a vulnerability**. This model assumes that all entities, even internal ones, could be threats. It follows the principle: **“Never trust, always verify.”**

### Key Features:
- No implicit trust based on device location or ownership.
- Requires authentication and authorization for every access request.
- Limits the damage of security breaches.

### Microsegmentation:
One of Zero Trust’s implementations, **microsegmentation**, breaks networks into smaller, controlled segments. Each segment enforces strict access control and authentication, reducing lateral movement in case of a breach.

## Balancing Trust and Security

While Zero Trust enhances security, applying it excessively may disrupt business operations. The goal is to **implement it effectively without unnecessary overhead**.

By strategically applying **Trust but Verify** and **Zero Trust**, organizations can build a more resilient security posture.

---

# Threat Versus Risk
here are three terms that we need to take note of to avoid any confusion.

- Vulnerability: Vulnerable means susceptible to attack or damage. In information security, a vulnerability is a weakness.
- Threat: A threat is a potential danger associated with this weakness or vulnerability.
- Risk: The risk is concerned with the likelihood of a threat actor exploiting a vulnerability and the consequent impact on the business.
Away from information systems, a showroom with doors and windows made of standard glass suffers a weakness, or vulnerability, due to the nature of glass. Consequently, there is a threat that the glass doors and windows can be broken. The showroom owners should contemplate the risk, i.e. the likelihood that a glass door or window gets broken and the resulting impact on the business.

Consider another example directly related to information systems. You work for a hospital that uses a particular database system to store all the medical records. One day, you are following the latest security news, and you learn that the used database system is not only vulnerable but also a proof-of-concept working exploit code has been released; the released exploit code indicates that the threat is real. With this knowledge, you must consider the resulting risk and decide the next steps.
