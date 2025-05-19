# Smart Home Energy Management System - Final Exam 

## 📌 Project Overview
**Course:** Database Development with PL/SQL (INSY 8311)  
**Student:** NGIRINSHUTI MUGISHA Joachim  
**Student ID:** 27256  
**Lecturer:** Eric Maniraguha  


---

## 🎯 Problem Definition-Phase I: Problem Statement
**Title:** Smart Home Energy Management System  
**Objective:**  
Develop an IoT-driven Oracle database solution to monitor, control, and optimize residential energy consumption using PL/SQL.  

**Key Challenges Addressed:**  
- High energy costs due to inefficient appliance usage.  
- Lack of real-time insights into energy patterns.  
- Manual scheduling of home appliances leading to wasted energy.  

---

## 🌍 Context & Target Users
**Context:**  
- Deployed in residential homes with IoT-enabled devices (e.g., smart thermostats, lights).  
- Integrates with cloud analytics for dynamic pricing adjustments.  

**Target Users:**  
- Homeowners seeking cost savings.  
- Utility companies for load balancing.  
- Environmental advocates promoting sustainable energy use.  

---

## 🚀 Project Goals
1. **Real-Time Monitoring:**  
   - Track live energy usage per appliance via a user portal.  
2. **Automated Controls:**  
   - Adjust HVAC and lighting based on schedules/energy tariffs.  
3. **Data-Driven Insights:**  
   - Generate reports on consumption trends and savings.  
4. **Alerts:**  
   - Notify users of abnormal usage or peak-hour spikes.  

---

## 📊 Core Entities (Phase I Preview)
| Entity               | Description                                  |
|----------------------|----------------------------------------------|
| `User`               | Homeowners managing devices and reports.     |
| `Home`               | Physical location with IoT sensors.          |
| `Appliance`          | Smart devices (e.g., fridge, AC).            |
| `EnergyUsageRecord`  | Timestamped energy consumption logs.         |

**Relationships:**  
- **User → Homes** (1:N)  
- **Home → Appliances** (1:N)  
- **Appliance → EnergyUsageRecord** (1:N)  
```  


```  
erDiagram
    USER ||--o{ HOME : "Manages"
    HOME ||--o{ APPLIANCE : "Contains"
    APPLIANCE ||--o{ ENERGY_USAGE : "Generates"

    USER {
        int user_id PK
        varchar name
        varchar email
        varchar phone
    }

    HOME {
        int home_id PK
        varchar address
        decimal sq_footage
    }

    APPLIANCE {
        int appliance_id PK
        varchar type
        decimal wattage
    }

    ENERGY_USAGE {
        int record_id PK
        timestamp datetime
        decimal kWh_consumed
    }
  ```  
   

