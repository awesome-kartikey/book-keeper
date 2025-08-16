# Frequently Asked Questions (FAQ)

Here are answers to some common questions about the Awesome Kartikey Book Keeper project.

**Q1: How are the bookmarks stored? Are they secure?**

Bookmarks are stored directly in your web browser's **Local Storage**. This is a client-side storage mechanism. Data stored here is specific to the browser and the domain (`file://` path or the web server domain if hosted). It's reasonably secure for non-sensitive data like bookmarks on your personal machine, but it's not encrypted and could be accessed if someone gains access to your browser profile or if the site hosting the app has security vulnerabilities (like XSS).

**Q2: Is there a limit to how many bookmarks I can save?**

Yes, there is a limit imposed by the browser's implementation of Local Storage. This limit is typically **5-10MB per domain**. While this is a lot of text data, it means you can store thousands of bookmarks, but it's not infinite.

**Q3: Will my bookmarks sync across different browsers or devices?**

**No.** Since the bookmarks are stored in Local Storage, they are tied to the specific browser profile on the specific device where you added them. They will not automatically appear if you open the application on a different computer or in a different browser (e.g., switching from Chrome to Firefox).

**Q4: Why does the app need the full URL (e.g., `https://google.com`)?**

The application uses the full URL for two main purposes:

1.  **Navigation**: To correctly link to the website when you click the bookmark.
2.  **Favicon Fetching**: It uses the domain part of the URL to request the site's favicon from Google's favicon service (`https://s2.googleusercontent.com/s2/favicons?domain=URL`). This requires a valid domain name.

**Q5: The app sometimes adds `https://` to my URL. Why?**

If you enter a URL without specifying the protocol (`http://` or `https://`), the application defaults to adding `https://` before saving it. This is done for convenience and to promote secure connections, as most modern websites use HTTPS.

**Q6: How does the favicon (website icon) retrieval work?**

The application uses a public Google service. When you add a bookmark like `https://github.com`, the script generates an image source URL like `https://s2.googleusercontent.com/s2/favicons?domain=github.com`. Your browser then requests the icon from that Google URL. This means it relies on Google's service being available and having the favicon cached.

**Q7: What happens if I clear my browser's cache or data?**

If you clear your browser's data, specifically selecting "Cookies and other site data" or "Local Storage," **all your saved bookmarks will be permanently deleted**. Be careful when clearing browser data if you want to keep your bookmarks.

**Q8: Can I import bookmarks from my browser or export the saved bookmarks?**

Currently, **no**. This feature is not implemented in this version of the application. Bookmarks can only be added manually through the interface.

**Q9: Why did you choose Local Storage instead of another storage method?**

Local Storage was chosen for its simplicity and the fact that it allows the application to function entirely on the client-side without needing a backend server or database. It's well-suited for small-scale applications where data synchronization isn't a primary requirement.

**Q10: The application looks simple. Is it meant for production use?**

This application serves as a good example of fundamental web development concepts (HTML, CSS, JS, DOM manipulation, Local Storage). While functional, it lacks features like user accounts, synchronization, robust error handling, and advanced organization (folders/tags) typically found in production bookmarking tools. It's more of a portfolio piece or a learning project.
