OSIM – Organizational Simulation and Internal Management System

Project Overview

OSIM (Organizational Simulation and Internal Management System) is a C++ project developed for the CS-1004 Object-Oriented Programming course at FAST-NUCES (National University of Computer & Emerging Sciences) during the Spring 2025 semester. The system simulates an organizational environment where users with distinct roles—Junior, Manager, Director, and Executive—interact through secure task management, encrypted messaging, and comprehensive activity logging. Built without using the C++ Standard Template Library (STL), OSIM emphasizes core OOP principles such as inheritance, polymorphism, operator overloading, and manual memory management.

Features
Role-Based Access Control (RBAC): Implements a strict access control system using a PolicyEngine class to enforce permissions based on user roles and clearance levels.
Secure Authentication: Supports user login with hashed passwords stored in users.txt and multi-factor authentication (MFA) using one-time passwords (OTPs) sent via secure messaging.
Task Management: Allows task creation, assignment, delegation, and tracking with statuses (Created, Assigned, InProgress, Completed, Expired). Tasks include a Time-To-Live (TTL) mechanism for automatic expiry, managed recursively.
Secure Messaging: Supports three message types (INFO, PRIVATE, ALERT) with PRIVATE messages encrypted for the intended recipient only. Messages are stored in inbox.txt and routed based on clearance levels.
Audit Logging: Logs all significant actions (login/logout, task updates, message transmissions) in an append-only audit.txt file using the << operator for immutable tracking.
Performance Review System: Tracks task completion rates, deadline adherence, and message interactions to generate performance scores, output using overloaded operators.
Audit Anomaly Detection: Monitors audit logs for suspicious activities (e.g., excessive task reassignments or unusual login times) and generates alerts.
Global Notification System: Enables Managers and Executives to send system-wide notifications (WARNING, EMERGENCY) logged and stored in the system.
Task Priority System: Supports task prioritization (High, Medium, Low) to manage delegation and execution order.

Technical Details
Language: C++ (no STL containers or smart pointers)

OOP Principles:

Inheritance: Multi-level hierarchy with Junior → Employee → Manager → Director → Executive.
Polymorphism: Runtime polymorphism using base class pointers for dynamic behavior.
Operator Overloading: Implements +=, <<, ==, and () operators for task handling, logging, and comparisons.


File Handling: Manual file operations for:

users.txt: Stores hashed user credentials.
tasks.dat: Serializes task data in binary format.
audit.txt: Logs all system activities.
inbox.txt: Stores user messages.
Memory Management: Uses pointers and manual memory allocation/deallocation.
Constraints: Minimum 15 distinct classes, recursion for TTL and delegation logic, and no hardcoded permission checks.









Bonus Features (Optional)




Digital signatures for task approvals (hash of username + timestamp).
Cycle detection in task delegation chains.
Encrypted binary log files.
ASCII-art-based GUI dashboard.

Learning Objectives

Master multi-level inheritance and runtime polymorphism.
Implement secure access control and credential management.
Develop manual file handling and serialization for persistent data storage.
Create immutable audit logs and detect anomalies.
Apply operator overloading for intuitive task and performance management.

