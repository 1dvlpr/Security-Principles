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

