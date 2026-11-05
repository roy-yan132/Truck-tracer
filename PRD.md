# Truck Tracer - Product Requirements Document

## 1.Project Overview

The system is designed to provide navigation and monitoring functions for different types of trucks.

## 2.Purpose

This document describes the requirements for the truck navigation and monitoring software.
It defines what the system must do and how well it must do it, and serves as the basis for design, implementation and testing.


## 3.Scope

In scope: GPS, navigation, truck information management, driver behavior and alerts, reporting, user and role management
Out of scope: payroll, cargo billing, maintenance scheduling, integration with third-party ERP systems.

## 4.Users

### Drivers

Drive the truck and use the navigation interface while driving
Need clear, minimal, glanceable information 
Can view their own trips, alerts and driving score

### Managers

Oversee a group of drivers and trucks
Need live-maps, trip history and view driver behavior
Can assign trucks to drivers and review driver behavior

### administrators

Maintain the system
Manage user accounts, roles, permissions, truck records and system configuration

## 5.Functional Requirements

### GPS

The system shall track each truck's real-time location, show it on a map, and store location history for every trip

### Navigation

The system shall provide turn-by-turn routes that take the truck's height, weight and length into account and avoid restricted roads, with ETA and automatic rerouting.

### Truck Info

The system shall store each truck's details (ID, plate number, type, dimensions, weight, cargo type) and its current status

### Driver behavior

The system shall record driving events such as harsh braking, harsh acceleration and sharp cornering, and give each driver a driving score

### Overspeeding

The system shall compare the truck's speed with the road's speed limit, alert the driver when it is exceeded, log the event, and notify the manager of serious cases

## 6.Non-Functional Requirements

### Safety

The driver interface shall minimize distraction and shall not route trucks onto roads that violate their legal restrictions

### Reliability

The system shall be highly available and keep working, with reduced features, when the network connection is lost

### Correctness

Location, speed and ETA information shall be accurate, and over-speeding detection shall produce few false alerts

### Modifiability

The system shall use a modular design so that features, alert thresholds and truck types can be changed without affecting other parts

### Reusability

Core components such as GPS handling and route calculation can be independent modules that can be reused in other applications

### Efficiency

The system shall update locations and calculate routes quickly, and use battery and mobile data economically

### Security & Privacy

The system shall encrypt communication, restrict data access by role, and protect location and driver data in line with GDPR

## 7.Constraints

- Each truck has a GPS-capable device and, most of the time, an internet connection
- Maps, traffic and speed-limit data come from a third-party provider
- The project must be completed by a small student team within the course timeline

