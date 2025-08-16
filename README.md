# Awesome Kartikey Book Keeper

A simple, clean web application to save and manage your website bookmarks locally in your browser.

![Book Keeper Screenshot](placeholder.png) _(Note: Replace placeholder.png with an actual screenshot if available)_

## Description

Awesome Kartikey Book Keeper provides a straightforward interface to add, view, and delete website bookmarks. It utilizes the browser's local storage to persist your saved links, making it a lightweight, client-only solution.

## Features

- **Add Bookmarks**: Easily save websites with a custom name and URL via a modal form.
- **View Bookmarks**: Displays saved bookmarks clearly, including the website's favicon.
- **Delete Bookmarks**: Remove bookmarks individually with a single click.
- **Local Persistence**: Bookmarks are saved in the browser's `localStorage`, remaining available across sessions.
- **URL Validation**: Basic check to ensure the entered URL is in a valid format.
- **Favicon Fetching**: Automatically fetches and displays favicons for saved bookmarks using a public service.
- **Responsive Design**: Basic responsiveness for usability on smaller screens.

## Tech Stack

- **HTML5**: Structure and content of the web page.
- **CSS3**: Styling, layout, and responsiveness. Uses CSS variables and a Google Font (Karla).
- **Vanilla JavaScript**: Application logic, DOM manipulation, event handling, and interaction with `localStorage`.
- **Font Awesome**: Icons for user interface elements.
- **Browser Local Storage**: Client-side storage mechanism for persisting bookmarks.

## Setup Instructions

This project is a client-side application and requires no special build steps or backend setup.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/awesome-kartikey/book-keeper.git
    cd book-keeper
    ```
2.  **Open the HTML file:**
    Simply open the `index.html` file in your web browser (e.g., Chrome, Firefox, Safari, Edge).

That's it! You can now start adding and managing your bookmarks.

## Usage

1.  **Adding a Bookmark**:
    - Click the "Add Bookmark" button at the top.
    - A modal window will appear.
    - Enter the "Website Name" and "Website URL" in the respective fields.
      - _Note_: If you don't include `http://` or `https://` in the URL, `https://` will be added automatically.
    - Click the "Save" button.
    - The modal will close, and your new bookmark will appear on the page.
2.  **Visiting a Bookmark**:
    - Click on the name of the bookmark. It will open in a new browser tab.
3.  **Deleting a Bookmark**:
    - Hover over the bookmark you wish to remove.
    - Click the 'x' icon (close icon) that appears in the top-right corner of the bookmark item.
    - The bookmark will be removed instantly.
