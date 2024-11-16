# Roblox VIP Automatic Shutdowner

A bookmarklet script to automatically shut down your Roblox VIP server at regular intervals. The script works by clicking the shutdown button in Roblox's private server interface.

## Features

- Automatically shuts down Roblox VIP servers at a user-defined interval.
- Easy to set up by creating a browser bookmark.
- Customizable interval to shutdown the server (default: 12 hours).

# Setup Instructions

## 1. Copy the following code snippet.
   
 ```javascript
javascript:(function() { const intervalInHours = 12; const intervalInMilliseconds = intervalInHours * 60 * 60 * 1000; function shutdownServer() { const menuButton = document.querySelector('.icon-more'); if (menuButton) { console.log("Three dots button found. Clicking..."); menuButton.click(); setTimeout(function() { const shutdownButton = document.querySelector('.rbx-private-server-shutdown'); if (shutdownButton) { console.log("Shutdown button found. Clicking..."); shutdownButton.click(); console.log('Server shutdown initiated!'); } else { console.log('Shutdown button not found!'); } }, 1000); } else { console.log('Three dots button not found!'); } } shutdownServer(); setInterval(shutdownServer, intervalInMilliseconds); })();
```

## In your browser, create a new bookmark:
- Right-click on the bookmarks bar and select Add Page or Add Bookmark.
- Name it something like "Roblox VIP Shutdowner".
- Paste the copied code into the URL field.

## Step 2: Use the Bookmarklet
- Go to your Roblox VIP server page
- Make Sure that the VIP server is visible
- Click the bookmark you created in your browser's bookmark bar.
- The script will automatically start and will shut down the server at the interval you set (default: every 12 hours).

## Customizing the Interval
You can customize the interval to shut down the server by modifying the intervalInHours variable in the script. Simply change the number of hours you want, save the bookmark again, and you’re good to go.

### Example
If you want the server to shut down every 6 hours, change the script to:
```js
const intervalInHours = 6; // Set the interval to 6 hours
```

## Troubleshooting
- No shutdown button found: Make sure you're on the correct page for your Roblox VIP server.
- Bookmarklet not working: Double-check that you've copied the entire script without any changes or missing parts.

## Contributing
If you'd like to contribute, feel free to fork the repository and submit a pull request with any improvements or bug fixes.


## Proper Format Code
If you think i have hidden a virus somewhere, heres the proper format, note that this does not work as its not correctly formatted for the Bookmark:
```js
javascript:(function() {
    
    const intervalInHours = 12; // Change this value to the desired interval in hours

    const intervalInMilliseconds = intervalInHours * 60 * 60 * 1000;

    function shutdownServer() {
        const menuButton = document.querySelector('.icon-more');
        if (menuButton) {
            console.log("Three dots button found. Clicking...");
            menuButton.click(); // Click the three dots button
            
            setTimeout(function() {
                const shutdownButton = document.querySelector('.rbx-private-server-shutdown');
                if (shutdownButton) {
                    console.log("Shutdown button found. Clicking...");
                    shutdownButton.click(); // Click the shutdown button
                    console.log('Server shutdown initiated!');
                } else {
                    console.log('Shutdown button not found!');
                }
            }, 1000); // 1-second delay before clicking the shutdown button
        } else {
            console.log('Three dots button not found!');
        }
    }

    // Initial shutdown
    shutdownServer();

    // Set interval to shutdown at the specified interval
    setInterval(shutdownServer, intervalInMilliseconds);
})();

```
