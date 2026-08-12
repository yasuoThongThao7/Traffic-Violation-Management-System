# Traffic Violation Management System

A Traffic Violation Management System written in C# (.NET / ASP.NET Core). The application allows recording, tracking, and managing traffic violations, storing evidence (images/videos), and generating statistical reports.

---

## Table of Contents

- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Configuration](#configuration)  
- [Database & Migrations](#database--migrations)  
- [Running the Application](#running-the-application)  
- [Testing](#testing)  
- [Contributing](#contributing)  
- [License](#license)  
- [Contact](#contact)

---

## Features

- Record violation reports (timestamp, location, violation type).  
- Manage vehicle and violator information.  
- Upload and store evidence (images, videos).  
- Create penalty decisions and track processing status (new / in-progress / resolved).  
- Search, filter, and paginate violation lists.  
- Statistical reports by area, violation type, and time range.  
- Basic role-based access control: Admin, Officer, Viewer.  
- RESTful API endpoints for main operations (if the project is implemented as a Web API).

## Tech Stack

- Language: C#  
- Framework: ASP.NET Core / .NET 6+  
- ORM: Entity Framework Core (if used)  
- Database: SQL Server / PostgreSQL / SQLite (configurable)  
- Common libraries (if applicable): AutoMapper, Serilog, FluentValidation, JWT authentication

## Prerequisites

- .NET SDK 6.0 or 7.0  
- A compatible database (SQL Server, PostgreSQL, or SQLite)  
- (Optional) Docker & Docker Compose if the repo includes container support

## Installation

1. Clone the repository:
   git clone https://github.com/yasuoThongThao7/Traffic-Violation-Management-System.git
   cd Traffic-Violation-Management-System

2. Restore packages and build:
   dotnet restore
   dotnet build --configuration Release

(If the solution contains multiple projects, navigate to the web project folder before running the commands.)

## Configuration

- Edit `appsettings.json` or `appsettings.Development.json` to configure the connection string, JWT settings, file storage paths, and other environment variables.

Example connection string (SQL Server):
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=TrafficViolationDB;Trusted_Connection=True;"
}
