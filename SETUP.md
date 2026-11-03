# Duplicate File Finder - Setup & Installation

**Version:** 0.2.0

---

## About

Duplicate File Finder is a Python desktop application designed to locate duplicate files using SHA-256 hashing.

It provides a graphical interface for scanning folders, reviewing detected duplicates, and viewing image information.

## Requirements

- Python 3
- Pillow (PIL)
- Tkinter
- Windows recommended

## Installation

### Step 1 - Install Python

Download Python 3:

https://www.python.org/downloads/

During installation on Windows, enable:

- Add Python to PATH

Verify the installation:

```bash
python --version
```

### Step 2 - Install Dependencies

Open Command Prompt and run:

```bash
python -m pip install Pillow
```

Pillow is used for loading, displaying, and resizing images.

### Step 3 - Verify Tkinter

Tkinter provides the application's graphical interface.

It is normally included with standard Python installations.

To verify it works, run:

```bash
python -m tkinter
```

A small test window should appear.

### Step 4 - Download the Project

1. Open the GitHub repository.
2. Select the green Code button.
3. Select Download ZIP.
4. Extract the downloaded ZIP file.
5. Locate the Python script.

## Running the Application

Open Command Prompt in the project directory.

Run:

```bash
python duplicate_file_finder.py
```

Replace the filename if your Python script uses a different name.

The application window should open automatically.

## Using the Application

### Select Folder

Click **Select Folder** to choose a directory to scan.

The application recursively searches the selected directory and its subdirectories.

Files are compared using SHA-256 hashes to identify matching contents.

### Detail View

The default view displays detected duplicate entries in a table.

### Tile View

Click **Toggle View** to switch to the thumbnail-based interface.

This view is intended for browsing image duplicates.

### Image Preview

The application includes a preview window intended to display the original and duplicate images side by side.

### Delete Selected

The application includes a button intended to delete selected duplicate files.

**Important:** This function has a known file-path indexing issue in this version. Do not rely on it until corrected.

### New Folder & Move

This option is intended to move selected duplicate files into a folder named:

```text
Duplicates
```

**Important:** This function also has a known file-path indexing issue in this version. Do not rely on it until corrected.

## Duplicate Detection

The application uses SHA-256 hashing to compare file contents.

Each file is read in chunks and processed to generate a hash.

Files with matching hashes are identified as duplicates, even if they have different filenames.

## Duplicate Logging

After a scan, the application generates:

```text
duplicate_log.txt
```

The log contains detected duplicate paths and their corresponding original file paths.

The log is created in the application's current working directory and overwritten by subsequent scans.

## Supported Image Formats

The application recognizes the following image formats for file information and previews:

- PNG
- JPG
- JPEG
- BMP
- GIF

Tile View additionally recognizes WEBP files.

## Troubleshooting

### Problem: No module named PIL

Install Pillow:

```bash
python -m pip install Pillow
```

### Problem: No module named tkinter

On Windows, reinstall Python with Tcl/Tk support enabled.

On Linux, install the appropriate Tkinter package through your distribution's package manager.

### Problem: No duplicates found

Make sure the selected directory contains files to scan.

Remember that files must have identical contents to be considered duplicates.

### Problem: Image preview fails

Make sure both files exist and that Pillow supports their image formats.

### Problem: Application cannot access certain files

Check folder permissions and make sure the application has permission to read the selected directory.

## Known Limitations

- Tile View currently has an initialization issue.
- Image preview resizing requires correction.
- Delete Selected has incorrect file-path indexing.
- New Folder & Move has incorrect file-path indexing.
- Compare & Rename is not implemented.
- File metadata is retrieved by helper functions but is not fully integrated into the results table.

## Safety Notice

This is an early development release.

Do not rely on the deletion or moving functions until their file-path handling issues have been fixed and tested.

Always maintain backups before performing file-management operations.

## Author

KeanuBC

## License

This project is distributed under the MIT License.

See the included LICENSE file for details.

---

Thank you for checking out Duplicate File Finder!
