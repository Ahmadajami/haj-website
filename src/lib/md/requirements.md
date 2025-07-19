#####

# System Requirements Document: Ride-Hailing System

This document outlines the system requirements for the ride-hailing platform, designed to function as a smaller-scale clone of Uber.

---

## 1. Introduction

This document details the functional and non-functional requirements for the core ride-hailing system, encompassing the **User Application**, **Driver Application**, and **Admin Dashboard**. The goal is to create an efficient and user-friendly platform for ordering and managing car trips.

---

## 2. Functional Requirements

### 2.1 User Application

-   **FR-UA-001: Car Ordering**  
    The system shall allow users to request a car for a trip.

-   **FR-UA-002: Live Trip View**  
    The User App shall provide a live, real-time view of the ongoing trip, showing the car's location and estimated time of arrival.

-   **FR-UA-003: Trip Type Selection**  
    Users shall be able to choose between different trip types (e.g., 'Premium' and 'Normal') before confirming a ride.

-   **FR-UA-004: Ride Cancellation**  
    Users shall be able to cancel an ordered ride before or during the trip, subject to predefined policies.

-   **FR-UA-005: Payment Integration**  
    The User App shall integrate with a payment system to process ride fares.

-   **FR-UA-006: Driver Details View**  
    Users shall be able to view details of their assigned driver, including name, rating, vehicle type, and license plate number.

-   **FR-UA-007: Trip Sharing**  
    Users shall be able to share their live trip details (e.g., current location, ETA, driver details) with selected contacts.

### 2.2 Driver Application

-   **FR-DA-001: Customer Matching**  
    The system shall enable drivers to receive notifications for the nearest available customer requests.

-   **FR-DA-002: Request Acceptance/Rejection**  
    Drivers shall be able to accept or reject incoming ride requests.

-   **FR-DA-003: Driver Availability Status**  
    Drivers shall be able to set their availability status (e.g., online, offline) to receive or stop receiving ride requests.

-   **FR-DA-004: Live Location Sharing**  
    The Driver App shall continuously transmit the driver's real-time location to be displayed on the User App during a trip.

-   **FR-DA-005: Trip Navigation**  
    The Driver App shall provide navigation assistance for the trip route.

-   **FR-DA-006: Trip Completion**  
    Drivers shall be able to mark a trip as completed upon reaching the destination.

### 2.3 Notification System

-   **FR-N-001: Ride Request Notification**  
    The system shall send notifications to drivers for new ride requests.

-   **FR-N-002: Ride Acceptance/Rejection Notification**  
    The system shall notify users when a driver accepts or rejects their ride request.

-   **FR-N-003: Driver Arrival Notification**  
    The system shall notify users when their assigned driver is approaching or has arrived at the pickup location.

-   **FR-N-004: Trip Start/End Notification**  
    The system shall send notifications to both users and drivers at the start and end of a trip.

-   **FR-N-005: Payment Confirmation Notification**  
    The system shall notify users upon successful payment processing for a trip.

### 2.4 Admin Dashboard (Backend Management)

-   **FR-AD-001: User Management**  
    Admins shall be able to view, add, edit, and delete user accounts.

-   **FR-AD-002: Driver Management**  
    Admins shall be able to view, add, edit, and delete driver accounts, including their vehicle details and status.

-   **FR-AD-003: Trip Management**  
    Admins shall be able to view, search, and manage ongoing and historical trip data.

-   **FR-AD-004: Pricing Configuration**  
    Admins shall be able to configure and adjust pricing for different trip types and regions.

-   **FR-AD-005: Sales Point System**  
    The dashboard shall include a sales point system for drivers to manage and pay their commissions or fees to the agency.

-   **FR-AD-006: Reporting & Analytics**  
    The dashboard shall provide reports and analytics on:

    -   Number of active users and drivers.
    -   Number of completed trips.
    -   Revenue generated.
    -   Driver earnings and payments.
    -   Trip duration and distance metrics.

-   **FR-AD-007: Support & Dispute Resolution**  
    Admins shall have tools to handle customer and driver support inquiries and resolve disputes.

---

## 3. Non-Functional Requirements

### 3.1 Performance

-   **NFR-P-001: Response Time**  
    All critical user and driver interactions (e.g., requesting a ride, accepting a request) shall have a response time of less than 2 seconds under normal load.

-   **NFR-P-002: Scalability**  
    The system shall be able to handle a growing number of concurrent users, drivers, and trips without significant degradation in performance.

### 3.2 Security

-   **NFR-S-001: Data Protection**  
    All sensitive user and driver data (e.g., personal information, payment details, trip history) shall be encrypted both in transit and at rest.

-   **NFR-S-002: Access Control**  
    Access to the Admin Dashboard and its functionalities shall be restricted to authorized personnel based on role-based access control (RBAC).

-   **NFR-S-003: Authentication & Authorization**  
    The system shall implement secure authentication mechanisms for users and drivers, and robust authorization checks for all actions.

### 3.3 Usability (UI/UX provided by Haj@ Agency)

-   **NFR-U-001: Intuitive Interface**  
    The User App, Driver App, and Admin Dashboard shall adhere to the provided UI/UX designs, ensuring an intuitive and user-friendly experience across all platforms.

-   **NFR-U-002: Clarity of Information**  
    All information presented to users and drivers (e.g., trip details, earnings, prices) shall be clear, concise, and easily understandable.

### 3.4 Reliability

-   **NFR-R-001: High Availability**  
    The core ride-hailing system shall be available 99.9% of the time, minimizing service interruptions.

-   **NFR-R-002: Data Integrity**  
    All trip, user, and driver data shall be consistent and accurate, with robust mechanisms to prevent data corruption.

### 3.5 Maintainability

-   **NFR-M-001: Code Modularity**  
    The system's codebase shall be modular and well-documented to facilitate future enhancements, bug fixes, and maintenance.

-   **NFR-M-002: Configuration Flexibility**  
    The system shall allow for easy configuration changes (e.g., pricing, trip types, notification settings) without requiring extensive code modifications.

### 3.6 Compatibility

-   **NFR-C-001: Platform Compatibility**  
    The User and Driver Apps shall be compatible with major mobile platforms (iOS and Android). The Admin Dashboard shall be compatible with modern web browsers.

-   **NFR-C-002: System Integration**  
    The system shall seamlessly integrate with third-party services as required (e.g., mapping services, payment gateways, SMS/email providers for notifications).

---

## 4. Assumptions

-   **AS-001:** Haj@ Agency will provide complete and finalized UI/UX designs for all user-facing, driver-facing, and admin-facing components of the ride-hailing system.
-   **AS-002:** Haj@ Agency will provide a comprehensive marketing plan that may influence certain system functionalities or data collection requirements.
-   **AS-003:** Necessary third-party API keys and credentials (e.g., for mapping, payment gateways) will be provided by Haj@ Agency or acquired as part of the project.
