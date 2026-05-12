
# Basic Express.js Server

## LAB OVERVIEW
A basic website backend server built using Node.js and Express to serve web pages.


## Prerequisites:
- npm
- Terminal CLI / CMD
- IDE
- Web browser (Chrome, Firefox)
- Node.js
- Express.js
- Nodemon


## Installation
git clone https://github.com/uries242/daily-grind-server
cd [your-repo-name-here]
npm init
npm install express
nodemon - to execute the server.js file



## Reflection Questions
1. What is the difference between res.send() and res.sendFile()? When would you use one over the other?
The difference between these two methods relates to the type of data they handle. For instance, res.send() handles primitive data types such as strings, arrays and objects while res.sendFile() handles static files. 
Res.send() is better suited for quick responses or API data. Res.sendFile() is used when serving full HTML pages such as index.html.

2. Why is the path module necessary when serving files? What could go wrong if you just used a relative path like 'public/index.html'?
The path module converts relative paths to absolute, system-agnostic paths. It ensures the file path is constructed properly and that the file serving works correctly. Using a relative path may result in your app crashing if node is unable to accurately locate the entry file. This is because relative paths resolve from whatever directory Node was launched from, not where server.js lives, so if the working directory differs, Node will look in the wrong place. 

3. How would you add a third page (e.g., a menu page) to this server? What steps would you take?
To add a third 'menu' page, I would first create a new file named 'menu.html' with relevant content inside my public directory. Next I would add a new route in my server.js file, also using the path module to create an absolute path. 