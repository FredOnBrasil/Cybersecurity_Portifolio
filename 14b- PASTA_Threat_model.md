# Business and Security Objectives

## I. Define Business and Security Objectives

### Specific Business Requirements:
1. **User Profile Management:**
   - Users should be able to create and manage their profiles within the app. They should also have the option to connect their profiles to external accounts (e.g., social media or other platforms) for ease of access.
  
2. **Financial Transaction Processing:**
   - The application must support secure and seamless financial transactions for users, ensuring that payment data is processed accurately and efficiently.

3. **Regulatory Compliance:**
   - The application must comply with the Payment Card Industry Data Security Standard (PCI-DSS) to ensure that all financial transactions and sensitive data handling meet industry security standards.

## II. Define the Technical Scope

### Technologies Used by the Application:
1. **Application Programming Interface (API):**
   - Facilitates communication between the application, users, and external systems, enabling functionality such as user authentication and financial transactions.

2. **Public Key Infrastructure (PKI):**
   - Used for securing communication through encryption and digital signatures, aiding in user identity verification.

3. **Advanced Encryption Standard (AES):**
   - Employed for encrypting sensitive data at rest and in transit to ensure confidentiality and integrity.

4. **SHA-256:**
   - A cryptographic hash function used for data integrity verification, primarily for passwords and transaction details.

5. **SQL:**
   - Utilized for database management and data retrieval operations, which must be secured against SQL injection attacks.

## III. Decompose Application

### Sample Data Flow Diagram:
- Create a diagram illustrating the flow of data between users, the mobile application, external systems (for external accounts), payment gateways, and the database. This should show the entry points for user data, transaction processing paths, and how data is stored.

## IV. Threat Analysis

### Types of Threats:
1. **Injection:**
   - An attacker might exploit vulnerabilities in the application, such as SQL injection or command, allowing unauthorized access or manipulation of the application’s database.

2. **Session Hijacking:**
   - An attacker could take control of a user's session by stealing session tokens, leading to unauthorized actions being performed on behalf of the user.

## V. Vulnerability Analysis

### Vulnerabilities:
1.Lack of Prepared Statements:**
   - The application may be using dynamic SQL queries that are susceptible to SQL injection attacks if user inputs are not properly sanitized and validated.

2. **Broken API Token:**
   - If the API tokens used for authenticating requests are poorly managed or insecure, they could be intercepted or reused by malicious actors, leading to unauthorized access to user or transactions.

## VI. Attack Modeling

### Sample Attack Tree Diagram:
- Create an attack tree diagram that shows possible attack vectors for the identified threats and vulnerabilities. For example:
  - **Root Goal:** Compromise User Data
    - **Attack Vector 1:** Exploit Session Hijacking
      - Sub-attack: Intercept session tokens
      - Sub-attack: Use stolen credentials
    - **Attack Vector 2:** Execute Injection Attack
      - Sub-attack: SQL Injection via login form
      - Sub-attack: Command injection through API

---

This framework provides a structured approach to the business and security objectives, technological scope, threat landscape, vulnerabilities, and possible attack pathways for the application.
