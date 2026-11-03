# Duplicate File Finder

A Python desktop application for finding duplicate files using SHA-256 hashing.

Scan folders, identify files with identical contents, and review potential duplicates through a graphical interface.

## Features

- **Duplicate Detection:** Finds files with identical contents using SHA-256 hashes.
- **Recursive Scanning:** Scans selected folders and their subdirectories.
- **Detail View:** Displays detected duplicates in a table.
- **Tile View:** Provides a thumbnail-based interface for image duplicates.
- **Image Preview:** Includes side-by-side previews of original and duplicate images.
- **Duplicate Logging:** Automatically generates a text log of detected duplicates.
- **File Management:** Includes options for deleting or moving selected duplicates.
- **File Information:** Retrieves file size, modification date, file type, image dimensions, and color mode.
- **Graphical Interface:** Built with Python Tkinter.

## Requirements

- Python 3
- Pillow
- Tkinter

## Installation

Install the required Python dependency:

```bash
python -m pip install Pillow
```

Tkinter is normally included with standard Python installations.

Download or clone this repository from GitHub.

For detailed installation instructions, see [SETUP.md](SETUP.md).

## Usage

Launch the application:

```bash
python duplicate_file_finder.py
```

Replace the filename with the actual script filename if different.

### Main Interface

**Select Folder**
- Opens a folder selection window.
- Recursively scans the selected directory.
- Searches for files with matching SHA-256 hashes.

**Delete Selected**
- Intended to delete selected duplicate files.

**New Folder & Move**
- Intended to move selected duplicates into a dedicated `Duplicates` folder.

**Toggle View**
- Switches between Detail View and Tile View.

### Image Preview

The application includes functionality for displaying original and duplicate images side by side.

### Duplicate Log

After scanning, the application generates:

`duplicate_log.txt`

The log records detected duplicate paths and their corresponding original file paths.

## Supported Image Formats

- PNG
- JPG
- JPEG
- BMP
- GIF
- WEBP (Tile View)

## Important Notes

- Duplicate detection is based on file contents, not filenames.
- Files with matching SHA-256 hashes are considered duplicates.
- Tile View is intended for browsing image duplicates.
- Compare & Rename is currently under development.
- Some file-management and preview functionality requires additional fixes.

**Warning:** This is an early development release. Do not rely on the delete or move functions until their file-path handling issues have been corrected.

Always keep backups of important files.

## Project Status

**Current Version:** 0.2.0

This project is an early development release. Some features are incomplete or require additional work.

## License

This project is licensed under the [MIT License](LICENSE).
