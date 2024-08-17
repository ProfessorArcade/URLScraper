<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Link Scraper</title>
    <style>
        :root {
            --background-color: #f4f4f4;
            --text-color: #333;
            --button-background: #007bff;
            --button-text: #fff;
            --box-background: #fff;
            --box-shadow: rgba(0, 0, 0, 0.1);
        }

        [data-theme="dark"] {
            --background-color: #1e1e1e;
            --text-color: #f4f4f4;
            --button-background: #555;
            --button-text: #fff;
            --box-background: #2c2c2c;
            --box-shadow: rgba(255, 255, 255, 0.1);
        }

        body {
            font-family: Arial, sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        h1 {
            color: var(--text-color);
        }

        #description {
            max-width: 800px;
            padding: 15px;
            background-color: var(--box-background);
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 20px;
            text-align: center;
            box-shadow: 0 2px 10px var(--box-shadow);
            transition: background-color 0.3s ease, box-shadow 0.3s ease;
        }

        #scrapeBtn {
            padding: 10px 20px;
            background-color: var(--button-background);
            color: var(--button-text);
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            margin-top: 10px;
            margin-bottom: 20px;
        }

        #scrapeBtn:hover {
            background-color: #0056b3;
        }

        #linksBoxContainer {
            position: relative;
            width: 90%;
            max-width: 800px;
            margin-bottom: 20px;
        }

        #linksBox {
            width: 100%;
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: var(--box-background);
            box-shadow: 0 2px 10px var(--box-shadow);
            min-height: 300px;
            color: var(--text-color);
            transition: background-color 0.3s ease, color 0.3s ease, box-shadow 0.3s ease;
        }

        #copyBtn {
            display: none;
            position: absolute;
            top: -30px;
            right: 10px;
            font-size: 12px;
            color: gray;
            background-color: transparent;
            border: none;
            cursor: pointer;
        }

        #demo {
            font-size: 16px;
            color: var(--text-color);
        }

        #urlInput {
            width: 80%;
            max-width: 600px;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-shadow: 0 1px 5px rgba(0, 0, 0, 0.1);
            color: var(--text-color);
            background-color: var(--box-background);
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        /* Dark Mode Toggle Button */
        #toggleThemeBtn {
            position: absolute;
            top: 10px;
            left: 10px;
            background: transparent;
            border: none;
            cursor: pointer;
        }

        /* Custom Sun Icon */
        .sun-icon {
            fill: var(--text-color);
        }

        /* Custom Moon Icon */
        .moon-icon {
            fill: var(--text-color);
        }

        /* GitHub Link Styling */
        #githubLink {
            position: absolute;
            bottom: 10px;
            left: 10px;
            font-size: 14px;
            color: var(--button-background);
            text-decoration: none;
        }

        #githubLink:hover {
            text-decoration: underline;
        }

    </style>
</head>
<body>
    <!-- Theme Toggle Button -->
    <button id="toggleThemeBtn">
        <svg id="themeIcon" class="sun-icon" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
            <!-- Sun Icon -->
            <circle cx="12" cy="12" r="5" stroke="currentColor" stroke-width="2" fill="none"></circle>
            <line x1="12" y1="2" x2="12" y2="4" stroke="currentColor" stroke-width="2"></line>
            <line x1="12" y1="20" x2="12" y2="22" stroke="currentColor" stroke-width="2"></line>
            <line x1="4.22" y1="4.22" x2="5.64" y2="5.64" stroke="currentColor" stroke-width="2"></line>
            <line x1="18.36" y1="18.36" x2="19.78" y2="19.78" stroke="currentColor" stroke-width="2"></line>
            <line x1="2" y1="12" x2="4" y2="12" stroke="currentColor" stroke-width="2"></line>
            <line x1="20" y1="12" x2="22" y2="12" stroke="currentColor" stroke-width="2"></line>
            <line x1="4.22" y1="19.78" x2="5.64" y2="18.36" stroke="currentColor" stroke-width="2"></line>
            <line x1="18.36" y1="5.64" x2="19.78" y2="4.22" stroke="currentColor" stroke-width="2"></line>
        </svg>
    </button>

    <h1>Link Scraper</h1>
    
    <div id="description">
        <p>Welcome to the Link Scraper! This tool allows you to extract all the links from a specified webpage. Simply enter the URL of the page you'd like to scrape, click the "Scrape Links" button, and the links will be displayed below.</p>
    </div>
    
    <input type="text" id="urlInput" placeholder="Enter a valid URL" />
    <button id="scrapeBtn">Scrape Links</button>

    <div id="linksBoxContainer">
        <button id="copyBtn">Copy links</button>
        <textarea id="linksBox" rows="20"></textarea>
    </div>

    <p id="demo"></p>

    <!-- GitHub Link -->
    <a href="https://github.com/your-repo" id="githubLink" target="_blank">GitHub</a>

    <script>
        let targetUrl;
        let links = [];

        // Function to remove duplicate links
        const removeDuplicates = (arr) => {
            arr.forEach(item => {
                const match = item.match(/https?:\/\/[^\s]+/);
                if (match) {
                    const url = match[0];
                    if (!links.includes(url)) {
                        links.push(url);
                    }
                }
            });
        };

        // Function to resolve relative URLs to absolute URLs
        const resolveURL = (base, relative) => {
            const baseEl = document.createElement('base');
            baseEl.href = base;
            const anchor = document.createElement('a');
            anchor.href = relative;
            return anchor.href;
        };

        // Function to fetch and parse links from the target URL
        const fetchLinks = async (url) => {
            try {
                        links = [];
                const response = await fetch(`https://api.allorigins.win/get?url=${encodeURIComponent(url)}`);
                const data = await response.json();
                const parser = new DOMParser();
                const doc = parser.parseFromString(data.contents, 'text/html');
                const linkElements = doc.querySelectorAll('a[href]');

                const urls = Array.from(linkElements).map(link => resolveURL(url, link.getAttribute('href')));
                removeDuplicates(urls);

                // Display links
                displayLinks();
            } catch (error) {
                console.error(error);
            }
        };

        // Function to validate and normalize the URL
        const isValidUrl = (url) => {
            // Add http or https if missing
            if (!url.match(/^https?:\/\//i)) {
                url = 'http://' + url;
            }
            try {
                const normalizedUrl = new URL(url);
                // Check for a valid hostname (e.g., "e" is not valid)
                if (!normalizedUrl.hostname.includes('.')) {
                    return false;
                }
                return normalizedUrl.href;
            } catch (e) {
                return false;
            }
        };

        // Function to display the links in the textarea and show the "Copy links" button
        const displayLinks = () => {
            const linksBox = document.getElementById('linksBox');
            const copyBtn = document.getElementById('copyBtn');
            linksBox.value = ''; // Clear the text box first
            document.getElementById("demo").innerHTML = `Here's your scraped links!`;
            links.forEach(url => {
                linksBox.value += `${url}\n`;
            });
            if (links.length > 0) {
                copyBtn.style.display = 'block'; // Show the "Copy links" button
            }
        };

        // Event listener for the "Scrape Links" button
        document.getElementById('scrapeBtn').addEventListener('click', () => {
            document.getElementById("demo").innerHTML = ``;
            targetUrl = document.getElementById('urlInput').value.trim();
            const validUrl = isValidUrl(targetUrl);
            if (!validUrl) {
                        linksBox.value = "";
                document.getElementById("demo").innerHTML = `Invalid Link`;
                return;
            }
            linksBox.value = ""; // Reset links array on each scrape
            fetchLinks(validUrl);
            document.getElementById("demo").innerHTML = `Scraping your links now... (This may take a while.)`;
        });

        // Event listener for the "Copy links" button
        document.getElementById('copyBtn').addEventListener('click', () => {
            const linksBox = document.getElementById('linksBox');
            linksBox.select();
            document.execCommand('copy');
            alert('Links copied to clipboard!');
        });

        // Theme Toggle Functionality
        const toggleThemeBtn = document.getElementById('toggleThemeBtn');
        const themeIcon = document.getElementById('themeIcon');
        let isDarkMode = false;

        toggleThemeBtn.addEventListener('click', () => {
            isDarkMode = !isDarkMode;
            document.body.dataset.theme = isDarkMode ? 'dark' : 'light';
            themeIcon.innerHTML = isDarkMode ? `
                <!-- Corrected Crescent Moon Icon -->
                <path class="moon-icon" d="M21 12.79A9 9 0 1111.21 3 7 7 0 1021 12.79z" />
            ` : `
                <!-- Sun Icon -->
                <circle cx="12" cy="12" r="5" stroke="currentColor" stroke-width="2" fill="none"></circle>
                <line x1="12" y1="2" x2="12" y2="4" stroke="currentColor" stroke-width="2"></line>
                <line x1="12" y1="20" x2="12" y2="22" stroke="currentColor" stroke-width="2"></line>
                <line x1="4.22" y1="4.22" x2="5.64" y2="5.64" stroke="currentColor" stroke-width="2"></line>
                <line x1="18.36" y1="18.36" x2="19.78" y2="19.78" stroke="currentColor" stroke-width="2"></line>
                <line x1="2" y1="12" x2="4" y2="12" stroke="currentColor" stroke-width="2"></line>
                <line x1="20" y1="12" x2="22" y2="12" stroke="currentColor" stroke-width="2"></line>
                <line x1="4.22" y1="19.78" x2="5.64" y2="18.36" stroke="currentColor" stroke-width="2"></line>
                <line x1="18.36" y1="5.64" x2="19.78" y2="4.22" stroke="currentColor" stroke-width="2"></line>
            `;
        });
    </script>
</body>
</html>
