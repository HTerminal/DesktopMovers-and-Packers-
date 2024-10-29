# DesktopMovers-and-Packers-
Cleans your desktop


# File Organizer Script

This script organizes files in a directory by moving them into folders based on their file types. It categorizes files such as documents, images, videos, and code files into predefined folders for easy organization.

## Features

- Moves files based on their extension (e.g., `.pdf` to a `PDFs` folder, `.mp4` to a `Videos` folder).
- Creates destination folders if they do not exist.
- Overwrites existing files in the destination folder to avoid duplicates.

## Folder Map

The script uses a predefined map of file extensions and their corresponding folder names:

| File Extension | Folder Name    |
|----------------|----------------|
| `pdf`          | PDFs           |
| `jpg`, `jpeg`, `png` | Images   |
| `doc`, `docx`  | Documents      |
| `txt`          | Text Files     |
| `mp3`, `wav`   | Music          |
| `mp4`, `avi`, `mov` | Videos    |
| `xlsx`, `csv`  | Excel Files    |
| `zip`, `rar`   | Archives       |
| `py`           | Pythons        |
| `ino`          | Arduino        |
| `tflite`       | Models         |
| `sql`          | Database       |
| `apk`          | APK            |
| `html`, `php`, `ovn` | HTML     |
| `ppk`          | KEYs           |
| `sh`           | Codes          |

Feel free to customize the folder map in the script to include additional file types.

## Usage

1. **Download and Run the Script**:
    - Save the script in the directory where you want to organize files.
    - Run the script with Python:
      ```bash
      python organize_files.py
      ```
    - The script will organize files in the current working directory where the script is located.

2. **Optional**: Handling Unknown File Types
    - By default, files with unknown extensions are ignored. You can uncomment the section marked as "Optionally handle unknown file types" to move these files to an "Others" folder.

## Functions

### `create_and_move(file, folder_name)`
- **Purpose**: Creates the destination folder if it doesn’t exist and moves the file.
- **Parameters**:
  - `file`: The file to move.
  - `folder_name`: The destination folder based on the file type.

### `move_files_to_folders(directory)`
- **Purpose**: Scans the specified directory, checks each file’s extension, and moves it to the appropriate folder using `create_and_move`.

## Notes

- The script operates on files in the directory where it is run. If you want to organize files in a different directory, change `current_directory` to the desired path.
- If a file already exists in the destination folder, it will be replaced.

## Example

If the script is run in a folder containing:
