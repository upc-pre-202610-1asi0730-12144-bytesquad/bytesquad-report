## Domain-Driven Software Architecture

### Design-Level Event Storming
![Design-Level Event Storming](../assets/Event%20Storming.png)

### Aggregates
![aggregates.png](../assets/aggregates.png)

# System Architecture (C4 Model)

## Level 1: System Context
El diagrama de contexto proporciona una vista de alto nivel del sistema, mostrando cómo los diferentes tipos de usuarios (entrenadores, administradores, clientes) y los sistemas externos interactúan con la plataforma.

![System Context](../docs/c4/01_SystemContext.png)

---

## Level 2: Containers
Esta sección detalla las aplicaciones y bases de datos que componen el sistema, destacando la separación entre el Frontend (aplicaciones web/móviles) y el Backend (APIs y microservicios).

### General Container View
![Containers](../docs/c4/02_Container.png)

### Bounded Contexts
Para facilitar la comprensión, los contenedores se agrupan en contextos delimitados según el dominio del negocio:
* **Frontend Bounded Contexts:**
  ![Frontend BCs](../docs/c4/02b_FrontendBCs.png)
* **Backend Bounded Contexts:**
  ![Backend BCs](../docs/c4/02c_BackendBCs.png)

---

## Level 3: Components
A continuación, se detallan los componentes internos de cada contenedor, organizados por módulo o dominio de negocio.

### 1. Identity & Access Management (IAM)
Gestiona el registro, inicio de sesión, roles y permisos de los usuarios dentro de la plataforma.
* **Backend:** ![IAM BE](../docs/c4-backend/04a_IAM_BE.png)
* **Frontend:** ![Auth FE](../docs/c4-frontend/03k_Auth_FE.png)

### 2. Membership
Módulo encargado de gestionar los planes de suscripción, estados de las membresías y pagos.
* **Backend:** ![Membership BE](../docs/c4-backend/04k_Membership_BE.png)
* **Frontend:** ![Membership FE](../docs/c4-frontend/03m_Membership_FE.png)

### 3. Profiles & Gym
Gestión de la información personal de los usuarios y la configuración de las sucursales del gimnasio.
* **Backend (Profiles):** ![Profiles BE](../docs/c4-backend/04b_Profiles_BE.png)
* **Backend (Gym):** ![Gym BE](../docs/c4-backend/04c_Gym_BE.png)

### 4. Reservation
Permite a los usuarios programar clases, reservar equipos y gestionar la capacidad del gimnasio.
* **Backend:** ![Reservation BE](../docs/c4-backend/04e_Reservation_BE.png)
* **Frontend:** ![Reservation FE](../docs/c4-frontend/03j_Reservation_FE.png)

### 5. Routines
Asignación, creación y seguimiento de rutinas de ejercicio personalizadas para los clientes.
* **Backend:** ![Routines BE](../docs/c4-backend/04d_Routine_BE.png)
* **Frontend:** ![Routines FE](../docs/c4-frontend/03l_Routines_FE.png)

### 6. Equipment & IoT Sensor Ingestion
Gestión del inventario de máquinas y recepción de datos en tiempo real provenientes de los sensores instalados en el equipo.
* **Frontend (Equipment):** ![Equipment FE](../docs/c4-frontend/03b_Equipment_FE.png)
* **Frontend (IoT):** ![IoT FE](../docs/c4-frontend/03c_IoT_FE.png)

### 7. Monitoring & Alerts
Supervisión del estado de las máquinas y generación de notificaciones o alertas ante fallas o desgastes detectados por IoT.
* **Backend:** ![Monitoring BE](../docs/c4-backend/04j_Monitoring_BE.png)
* **Frontend (Monitoring):** ![Monitoring FE](../docs/c4-frontend/03d_Monitoring_FE.png)
* **Frontend (Alerts):** ![Alerts FE](../docs/c4-frontend/03e_Alerts_FE.png)

### 8. Maintenance
Gestión de tickets, registro de fallas y programación de reparaciones para el equipo técnico.
* **Backend:** ![Maintenance BE](../docs/c4-backend/04f_Maintenance_BE.png)
* **Frontend:** ![Maintenance FE](../docs/c4-frontend/03h_Maintenance_FE.png)

### 9. Analytics & Dashboards
Procesamiento de datos históricos y visualización de métricas de uso y estado financiero para administradores.
* **Backend:** ![Analytics BE](../docs/c4-backend/04i_Analytics_BE.png)
* **Frontend (Analytics):** ![Analytics FE](../docs/c4-frontend/03f_Analytics_FE.png)
* **Frontend (Dashboard):** ![Dashboard FE](../docs/c4-frontend/03g_Dashboard_FE.png)

### 10. Shared & Configuration
Utilidades, configuraciones globales y componentes base reutilizados en todo el sistema.
* **Backend (Shared):** ![Shared BE](../docs/c4-backend/04h_Shared_BE.png)
* **Frontend (Shared):** ![Shared FE](../docs/c4-frontend/03a_Shared_FE.png)
* **Frontend (Configuration):** ![Config FE](../docs/c4-frontend/03i_Configuration_FE.png)

---

## Level 4: Dynamic Views (Aggregate Flows)
Esta sección contiene los diagramas dinámicos que muestran cómo interactúan los objetos y componentes a lo largo del tiempo para cumplir con los flujos de trabajo específicos de cada agregado (*aggregate*) del dominio.

### 1. IAM & User Flow
Flujo secuencial de las interacciones de los usuarios durante los procesos de autenticación y autorización.
![IAM User Flow](../docs/c4-aggregate/05a_IAM_User_flow.png)

### 2. Profiles & Gym Flows
Ciclo de vida y secuencia de pasos para la gestión de datos de usuario y configuración de los gimnasios.
* **Profiles:** ![Profiles Flow](../docs/c4-aggregate/05b_Profiles_flow.png)
* **Gym:** ![Gym Flow](../docs/c4-aggregate/05c_Gym_flow.png)

### 3. Equipment & Routine Flows
Interacciones dinámicas relacionadas con el inventario de máquinas y el flujo de asignación/seguimiento de rutinas.
* **Equipment:** ![Equipment Flow](../docs/c4-aggregate/05d_Equipment_flow.png)
* **Routine:** ![Routine Flow](../docs/c4-aggregate/05e_Routine_flow.png)

### 4. Reservation & Requests Flows
Secuencia detallada desde que un cliente solicita una reserva hasta que el sistema la procesa, valida el aforo y la confirma.
* **Reservation General:** ![Reservation Flow](../docs/c4-aggregate/05f_Reservation_flow.png)
* **Reservation Request:** ![Reservation Request Flow](../docs/c4-aggregate/05g_ReservationRequest_flow.png)

### 5. Maintenance & Technical Ticket Flows
Flujos dinámicos del ciclo de vida del mantenimiento, abarcando desde la detección de fallas, la creación de tickets de soporte técnico, la asignación de trabajos, hasta el cierre del registro en la bitácora histórica.
* **Maintenance General:** ![Maintenance Flow](../docs/c4-aggregate/05h_Maintenance_flow.png)
* **Maintenance Job:** ![Maintenance Job Flow](../docs/c4-aggregate/05i_MaintenanceJob_flow.png)
* **Technical Ticket:** ![Technical Ticket Flow](../docs/c4-aggregate/05j_TechnicalTicket_flow.png)
* **Maintenance Log:** ![Maintenance Log Flow](../docs/c4-aggregate/05k_MaintenanceLog_flow.png)

## 4.7. Software Object-Oriented Design
### 4.7.1. Class Diagrams Frontend

#### 4.7.1.1. Analytics Diagram Class
![diagram0](../assets/class-diagrams/frontend-diagram-class/analytics-diagram-class.png)
#### 4.7.1.2. Gym Diagram Class
![diagram1](../assets/class-diagrams/frontend-diagram-class/gym-diagram-class.png)
#### 4.7.1.3. Manteinance Diagram Class
![diagram2](../assets/class-diagrams/frontend-diagram-class/manteinance-diagram-class.png)
#### 4.7.1.4. Profiles Diagram Class
![diagram3](../assets/class-diagrams/frontend-diagram-class/profiles-diagram-class.png)
#### 4.7.1.5. Reservation Diagram Class
![diagram4](../assets/class-diagrams/frontend-diagram-class/booking-diagram-class.png)
#### 4.7.1.6. Routine Diagram Class
![diagram5](../assets/class-diagrams/frontend-diagram-class/routines-diagram-class.png)
#### 4.7.1.7. Dashboard Diagram Class
![diagram6](../assets/class-diagrams/frontend-diagram-class/dashboard-diagram-class.png)
#### 4.7.1.8. Monitoring Diagram Class
![diagram7](../assets/class-diagrams/frontend-diagram-class/monitoring-diagram-class.png)
#### 4.7.1.9. Alerts Diagram Class
![diagram8](../assets/class-diagrams/frontend-diagram-class/alerts-diagram-class.png)
#### 4.7.1.10. Financial Diagram Class
![diagram9](../assets/class-diagrams/frontend-diagram-class/financial-diagram-class.png)
#### 4.7.1.11. Configuration Diagram Class
![diagram10](../assets/class-diagrams/frontend-diagram-class/configuration-diagram-class.png)
#### 4.7.1.12. Shared Diagram Class
![diagram11](../assets/class-diagrams/frontend-diagram-class/app-diagram-class.png)
#### 4.7.1.13. IAM Diagram Class
![diagram12](../assets/class-diagrams/frontend-diagram-class/iam-diagram-class.png)


### 4.7.2. Class Diagrams Backend 

#### 4.7.2.1. Analytics Diagram Class
![diagram0](../assets/class-diagrams/backend-diagrams-class/analytics-diagram-class.png)
#### 4.7.2.2. Gym Diagram Class
![diagram2](../assets/class-diagrams//backend-diagrams-class/gym-diagram-class.png)

#### 4.7.2.3. Manteinance Diagram Class
![diagram1](../assets/class-diagrams/backend-diagrams-class/manteinance-diagram-class.png)

#### 4.7.2.4. Membership Diagram Class
![diagram2](../assets/class-diagrams/backend-diagrams-class/membership-diagram-class.png)

#### 4.7.2.5. Reservation Diagram Class
![diagram3](../assets/class-diagrams/backend-diagrams-class/reservation-diagram-class.png)


#### 4.7.2.6. Dashboard Diagram Class
![diagram4](../assets/class-diagrams/frontend-diagram-class/dashboard-diagram-class.png)

#### 4.7.2.7. IOT Diagram Class
![diagram5](../assets/class-diagrams/backend-diagrams-class/iot-diagram-class.png)

#### 4.7.2.8. Monitoring Diagram Class
![diagram6](../assets/class-diagrams/backend-diagrams-class/monitoring-diagram-class.png)

#### 4.7.2.9. Shared Diagram Class
![diagram7](../assets/class-diagrams/backend-diagrams-class/shared-diagram-class.png)

#### 4.7.2.10. IAM Diagram Class
![diagram8](../assets/class-diagrams/backend-diagrams-class/iam-diagram-class.png)


#### 4.7.2.10. EventFlow Diagram Class
![diagram9](../assets/class-diagrams/backend-diagrams-class/eventfloe-backend.png)

## 4.8. Database Design.
### 4.8.1. Database Diagrams
<div align= "center">
  <align>
    <img src="../assets/diagrama-base-datos/ERD.PNG" alt="bounded" width="500"/>
  </div> <br>