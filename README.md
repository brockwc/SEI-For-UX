# WDI for UXDI

![UX and WDI](assets/combined.png)

## Understanding Developers

### **Developer Roles**

- **Fullstack Web Developer**
  - Works in both developing the Client facing side and Server facing side.
- **Front End Web Developer**
  - Works on the client facing side dealing mostly with HTML, CSS, and Javascript following design patterns handed to them from design team. They are often responsable for connecting the client facing side to the back via API calls.
- **Back End Web Developer**
  - Works on the backend server facing side. Responsible for maintaining the site's database structure and ensures the site is constantly up and running with minimal down time. 

There are many types of web developer roles, but most can fit into these three catagories. [Here are some examples.](https://blog.codeplace.com/all-the-job-titles-you-can-have-as-a-developer-f16c5f1f1380)

### **Developer Tools**

**CLI / BASH / Terminal  <img src="assets/terminal1234.png" width=25px/>**

![terminal](assets/cli.gif)

[Terminal Cheat Sheet](https://gist.github.com/LeCoupa/122b12050f5fb267e75f)

**Code Editors </>**
  - [Visual Studio Code (New hotness)](https://code.visualstudio.com/)
  - [Sublime Text](https://www.sublimetext.com/)
  - [Atom](https://atom.io/)

![code](assets/vscode.gif)

**GITHUB <img src="assets/Octocat.png" width=50px/>**

**What is it?**

Github is a source managment system that is hosted online for remote version control. For developers it allows us to create clones, backups, and work together on our software. Some alternatives you might see out there are Gitbucket, GitLabs, and Source Forge.

How Github works:

![git diagram](assets/local-remote-chart.png)

Branches with Github:

![branches diagram](assets/branches.png)


[Github Example](https://github.com/nodejs/node)

### **Browser Dev Tools**

Built right into our browsers are powerful development tools! Check them out with: 

right click -> Inspect

View -> Developer -> Developer Tools

Option + Command + i

![dev tools](assets/chromeDevTools.gif)

## How to Work and Communicate Effectively With Developers

### **Provide an adequate level of documentation.**

Developers LOVE <3 documentation. Nothing is scarier to a developer then a blank canvas. Leave notes and descriptions of everything in your design layouts to ensure there is no miscommunication on what something is suppose to be/do.

Below we have a basic wireframe example. With no documentation we can see how open it is for interpretation. 
![no docs](assets/wireframes.png)

Here we have a little more direction with colors and general spacing, but still no documentation to help decide things like exact color, font, etc.

![no docs](assets/nodocs.png)

Finally we have a wireframe with some documentation to let the developer know what font they will be using. Adding in things like line height, weight, and colors will make a big difference. 

![docs](assets/docs.png)

If you do all of this your dev team will be *oh so happy*.

### **Be decisive.**

Once again, nothing scares a developer more then a blank canvas. With clear and precise directions developers will follow them through to a tee and deliver a final product. Programmers are by nature **not** design oriented. This occurs due to the technical critical thinking that is important to strong development. So be decisive in your designs and own them. If you are seeking input about functionality or overall appeal of the design feel free to include your developer to create a strong bond, but don't leave your designs open for interpretation. This only slows down development time overall.

### **Communication is key, so be available to clerify.**

Your developer will have questions about your designs and documentation. Never expect your developer to know all of your lingo. No matter how simple it is. So be open to answering questions that they will have. 

For example: 
```
"What is this arrow suppose to represent on the bottom of the profile page?" 
```

### **Set realistic deadlines, and stick to them.**

Time blocking and sprints are a developer's best friend. If you are taking the time to ensure you are hitting the sprints on time and sticking to your deadlines this will ensure your developers have plenty of time to work on their code. The more time a developer has the more time that is open for development, testing, and deploying. 

### **Test it yourself.**

Don't rely soley on your developers code. A second pair of eyes and hands will find bugs and ensure that *your* design is coming together. If you do find a bug or an unexpected design shift in the site's functionality let your developer know immediatly. 

## Time to step into the shoes of a developer.

### How does the internet work? 

The flow of the internet is directed via this: 

Client goes to their browser and types in Google.com -> The browser sends this **request** to a DNS server and translates the Google.com to an **IP Address** -> With this information the browser and connect directly to the **web server** holding holding all the code for the site. -> The **web server** checks it **database** for information that is percistant across the site and sends it back to the **web server** -> from there the **web server** sends the final site back to the **client side web browser**. 

Alot of work for you to look at cat gifs.

<img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" width=200px/>

Here is a general flowchart.

<img src="assets/webflow.gif" width=200px/>

### **The languages that make up the web.**

  - HTML
    - The "structure" of a web site.
  - CSS
    - The "design" portion of a web site.
  - Javascript
    - The "functionality" of a web site.

### **HTML**

There are two main areas of HTML. The Head and the Body.

The **Head** holds the meta data of the site. This includes links to other files and important information including how to detect the screen size.

```html
<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Portfolio</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" media="screen" href="main.css" />
    <script src="app.js" defer></script>
</head>
```

The **Body** holds the *rendered* content of the website. This is what the user will see and interact with. This in most cases have an internal split of a **Header**, **Main**,and **Footer**.


Let's breakdown a simple static one page portfolio site.

```html
<body>
    <header>
        <Nav>
            <a class="menu" href="#">Home</a>
            <a class="menu" href="#">Projects</a>
            <a class="menu" href="#">Contact</a>
        </Nav>
    </header>
    <main>
        <section id="hero">
                <h1>Welcome to my portfolio!</h1>
                <p>Take a look at all my cool stuff!</p>
        </section>
        <img src="https://media.giphy.com/media/freTElrZl4zaU/giphy.gif" alt="cat gif">
        <form action="post">
            <input type="text" placeholder="You can type stuff here!">
            <button type="submit">Submit</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2018</p>
    </footer>
</body>
```
To tell our document which version of HTML to use we have to add the following around our **head** and **body** :

```html
<!DOCTYPE html>
<html>
  <!-- Code inside here -->
</html>
```
When we put it all together we get: 

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Portfolio</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" media="screen" href="main.css" />
    <script src="app.js" defer></script>
</head>
<body>
    <header>
        <Nav>
            <a class="menu" href="#">Home</a>
            <a class="menu" href="#">Projects</a>
            <a class="menu" href="#">Contact</a>
        </Nav>
    </header>
    <main>
        <section id="hero">
                <h1>Welcome to my portfolio!</h1>
                <p>Take a look at all my cool stuff!</p>
        </section>
        <img src="https://media.giphy.com/media/freTElrZl4zaU/giphy.gif" alt="cat gif">
        <form action="post">
            <input type="text" placeholder="You can type stuff here!">
            <button type="submit">Submit</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2018</p>
    </footer>
</body>
</html>

```

When our page renders out we are greeted with the following: 

<img src="assets/portfolio1.png" width=500px/>

#### *YIKES!* 

That is not looking very good. Time to bring in CSS!

### **CSS**

