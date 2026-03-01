
# SongStorage

## Project Description

SongStorage is a CLI (Command Line Interface) application for managing a local audio file library.  
The application provides organized storage of audio files inside a dedicated folder, along with persistent metadata stored in an SQLite database.

The main features of the application are:

- adding and deleting songs  
- selective metadata editing  
- searching using multiple criteria combined with logical AND  
- creating playlists (savelists)  
- audio playback using a third-party library  

---

## Required Installations

### Requirements

- Python 3.10 or newer  
- pip  

### Python Dependencies

- `pygame` (used for audio playback)

Install dependencies using:

```bash
pip install pygame
```

## How to Run the Application

The application is executed exclusively as a Python module, from the project root directory:

```bash
python -m cli.main <command> [options]
```

## Usage
Available commands:
```bash
  add        Add a new song
  delete     Delete a song by ID
  edit       Edit song metadata
  search     Search songs
  savelist   Create a playlist archive
  play       Play a song
  help       Show help
```
Use 'songstorage help <command>' for details.

### Add Command
```bash
Usage: songstorage add --file PATH --artist TEXT --title TEXT 
					[--release-date DATE] 
					[--tags TAGS] 
Note: Release date must be in YYYY-MM-DD format. Tags must be quoted and separated by commas.
```
### Edit Command
```bash
Usage: songstorage edit --id ID 
					[--artist TEXT] 
					[--title TEXT] 
					[--release-date DATE] 
					[--tags TAGS] 
Note: At least one field must be provided for update. Release date must be in YYYY-MM-DD format. Tags must be quoted and separated by commas.
```
### Delete Command
```bash
Usage: songstorage delete --id ID
```
### Search Command
```bash
Usage: songstorage search [--artist TEXT] 
						  [--title TEXT] 
						  [--format FORMAT] 
						  [--tags TAG]
```
### Savelist Command
```bash
Usage: songstorage savelist --output NAME 
						    [search filters...]
```
### Play Command
```bash
Usage: songstorage play --id ID
```
Note:
Values containing spaces must be quoted.
