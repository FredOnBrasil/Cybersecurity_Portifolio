# Threat Modeling for Sneaker Enthusiast Mobile App

## I. Define Business and Security Objectives

- Will the app process transactions? "yes, it will"
- Does it have a user authentication and identity verification system?"yeah, needs to have"
- Are there industry regulations related to payment processing and data privacy (e.g., PCI DSS, GDPR) that need to be considered?"I dont believe so"

## II. Define the Technical Scope

The technologies prioritized for the sneaker app include **API**, **PKI (Public Key Infrastructure)**, and **AES (Advanced Encryption Standard)**. 

- **API**: Prioritized for facilitating seamless communication between different components of the application, enabling smooth user experiences for buying and selling shoes.
- **PKI**: Critical for providing a framework for secure communication.
- **AES**: Ensures data encryption to protect sensitive information during transactions.

## III. Decompose Application

### Sample Data Flow Diagram

1. User opens the app.
2. User registers/signs in (authentication).
3. User searches for sneakers (API call to the database).
4. User lists sneakers for sale (data sent to the server).
5. User makes a transaction (payment processing).
6. Confirmation and notification sent to the user.

## IV. Threat Analysis

- **Internal Threats**: Malicious insider attacks, e.g., employees with access to the database who may manipulate or steal user data.
- **External Threats**: Phishing attacks targeting users to steal credentials or financial information, and Distributed Denial of Service (DDoS) attacks disrupting app availability.

## V. Vulnerability Analysis

- **Codebase Vulnerabilities**: Potential for SQL injection attacks if input validation is insufficient, allowing attackers to manipulate database queries.
- **Weaknesses in the Database**: Misconfigured database permissions could allow unauthorized access to sensitive user information, leading to data breaches.

## VI. Attack Modeling

### Sample Attack Tree Diagram

- **Top Node**: Unauthenticated user accesses sensitive data.
  - **Child Node 1**: Exploit SQL injection vulnerability.
  - **Child Node 2**: Utilize stolen API keys.
  - **Child Node 3**: Phish user credentials through fake application interface.

## VII. Risk Analysis and Impact

1. **Implement multi-factor authentication (MFA)** to strengthen user verification and prevent unauthorized access.
2. **Regular security audits** to identify and remediate vulnerabilities in the code and infrastructure.
3. **Security awareness training** for employees to mitigate social engineering and insider threats.
4. **Encrypt data at rest and in transit** to protect sensitive information against interception and unauthorized access.
