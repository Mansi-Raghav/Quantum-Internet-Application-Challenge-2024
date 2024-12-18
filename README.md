# Quantum-Internet-Application-Challenge-2024

My idea for the **Quantum Internet Application Challenge 2024** is to develop a **Quantum Token** system. This idea is inspired by quantum money schemes but incorporates variations for practical deployment, especially using the **SquidASM** platform. Below, I provide a detailed explanation of the concept, its implementation, and potential applications.

---

## Overview

The Quantum Token System leverages the unique capabilities of the **quantum internet** to deliver enhanced security and one-time use authentication. Inspired by quantum money, the system provides a practical framework for highly secure, tamper-proof, and unique tokens for authentication and service access. 

Each quantum token consists of:
1. **Serial Number (s):** A unique, publicly known identifier.
2. **Quantum State (∣ψ⟩):** A quantum state tied to the serial number through a pseudorandom function.

The quantum internet enables secure transmission of quantum states over long distances by using entanglement and other quantum communication protocols, making this system possible.

---

## System Components

### 1. Quantum Random Number Generator (QRNG)
QRNGs utilize the inherent unpredictability of quantum mechanics, such as the measurement of photon polarization or phase, to generate truly random values. These values are fundamentally non-deterministic and provide cryptographic-level security. 

- **Example:** A QRNG generates a secret key (k = 100011), which is securely stored by the issuing authority and used to link a serial number to a unique quantum state.

### 2. Pseudorandom Function ((f_k(s))
A pseudorandom function deterministically generates random-looking output from the serial number s and the secret key k. This function ensures that:
- Even if s is publicly known, the output f_k(s) remains unpredictable without k.
- The output of f_k(s) is used to define the quantum state ∣ψ⟩.

- **Example:** For s = 101010 and k = 100011, the pseudorandom function produces f_k(s) = 000011000011.

### 3. Quantum State Generation
The output of f_k(s) determines the basis (computational or Hadamard) and the state for each qubit in ∣ψ⟩. A secure quantum communication protocol (enabled by the quantum internet) ensures the safe delivery of the quantum state to the user.

- **Example:** 
  - 0s in f_k(s) correspond to the computational basis ((|0⟩, |1⟩).
  - 1s in f_k(s) correspond to the Hadamard basis (|+⟩, |-⟩).

From f_k(s) = 000011000011, the quantum state ∣ψ⟩ can be generated by preparing qubits accordingly.

### 4. Verification Mechanism
The token is verified by reconstructing the correct measurement basis using s and k to calculate f_k(s). The quantum state ∣ψ⟩ is then measured, and the outcomes are compared against expected results.

- **Example:** If the measurement outcomes align with the expected results, the token is validated and the service is granted.

---

## Step-by-Step Implementation

### 1. Token Issuance

1. **Secret Key Generation:**
   - A random secret key k is generated using a QRNG and securely stored.
   - **Example:** k = 100011.

2. **Serial Number Assignment:**
   - A unique serial number s is assigned to each token.
   - **Example:** s = 101010.

3. **Quantum State Generation:**
   - The pseudorandom function calculates f_k(s) using s and k.
   - **Example:** f_k(s) = f(101010) = 000011000011.
   - The string f_k(s) determines the basis for each qubit: computational or Hadamard.
   - A quantum state ∣ψ⟩ is prepared using this basis.

4. **Token Delivery:**
   - The token containing s and ∣ψ⟩ is securely delivered to the user.

### 2. Token Verification

1. **Token Submission:**
   - The user submits the token, including s and ∣ψ⟩, for verification.

2. **Basis Reconstruction:**
   - The authority recomputes f_k(s) using s and k to reconstruct the measurement basis.

3. **Quantum State Measurement:**
   - The quantum state ∣ψ⟩ is measured using the reconstructed basis.

4. **Validation and Outcome:**
   - If the measurement outcomes match the expected results, the token is valid and the service is granted. If not, the token is invalidated and cannot be reused.

---

## Advantages

### 1. High Security
- Tokens are inherently secure due to the **No-Cloning Theorem**, which prohibits the replication of unknown quantum states.
- The use of pseudorandom functions ensures that even if s is intercepted, ∣ψ⟩ remains secure.

### 2. One-Time Use
- Tokens are destroyed after verification, preventing reuse or replication.

### 3. Decentralization Ready
- The system can be integrated into decentralized networks, using the quantum internet for secure communication, entanglement distribution, and token validation.

---

## Role of the Quantum Internet

The quantum internet enables secure, large-scale deployment of quantum token systems by providing:
1. **Entanglement Distribution:** Allows secure transmission of quantum states using shared entangled pairs between nodes.
2. **Quantum Key Distribution (QKD):** Facilitates secure exchange of classical and quantum keys.
3. **Teleportation:** Enables the transmission of quantum states ∣ψ⟩ between users without direct physical transport.

---

## Potential Use Cases

1. **Access Control:** 
   - One-time secure entry tokens for sensitive facilities, ensuring no duplication.
2. **Digital Payments:** 
   - A novel payment method leveraging quantum tokens for secure, tamper-proof transactions.
3. **Data Sharing:** 
   - Temporary, one-time secure access to confidential files or resources.

---

This documentation outlines a robust framework for implementing a **Quantum Token System** using the quantum internet. The system is future-proof, leveraging advanced quantum communication protocols for high security, scalability, and practical application.

---

Unfortunately, I was unable to fully implement and test this application on the SquidASM platform due to my current level of familiarity with its functionalities. While I successfully completed the installation process, I encountered technical issues with my credentials for accessing NetQASM and eventually SquidASM, which prevented further progress. Hence, I have not fully completed the challenge, nevertheless, this experience provided valuable insights into the platform's potential, and I am eager to continue exploring and enhancing my understanding of SquidASM for future projects.

---

Thank You.
