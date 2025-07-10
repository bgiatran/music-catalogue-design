# Music Catalogue Design

A complete system design and prototype for managing and exploring music catalogs based on **genre**, **mood**, **BPM**, and **region**. Built with DJs, producers, and music explorers in mind, this project blends relational database architecture, wireframing, and search/filter logic into a cohesive offline-ready platform.

Unlike streaming services, this tool emphasizes **metadata precision**, **offline control**, and **smart discovery workflows** for professionals working with large local music libraries.

Developed for the **Application Programming** course, this project demonstrates scalable system design, SQL programming, and interface-level UX thinking through:

- An ERD and normalized database schema
- SQL scripts for real-world functionality
- Wireframes, navigation diagrams, and mood boards for product design
- System architecture and flow documentation

---

## Purpose

In the ever-growing world of digital music, there’s a clear need for **offline-first**, **metadata-driven** music management tools. DJs and producers often manage massive local libraries that require:

- Clean, flexible database structures
- Advanced discovery and filtering tools
- Region/mood/BPM-aware sorting for set building and inspiration
- Tools that don’t rely on internet access or streaming services

This project simulates the backend and UI architecture of such a platform — combining application programming, systems design, and UX wireframing into a single cohesive artifact.

---

## Core Features

### Database Design
- Fully normalized relational schema (3NF)
- Designed using Lucidchart
- Many-to-many link tables for genres, moods, and tags
- Indexed for efficient lookup and filtering

### SQL Functionality
- Scripts for:
  - Table creation and test data inserts
  - Advanced multi-criteria filter queries (e.g., BPM + region + genre)
  - Stored procedures for mood and key matching
  - Backup and restore logic

### Metadata Management
- Track-level metadata: title, artist, album, genre, BPM, key, tags, year, region
- Region table includes continent → country relationships
- Tag system supports moods, events, themes

###  UI & Experience Design
- Wireframes for a desktop-first app layout
- Playlist builder and editable library views
- Mood boards to guide aesthetic design
- Navigation diagrams to capture end-to-end flow

---

## System Artifacts

### Entity Relationship Diagram (ERD)

The ERD defines the underlying structure of the system’s data. Key relationships include:
- `Artists`, `Albums`, and `Tracks`
- Many-to-many tagging through junction tables (e.g., `Track_Genres`, `Track_Moods`)
- Region mappings and mood-based filtering logic

![Entity Relationship Diagram](ERD%20Final.png)

> *Visualizing the relational structure of the music catalogue system.*

---

### Normalized Schema Diagram

This diagram illustrates how the raw ERD is transformed into a **normalized SQL schema** following 3NF principles. It includes:
- Final table structures
- Foreign key constraints
- Reference integrity across the database

![Normalized Schema](schema_diagram.png)

> *Final database schema reflecting normalized table design.*

---

### Navigation Diagram

This diagram maps out user flow and screen relationships, including:
- Library view
- Track/album detail pages
- Edit and filter panels
- Playlist creation screen

[View Full PDF: Navigation Diagram](NavDiagram_Final.pdf)

> *An overview of how users move through the app interface.*

---

### Wireframe Screens

Core wireframes include:
- Main library grid (sortable/filterable)
- Playlist builder screen
- Detailed metadata editor view

[View Full PDF: Wire Diagram](WireDiagram_Final.pdf)

> *Layout structure and component arrangement across core screens.*

---

### Mood Board

This visual board guided the aesthetic direction, emphasizing:
- Sleek dark-mode UI with clear hierarchy
- Inspiration from Spotify, Notion, and music visualizers
- Calm tones, rounded edges, and minimalist control panels

_*(Image Placeholder: Add your mood board image here once finalized)*_

---

### Test Plan & Sample Data Document

This document outlines how functionality was validated using sample datasets and test queries:

- Sample inserts for tracks, albums, and tags  
- Validations for foreign key constraints and multi-table queries  
- Test cases for filtering by BPM, region, and mood  

[View Test Plan Document](Test_Document.pdf)

> *Simulating real-world use cases with test data and edge conditions.*

---

### SQL Scripts

This folder includes SQL code written for this project:

- `schema.sql`: Table creation and schema definition  
- `test_data.sql`: Sample inserts for development  
- `queries.sql`: Discovery filters, mood matching, and utility joins  
- `procedures.sql`: Stored procedures for advanced logic  
- `backup_restore.sql`: Export/import templates for local use  

[View SQL Scripts Folder](sql/)

> *Core database logic driving the music discovery platform.*

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
