# Multi File Upload Editor

![Main Screen](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/main-screen.png)

changelogs available here: <https://github.com/error311/multi-file-upload-editor-docker/>

Multi File Upload Editor is a lightweight, secure web application for uploading, editing, and managing files. It’s built with an Apache/PHP backend and a modern JavaScript frontend (ES6 modules) to provide a responsive, dynamic file management interface. The application is ideal for scenarios like document management, image galleries, firmware file hosting, or any situation where multiple files need to be uploaded and organized through a web interface.

---

## Features

- **Multiple File Uploads with Progress:**
  - Users can select and upload multiple files at once. Each file upload shows an individual progress bar with percentage and upload speed, and image files display a small thumbnail preview (default icons for other file types).
- **Built-in File Editing & Renaming:**
  - Text-based files (e.g., .txt, .html, .js) can be opened and edited in a modal window without leaving the page. The editor modal is resizable for convenience. Any file can be renamed in-place via a dedicated “Rename” action, without needing to open or re-upload it.
- **Batch Operations (Delete/Copy/Move):**
  - Users can select one or many files and perform batch actions: delete files, copy them to another folder, or move them to a different folder. Action buttons for these operations remain visible whenever files exist and become enabled only when one or more files are selected.
- **Folder Management:**
  - Supports organizing files into folders and subfolders. Users can create new folders, rename existing folders, or delete folders. A dynamic folder tree in the UI allows navigation through directories and updates in real-time to reflect changes after any create, rename, or delete action.
- **Sorting & Pagination:**
  - The file list can be sorted by name, last modified date, upload date, size, or uploader. Dates are reliably sortable thanks to a custom date parser. For easier browsing, the interface supports pagination with selectable page sizes (10, 20, 50, or 100 items per page) and navigation controls (“Prev”, “Next”, specific page numbers).
- **User Authentication & Management:**
  - Secure, session-based authentication protects the editor. An admin user can add or remove users through the interface. Passwords are hashed using PHP’s password_hash() for security, and session checks prevent unauthorized access to backend endpoints.
- **Responsive, Dynamic UI:**
  - The interface is mobile-friendly and adjusts to different screen sizes (hiding non-critical columns on small devices to avoid clutter). Updates to the file list, folder tree, and upload progress happen asynchronously (via Fetch API and XMLHttpRequest), so the page never needs to fully reload. Users receive immediate feedback through toast notifications and modal dialogs for actions like confirmations and error messages, creating a smooth user experience.

---

## Screenshots

  ![Login](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/login-page.png)  
  ![Login](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/edit-larger-window.png)  
  ![Login](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/move-selected.png)  
  ![Login](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/create-folder.png)  
  ![Login](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/delete-folder.png)  
  ![Login](https://raw.githubusercontent.com/error311/multi-file-upload-editor/refs/heads/master/resources/create-user.png)  

based off of:
<https://github.com/sensboston/uploader>

## Prerequisites

- Apache2, configured, up and running
- PHP 8.1 or higher
- Required PHP extensions: `php-json`, `php-curl`  
