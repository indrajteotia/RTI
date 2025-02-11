Current active and public Invidious Instance: https://inv.nadeko.net/

To know more about Invidious Instance or check other instances: https://docs.invidious.io/instances/

# YouTube Redirect to Invidious

This Chrome extension automatically redirects YouTube URLs from `youtu.be` and `www.youtube.com` domains to an Invidious instance, `invidious`. This can be useful for users who prefer to use Invidious for privacy reasons or to avoid YouTube's tracking and advertisements.

## Features

*   **Automatic Redirection:**  Seamlessly redirects `youtube` to `invidious`.
*   **Privacy-Focused:**  Utilizes Invidious, an open-source, privacy-respecting front-end for YouTube.
*   **Lightweight:**  Simple and efficient extension with minimal resource usage.

## Installation

There are two ways to install this extension:

**1. Load Unpacked (for development and testing):**

1.  Download or clone this repository to your local machine.
2.  Open Google Chrome or any other chromium browser.
3.  Go to `chrome://extensions/` in the address bar.
4.  Enable "Developer mode" in the top right corner of the page.
5.  Click "Load unpacked" in the top left corner.
6.  Browse to the repository folder you downloaded and select it.
7.  The extension should now be loaded and active in your Chrome browser.

**2. Packaged Extension (`.crx` file - for distribution):**

1.  **If you haven't already packaged the extension:**
    *   Follow steps 1-5 from "Load Unpacked" above to load the extension unpacked first.
    *   Go back to `chrome://extensions/`.
    *   Click "Pack extension" in the top left corner.
    *   In the "Extension root directory" field, browse to your repository folder.
    *   Leave the "Private key" field empty for the first time. Click "Pack extension".
    *   A `.crx` file will be created in the parent directory of your repository folder. Note the location of the `.crx` file and the generated `.pem` file (keep the `.pem` file safe for future updates!).

2.  **Install the `.crx` file:**
    *   Open Google Chrome.
    *   Go to `chrome://extensions/` in the address bar.
    *   Drag and drop the `.crx` file onto the `chrome://extensions/` page.
    *   Chrome may ask you to confirm the installation. Click "Add extension".

## Usage

Once installed, the extension works automatically in the background.

1.  Simply click on any YouTube link that uses the `youtu.be` or `www.youtube.com/watch?v` format.
2.  The extension will automatically redirect you to the same video on the `inv.nadeko.net` Invidious instance.

## Repository Contents

*   `manifest.json`:  The extension's manifest file, containing metadata, permissions, and background script declaration.
*   `rules.json`:  Contains the declarative Net Request rules that define the URL redirection logic.
*   `background.js`: (Currently empty, but included as declared in `manifest.json`). You can add background scripts here for more advanced functionality in the future.
*   `README.md`: This file, providing information about the extension.

## Important Notes

*   **Invidious Instance:** This extension currently redirects to `inv.nadeko.net`. You can easily change this to another Invidious instance by modifying the `rules.json` file and replacing `inv.nadeko.net` with your preferred instance URL. You can find a list of public Invidious instances [here](https://redirect.invidious.io/api/v1/instances.json). (Note: Link may be outdated, please search for "Invidious instances list" for the latest list).
*   **Permissions:** This extension requires the following permissions:
    *   `declarativeNetRequest`, `declarativeNetRequestFeedback`, `declarativeNetRequestWithHostAccess`: Necessary for efficient URL redirection.
    *   `host_permissions` for `https://yu.be/*` and `https://www.yy.com/*`:  Allows the extension to intercept requests to these domains.
*   **Privacy:** While Invidious is designed for privacy, always be aware of the specific instance you are using and its privacy policy.
*   **Future Enhancements:**  Possible future features could include:
    *   Options to customize the Invidious instance.
    *   Support for more YouTube URL formats.
    *   A browser action popup with settings.
