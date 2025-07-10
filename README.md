# Music Catalogue Design

A complete system design and prototype for managing and exploring music catalogs based on **genre, mood, BPM, and region**. Built with DJs, producers, and music explorers in mind, this project combines relational database architecture, wireframing, and search/filter system logic into a cohesive offline-ready platform.

Unlike streaming services, this design emphasizes **metadata precision**, **offline control**, and **smart discovery tools** for professionals working with personal music libraries.

Developed for the *Application Programming* course, this project includes an **ERD**, **normalized schema**, **SQL scripts**, **interface wireframes**, and system flow documentation to demonstrate scalable system design and practical backend engineering.

---

## Purpose

In a growing world of digital music, there’s a clear need for tools that enable **offline-first, metadata-driven music organization**. DJs and producers often work with massive personal libraries that require:

- Clean, flexible database structures
- Advanced discovery and filtering tools
- Region/mood/BPM-aware sorting for set building and inspiration
- Tools that don't depend on internet access or streaming services

This project simulates the backend system of such a platform — combining application programming, systems design, and UX wireframing into one cohesive artifact.

---

## Core Features

### Database Design
- Fully normalized relational schema in 3NF
- Entity Relationship Diagram (ERD) designed in Lucidchart
- Many-to-many link tables for genres, moods, and tags
- Indexed for efficient lookup and filtering

### SQL Functionality
- SQL scripts for table creation, test inserts, and advanced queries
- Stored procedures for mood + BPM matching and key similarity
- Backup and restore logic
- Multi-criteria filter queries (e.g., BPM + region + genre)

### Metadata Management
- Support for detailed metadata: title, artist, album, genre, year, BPM, key, tags, region
- Region table with continent → country mapping
- Tag system for moods, events, and themes

### UI & Experience Design
- Wireframes for desktop app layout: filterable library, playlist builder, edit screens
- Mood boards for visual consistency and aesthetic design
- Navigation diagrams for end-to-end user flow

---

##  System Artifacts

![Entity Relationship Diagram](ERD%20Final.png)
- ![Wireframe UI](./images/wireframe-ui.png)
- ![User Flow](./images/user-flow-diagram.png)

---

## What I Learned

### Technical Skills
- Designing normalized SQL databases with complex relationships
- Writing joins and stored procedures to simulate real-world discovery tools
- Working with SQLite and CSV for local storage
- Implementing application logic through SQL alone, without a full frontend

### UX & Product Thinking
- Creating wireframes and mood boards aligned with DJ/producer workflows
- Mapping out intuitive user journeys with actionable navigation states
- Balancing technical depth with user accessibility

### Problem Solving
- Translating musical properties (e.g., mood, BPM, key) into relational models
- Designing filters that feel powerful but stay performant
- **Overcoming SQL learning curve**: one major challenge was getting used to JOIN logic — particularly distinguishing between INNER, LEFT, and OUTER joins, and debugging missing or mismatched records

---

## Tech Stack

| Layer              | Technology           |
|-------------------|----------------------|
| Backend Language   | Python (for future expansion) |
| Database           | SQL (PostgreSQL / MySQL / SQLite) |
| Storage Format     | CSV (import/export support) |
| Design Tools       | Lucidchart, Balsamiq, Figma |
| Data Interaction   | SQL scripts, stored procedures |
| Interface Design   | Wireframes, Mood Boards |

---

## Challenges Faced

- Designing **multi-tag systems** for mood and genre without losing performance
- Understanding **complex JOIN logic** and how to filter across multiple criteria
- Creating a discovery-focused system without relying on frontend interactivity
- Balancing normalization with usability for actual filtering and playlist creation

---

## Future Improvements

- Build a **Streamlit** or **desktop GUI** app to interact with the schema
- Connect to live metadata APIs (Spotify, Last.fm, MusicBrainz)
- Add full-text search (e.g., lyrics, descriptions)
- ML-based recommendation features (clustering by mood, tempo, energy)
- Creative UX additions: waveform visualization, color-coded key indicators
- Smarter playlist creation via drag-and-drop and tag suggestions
