# IKSHANA
## The Fake Vote Invigilator

> **A real-time voter authentication layer designed to detect duplicate voting and identity fraud across polling booths.**

**GitHub:** https://github.com/MonikaRGowda/ikshana


## 1. Project Overview

**Ikshana** is a full-stack web application designed to strengthen voter authentication at polling booths.

The central idea is **A voter should not be able to authenticate twice, even if the second attempt happens at another booth.**

The prototype introduces a real-time authentication layer between voter verification and the actual voting process. It combines **Voter ID verification, fingerprint verification, facial verification, fraud detection, and real-time cross-booth synchronization**.

A key design principle is that Ikshana is an **authentication gateway**, not part of the voting process itself. It verifies identity and whether a person has already authenticated, but it does not record or influence the voter's ballot choice.

<img width="1254" height="1254" alt="4febbb89-81d6-4353-b488-96a0f7f015b1" src="https://github.com/user-attachments/assets/d6ac3f1b-8ffd-4925-85a6-def672e7f6ef" />


#  The Problem

The existing approach has several limitations:

###  Manual verification
The indelible ink mark on a voter's finger is physically inspected by polling personnel. This process is manual and can be difficult to verify consistently.

###  Isolated polling booths
Individual booths do not automatically share voter authentication status in real time.

###  Identity and impersonation risk
A fraudulent person may attempt to use another voter's identification to pass through a conventional identity check.

###  Limited digital auditability
Authentication and fraud attempts are not represented in one centralized, real-time digital trail.



#  The Proposed Solution

Ikshana addresses this gap by introducing a **triple-factor authentication checkpoint**.
##  Triple-Factor Authentication

Ikshana combines three verification layers:

**Voter ID + Fingerprint + Face**
The authentication event is then synchronized across connected booths.
The multiple checks strengthen the authentication process before a voter proceeds to the voting stage.

The flow is:

<img width="806" height="613" alt="image" src="https://github.com/user-attachments/assets/1b9900c6-bbb6-407c-b161-3c9d607db3c7" />


##  Real-Time Cross-Booth Synchronization

Authentication events are broadcast through **Socket.IO**.

When a voter is authenticated at Booth A, the relevant authentication state can be propagated to Booth B and Booth C.

This removes the dependency on isolated, booth-level knowledge.

##  Multi-Scenario Fraud Detection

Ikshana is designed around three fraud scenarios.

### Scenario 1: Duplicate Voting

A voter who has already authenticated attempts to authenticate again using the same identity.

**Result:** The attempt is blocked and recorded as a duplicate voting attempt.

### Scenario 2: Identity Fraud

The biometric identity is associated with a different Voter ID from the one presented.

**Result:** The attempt is classified as identity fraud / impersonation.

### Scenario 3: Voter ID Forgery

The presented Voter ID exists, but the biometric identity does not match the registered identity.

**Result:** The attempt is classified as Voter ID forgery / impersonation.


#   Biometric Authentication

## Fingerprint Verification

The prototype integrates **Mantra MFS fingerprint biometric technology** for voter authentication.

The voter's fingerprint is captured using the Mantra MFS scanner and processed through the biometric verification workflow. 
If fingerprint verification fails or the fingerprint quality is insufficient, the system can use facial verification as a fallback to complete the authentication process.

## Face Verification

Facial verification is performed using **DeepFace**.

The face workflow provides an additional biometric layer and serves as the fallback when fingerprint verification is not sufficiently reliable.


#  Database Architecture

The system uses PostgreSQL for election data and fraud logging.

The architecture separates temporary election information from the permanent fraud record.

```text
                    PostgreSQL
                        │
              ┌─────────┴─────────┐
              │                   │
              ▼                   ▼
       Election Database      Fraud Log
          Temporary            Permanent
              │                   │
        Voter State          Fraud Events
        Election State        Audit Records
```

The election database is intended to exist only for the duration of polling. Before it is removed, flagged fraud information is preserved in the permanent fraud log.


#  Technology Stack

 Frontend -> React.js 
 Backend -> Python 
 API Framework -> FastAPI 
 Database -> PostgreSQL 
 Real-time communication -> Socket.IO 
 Python Socket.IO implementation -> python-socketio 
 Face verification -> DeepFace 
 Fingerprint integration -> Mantra MFS100 
 Synthetic data generation -> Python Faker 


#  Application Workflow

The complete authentication workflow is:

```text
1. Voter arrives at polling booth
              ↓
2. Voter ID is entered / verified
              ↓
3. Voter record is checked
              ↓
4. Fingerprint is scanned
              ↓
5. Fingerprint is verified / hashed
              ↓
6. Face is captured and verified
              ↓
7. Fraud scenarios are checked
              ↓
8. Cross-booth state is checked
              ↓
        ┌─────┴─────┐
        ▼           ▼
    Verified       Fraud
        │           │
        ▼           ▼
   Allow voter    Block
   to proceed       +
                   Alert
                    +
                   Log
```

#  Booth Interface

The booth terminal is designed for polling officers to perform voter authentication.

The interface supports the authentication workflow and communicates with the backend for voter verification and fraud detection.
It also provides place holder for fingerprint and face authentication.

#  Admin Dashboard

The administrator interface provides centralized visibility into the election authentication process.

The dashboard is designed to display:

- Election status
- Active booth status
- Authentication activity
- Fraud alerts
- Fraud classifications
- Audit information
- Real-time updates

#  Real-World Deployment Considerations

The prototype operates on a local network. A real election deployment would require secure and reliable communication infrastructure.

The project's proposed deployment path is integration with **NIC government infrastructure and VSAT connectivity**, especially for remote polling booths.

The actual voting mechanism remains separate from this authentication system.



#  Project Data

The prototype uses **synthetic voter data** for demonstration.

The dataset includes fields such as:

- Name
- Relative name
- Relative type
- Date of birth
- Gender
- Phone number
- Address
- Voter ID
- Constituency
- Booth ID
- Part number

The project documentation states that more than 1,000 synthetic voter records are generated using Python Faker with the Indian locale.

<img width="648" height="805" alt="image" src="https://github.com/user-attachments/assets/9367f323-98ac-4354-a859-46c67ac20230" />

> * Synthetic voter dataset used for demonstration.*



#   Limitations

The current prototype has important limitations:

1. **Rural network connectivity:** The system is not designed for sustained offline operation.
2. **Biometric hardware provisioning:** Real deployment would require dedicated and certified fingerprint scanners and cameras.
3. **Biometric edge cases:** Fingerprint quality and poor lighting can affect authentication.
4. **Power failures:** Complete independent power-failure recovery is not implemented.
5. **National-scale load:** The prototype has not been tested with thousands of simultaneous booths.
6. **Production encryption:** End-to-end encryption is required before real-world deployment.
   

# Future Scope

## 1. End-to-End Encryption
Implement SSL/TLS encryption for all communication between booths and the central server.

## 2. Offline Resilience
Introduce a booth-level queue that stores authentication attempts during temporary connectivity loss and synchronizes them when the connection returns.

## 3. Advanced Biometrics
Explore **iris recognition** to improve authentication accuracy and reduce false acceptance.

## 4. Tamper-Proof Audit Trail
Explore blockchain-based fraud records to create an immutable audit trail.

## 5. National-Scale Deployment
Explore **NIC + VSAT integration** and a scalable architecture capable of supporting thousands of booths and millions of voters.


#  Screenshot Gallery

>  **Login**

<img width="1876" height="831" alt="image" src="https://github.com/user-attachments/assets/035afb3f-ac83-4042-b679-d5460c8bee05" />


> **Booth Dashboard**

<img width="1906" height="820" alt="image" src="https://github.com/user-attachments/assets/50bef44c-804e-49d0-b768-11ed206a48fd" />


>  **Voter Verification**

<img width="1864" height="800" alt="image" src="https://github.com/user-attachments/assets/9fa5ef35-e0c7-497d-810d-98c29a9ff7a9" />


>  **Fingerprint Verification**

<img width="1305" height="660" alt="image" src="https://github.com/user-attachments/assets/443b3b61-5d60-4bee-87f5-39e5a414d8c4" />


>  **Face Verification**

<img width="1276" height="738" alt="image" src="https://github.com/user-attachments/assets/1fd27f64-f214-4d20-b043-ac7e26f90a32" />


>  **Successful Authentication**

<img width="1873" height="831" alt="image" src="https://github.com/user-attachments/assets/3c3415ec-abac-4390-a562-8942257ac19f" />


>  **Duplicate Voting Alert**

<img width="646" height="524" alt="image" src="https://github.com/user-attachments/assets/89ccff10-4168-4e19-a0f0-0254b1ad88c8" />


>  **Identity Fraud Alert**

<img width="1840" height="691" alt="image" src="https://github.com/user-attachments/assets/f1f9bedd-0445-425f-a828-e0bfb63d06f1" />

>  **Admin Dashboard**

<img width="1846" height="859" alt="image" src="https://github.com/user-attachments/assets/b1ac289c-2bf1-43f8-a649-31ff60d082df" />


>  **Audit Log**

<img width="1243" height="775" alt="image" src="https://github.com/user-attachments/assets/08ff050d-6f06-4722-b50b-df6ffdcae790" />

