# README: Music Collection Manager (MCM)

---

## 📌 Project Overview

**Music Collection Manager (MCM)** is an offline desktop application built for DJs, music producers, and enthusiasts to efficiently organize, search, and analyze large personal music libraries.

Unlike streaming apps, MCM provides advanced offline tools such as detailed metadata entry, similarity analysis, and intelligent filtering — ideal for professional and live settings.

---

## 🎯 Core Objectives

- Build an intuitive app to manage local music libraries
- Provide advanced search/filter functionality with metadata
- Implement BPM, key, and mood-based song matching
- Allow customizable playlist creation
- Operate entirely offline with data export/import features

---

## 🛠️ Tools & Technologies Used

- **Backend Language**: Python  
- **Database**: SQL (PostgreSQL/MySQL with ERD & schema design)  
- **Interface Design**: Wireframes, mood boards, navigation diagrams  
- **GUI Framework**: Tkinter (or another Python-based GUI tool)  
- **Data Handling**: SQLite/CSV integration for local storage  
- **ERD Design Tool**: LucidChart / dbdiagram.io  
- **Wireframing Tools**: Figma / Balsamiq / Canva  
- **Markdown & Documentation**: VS Code / Obsidian / Typora

---

## 🧱 Key Components

### 1. ERD & Database Schema
- Tables for: `Songs`, `Artists`, `Albums`, `Playlists`, `Genres`, `Tags`
- One-to-many and many-to-many relationships
- Normalized schema with indexes for fast queries

### 2. SQL Scripts
- Table creation scripts
- Sample inserts and bulk data loading
- Stored procedures for advanced filters (e.g., songs by BPM + key)
- Backup/restore procedures

### 3. Wireframes & Interface Design
- Home screen layout with playlist and filter panels
- Add/Edit Track screen
- Playlist builder interface
- Dark/Light mode toggle
- Drag-and-drop support for songs in playlists

### 4. Navigational Diagrams
- User flow from launching app → editing track → building playlist
- Diagrams include error handling and user feedback loops

### 5. Mood Boards
- Aesthetic inspiration: clean, modern, tech + analog DJ feel
- Dark mode primary with vibrant accent colors
- Font/typography: readable, minimal

---

## 🔍 Main Features

### 🎶 Music Management
- Add/edit/delete songs, albums, and artists
- Assign detailed metadata: Title, Artist, Album, Genre, Year, BPM, Key, Tags

### 🔎 Advanced Search & Filters
- Multi-criteria filtering (e.g., genre + BPM range + tag)
- Smart search suggestions
- Cross-genre discovery tools

### 🔁 Similar Song Matching
- Match by BPM and musical key
- Filter by energy, vocal tone, instrumentation
- Recommend mixable tracks

### 🗃️ Playlists & Tagging
- Build dynamic and static playlists
- Tag system for moods, events, or performance themes
- View by tag cloud or timeline

### 🔐 Data & Backup
- Full offline mode
- Backup and restore music library
- Export metadata to CSV or SQL

---

## 🚀 What I Learned

### 💡 Technical Skills
- How to design normalized databases and create ERDs
- Writing efficient SQL queries, joins, and stored procedures
- Building GUI apps using Python
- Structuring user-friendly interfaces based on UX principles

### 🧠 Design & UX
- Creating wireframes and mood boards from scratch
- Mapping user journeys and designing accessible interfaces
- Balancing simplicity with power in feature design

### 🔍 Problem Solving
- Translating complex music metadata into usable database structures
- Creating efficient filters that don’t overwhelm users
- Managing local app state without a cloud backend

---

## 📂 Project Files & Structure

```bash
/music-collection-manager/
├── main.py
├── database/
│   ├── schema.sql
│   ├── sample_data.sql
│   └── backup_restore.sql
├── assets/
│   ├── wireframes/
│   ├── moodboards/
│   └── diagrams/
├── ui/
│   ├── add_song.py
│   ├── playlist_builder.py
│   └── dashboard.py
├── README.md
└── requirements.txt
