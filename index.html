<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Link Scraper</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        h1 {
            color: #333;
        }

        #description {
            max-width: 800px;
            padding: 15px;
            background-color: #fff;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        #scrapeBtn {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
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
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            min-height: 300px;
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
            color: #555;
        }

        #urlInput {
            width: 80%;
            max-width: 600px;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-shadow: 0 1px 5px rgba(0, 0, 0, 0.1);
        }

        /* GitHub Link Styling */
        #githubLink {
            position: absolute;
            bottom: 10px;
            left: 10px;
            font-size: 14px;
            color: #007bff;
            text-decoration: none;
        }

        #githubLink:hover {
            text-decoration: underline;
        }

    </style>
</head>
<body>
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
                document.getElementById("demo").innerHTML = `Invalid Link`;
                return;
            }
            links = []; // Reset links array on each scrape
            fetchLinks(validUrl);
            document.getElementById("demo").innerHTML = `Scraping your links now...`;
        });

        // Event listener for the "Copy links" button
        document.getElementById('copyBtn').addEventListener('click', () => {
            const linksBox = document.getElementById('linksBox');
            linksBox.select();
            document.execCommand('copy');
            alert('Links copied to clipboard!');
        });
    </script>
</body>
</html>
