# Sound-Hub

Sound-Hub is a robust, multi-module audio streaming and music management platform designed similarly to Spotify. The system supports full CRUD operations for managing artists, bands, albums, and tracks, along with user-interactive features like custom playlist creation, social commenting, and reaction engagement. 

Originally built as an MVC application utilizing server-side templates, the project has evolved into a decoupled architecture featuring a dedicated REST module exposing production-ready APIs.

---

## 🚀 Key Features
* **User Ecosystem:** Custom authentication with secure roles (Admin, User) and automated email notifications.
* **Music Discovery & Cataloging:** Comprehensive relational management linking Songs to specific Artists, Bands, and Genres.
* **Social Engagement:** Real-time playlist curation, user profiles, interactive song/album comment threads, and reaction tracking.
* **Cloud Audio Streaming:** Direct audio streaming powered by distributed object storage buckets (AWS S3).

---

## 🛠️ Technical Stack & Dependencies

* **Core Platform:** Java 21 / Spring Boot
* **Build System:** Maven Multi-Module Architecture
* **Database & Persistence:** PostgreSQL, Spring Data JPA, Hibernate
* **Database Migrations:** Liquibase (Version-controlled XML schema change tracking)
* **Cloud Storage:** Amazon Web Services (AWS S3) for hosting and streaming `.mp3` assets
* **Security & Access Control:** Spring Security, JSON Web Tokens (JWT)
* **Frontend Components:** Thymeleaf, HTML5/CSS3 (Legacy MVC Layouts)

---

## 📂 Multi-Module Architecture

The project leverages a decoupled, clean-architecture directory layout to separate concerns and ensure maintainability:

```text
sound-hub-modular/
│
├── common/          # Shared domain models, configurations, and general utilities.
├── persistence/     # Data Layer: Entities, Spring Data JPA Repositories, and Liquibase logs.
├── app/             # Application core services, implementations, and legacy MVC Thymeleaf controllers.
└── rest/            # REST API Layer: Independent controllers, DTO configurations, and API endpoints.
