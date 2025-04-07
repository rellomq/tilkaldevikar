# Tilkaldevikar - Temporary Worker Scheduling System

## Overview

This project is a web-based system designed to manage the scheduling of temporary workers (vikars) for UngKolding. It aims to streamline the process of requesting temporary staff, assigning available workers, and tracking assignments.

## Features

- **Vikar Request:**  Leaders can submit requests for temporary workers, specifying the date, time, and duration of the assignment.
- **Automated Notification:** The system automatically sends SMS messages to available workers when a new request is submitted.
- **Worker Acceptance:**  Workers can accept or decline assignments via a unique link in the SMS message.
- **Daily Report:** A daily report is automatically emailed to leaders, summarizing the status of all assignments.
- **Admin Dashboard:**  An administrative dashboard allows authorized users to manage users, clubs, and workers.

## Technology Stack

- **Language:** PHP
- **Database:** MySQL
- **Web Server:** Apache
- **SMS API:** CPSMS (https://www.cpsms.dk/)

## Setup Instructions

1. **Clone the repository:** git clone [repository URL] (Replace [repository URL] with the URL of your GitHub repository)
2. **Install dependencies:**  (None yet, but you'll add this as you add dependencies)
3. **Configure the database:**

   - Create a MySQL database named vikarsystem.
   - Create a user with access to the database.
   - Update the database connection settings in includes/db_connect.php.

4. **Configure SMS API:**

   - Obtain your CPSMS username and password from Carsten.
   - Update the API credentials in includes/sms_config.php.

5. **Run the application:**  (Instructions will be added once the application is fully deployed.)

## Database Schema

- **Users:** BrugerId, Navn, Email, Mobilnummer, Password, ErAdmin
- **Clubs:** KlubId, Klubnavn, Adresse, Postnr, By
- **Vikarer:** VikarId, Navn, Email, Mobil, ErAktiv
- **Vikarbehov:** BehovId, KlubId, Dato, Tid, Varighed, Status, TildelingsVikarId, OprettetAf, OprettetTid
- **SMSLogs:** LogId, BehovId, VikarId, SendtTid, Status

## Contributing

Contributions are welcome! Please see the CONTRIBUTING.md file for guidelines.

## License

[Add license information here if you choose one]# tilkaldevikar
A system for managing temporary worker scheduling.
