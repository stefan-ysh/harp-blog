# blogstrapi
Personal blog using a Dynamic CMS for development with a Static HTML for deployment.

---
## About blogstrapi
**blogstrapi** was a personal project to create a GUI **head** that is modular, which can be developed with any "Headless" CMS backend.

![Index page](https://snipboard.io/wuN75Z.jpg)

---
### Responsive and Fast
The GUI is developed using Bootstrap 4 and Harp.js, which supports EJS. The navigation menu collapses, when viewed on a mobile device, into a *hamburger* menu.

![Viewed on a mobile device](https://snipboard.io/GliKR3.jpg)

---
### Modular
Partials that contain embeddable code are stored in the *layout* folder, e.g. *_header.ejs*.

---
### Head
Blog articles are stored as *markdown* files in the *blog/* folder, while their metadata are stored in *_data.json* within the same folder. Harp generates one *html* per *markdown* file.

The index page dynamically populates all articles' snippets from the *metadata* stored in *blog/_data.json*.

---
## Blog
This is my [blog](http://blog.tldr.pro), which is based on the this template, and it has a [tutorial](http://tldr.pro/blog/blog/creating-a-blog-theme-with-bootstrap-and-harp.html) explaining how **bootstrapi** was developed.

---
## Project Structure
     blogstrapi/                 <-- Root of your project
       |- package.json           <-- Node.js project entries
       |- _harp.json             <-- Global variables goes here
       |- _data.json             <-- Page variables goes here
       |- _layout.ejs            <-- Common layout for each page in root folder
       |- index.ejs              <-- Home page of your blog, Harp will produce an index.html
       +- css/                   <-- Holds any CSS or SCSS theme files
          |- bootstrap.min.css   <-- At a minimum, the bootstrap CSS file
          |- mytheme.css         <-- Our custom CSS theme goes here
       +- js/                    <-- Holds any JS files
          |- bootstrap.min.js    <-- At a minimum, the bootstrap JS file
       +- layout/                <-- Holds any partials, prefixed with "_"
          |- _header.ejs         <-- Header partial, i.e. called by partial() function
          |- _footer.ejs         <-- Footer partial, i.e. called by partial() function
       +- blog/                  <-- Holds any articles in Markdown files, Harp produces a html per md file
          |- _data.json          <-- Blog articles metadata goes here
          |- _layout.ejs         <-- Layout for each article in blog/ folder

---
## Example Usage
In the following example, the default application will be created in the folder *myproject/*.

     $ harp init myproject --boilerplate dennislwm/blogstrapi

In the folder *myproject/*, spin up the server, which can be viewed at [localhost:9000](http://localhost:9000)

     $ harp server

---
## Reach Out!
Please consider giving this repository a star on GitHub.

---
## License
The **blogstrapi** source code is licensed under the [GPL-3.0 license](https://github.com/dennislwm/blogstrapi/blob/master/LICENSE).