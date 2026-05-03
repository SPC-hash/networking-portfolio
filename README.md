# Enterprise Network Troubleshooting Lab (VLAN + ACL Case Study)

## Overview
This project simulates a real-world enterprise network issue involving VLAN misconfiguration, incorrect gateway assignment, and overly restrictive ACL rules. The goal was to diagnose and restore connectivity using structured troubleshooting methods.

The lab was built and tested using Cisco Packet Tracer.

---

## Network Design

The network consists of three segmented departments:

- VLAN 10: HR Department (192.168.10.0/24)
- VLAN 20: IT Department (192.168.20.0/24)
- VLAN 30: Guest Network (192.168.30.0/24)

A router-on-a-stick configuration was used to enable inter-VLAN routing.

---

## Problem Scenario

Users in the HR department reported loss of connectivity:

- Unable to reach gateway
- Unable to communicate with other internal VLANs
- IT department remained fully operational

This indicated a localized configuration issue rather than a full network outage.

---

## Troubleshooting Process

The following systematic approach was used:

### 1. Host-Level Verification
- Verified IP addressing on affected HR hosts
- Identified incorrect default gateway configuration on one endpoint

### 2. Switching Layer Investigation
- Used `show vlan brief` to confirm VLAN membership
- Identified incorrect VLAN assignment on switch access port

### 3. Routing Layer Analysis
- Verified router subinterface configuration
- Confirmed inter-VLAN routing was operational

### 4. Security Policy Review
- Examined ACL configuration using `show access-lists`
- Identified overly restrictive rule blocking HR subnet traffic

---

## Resolutions Implemented

- Corrected VLAN assignment on switch access port
- Fixed default gateway configuration on affected host
- Modified ACL to properly restrict Guest network without impacting HR or IT traffic

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- VLAN segmentation
- Inter-VLAN routing (router-on-a-stick)
- Access Control Lists (ACLs)

---

## Evidence

All supporting screenshots are located in the `/screenshots` directory:

- Network topology
- VLAN configuration output
- Failed connectivity tests
- ACL configuration verification
- Final successful connectivity validation

---

## Key Skills Demonstrated

- Network troubleshooting methodology (Layered approach)
- VLAN configuration and segmentation
- Router subinterface configuration
- ACL-based traffic control
- Root cause analysis in enterprise network environments

---

## Outcome

- Restored full HR department connectivity
- Maintained security isolation for Guest network
- Verified end-to-end communication across VLANs
- Demonstrated structured troubleshooting process aligned with enterprise IT workflows

---
