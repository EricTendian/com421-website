# COM 421 Website Project

[View the website at erictendian.github.io/com421-website](http://erictendian.github.io/com421-website/)

This website is pretty simple - it just has two pages, an online version of my resume, and an additional page with a portfolio of my past work. Both pages in the site make use of a 12-column grid system, and the columns are also responsive - each column takes up the full width of the page below a certain screen size.

On the resume page, you can see I transferred over a lot of the styling and formatting from my original print resume, but adapted it for the web. That means there is a bit more spacing in some places, and less space in others. I was able to transfer over the icons from the print resume and include them in `::before` pseudoelements as a background image. I made use of CSS classes and ids to style the page, and separated styling specific to the resume from the base styling via adding the ID "resume" on the `<body>` element. I also made use of columns, borders, and padding to make the layout match the print resume.

On the about page, I have a couple sections: an introduction header with a background image, a small portfolio of my past web development work, a longer biography of myself, and a footer with additional links. I used CSS transitions to make the button on the header fade in and out. The portfolio was grouped into types of websites, and each image is linked to a larger version. I made sure the alt text for the images described the website shown. The biography section on the about page contains a couple more links to other things I have worked on. The footer has two parts - the top part is a 3-column layout with some relevant info in each column, and the bottom part is just for copyright and citations.

While I did put a good amount of effort into this project, there are many more things I wanted to implement given more time. First, I would want to optimize the site for mobile, which would mean adding more queries and sticking to a mobile-first approach. Secondly and related, I want to standardize the units I use in my CSS - make everything in EMs, which are better for accessibility and scaling purposes. Currently the units are mixed up which is not ideal. I would also want to convert the existing CSS into SASS or LESS, which would help improve the readability of my CSS and also make it more easy to manipulate. As I am adding `#resume` or `#about` to many of my rules, that can become tedious. On the design side, I would make a better looking navbar and add a better footer to my resume page. Furthermore, there is little consistency in design between the resume and about page - while this was intentional as I tried to replicate the look of my print resume for the web, the about page design was based on some of the existing websites I had built.

*Citations:*

- The original folder/file structure, as well as a couple files, came from HTML5 Boilerplate. I am using the included `normalize.css` to help standardize the look of the pages across different browsers. `modernizr.js` is also used to support some HTML5-only features.
- There was no JavaScript used in this site, although I do have some JavaScript files loaded in case I want to add some in the future.
- Icons for the resume came from The Noun Project (various authors) and icons for the about page came from Font Awesome.
- The picture in the header of the about page (an icon of my face) was designed by a coworker at Packback.
- The background image for the header is a public domain image from SpaceX.

*Addressing feedback:*

- [done] You can get rid of that business about IE8 and outdated browsers entirely. Chances are if someone is using IE8, they're being forcibly compelled to do so. Later on you can build a responsive site that serves outdated browsers (you can even make it so that it will work on a text only browser if you want to).
- [done] That Pure template that you're using is a mess. Keep what you want for the section and header spacing, but trash all of the text formatting, etc. You can do a better job on your own. Provided it's not a ToS violation to download the sheet and modify it (I'm guessing not), grab it and comment out all of the text formatting, then write that up in your separate CSS file.
- [done] One thing it's screwing up are your h3's -- you're getting slightly different displays and spacing between your sections. Set it up so that they are all the same.
- [done] The personal details section is a little hard to read--space out those lines
- [done] About page: you need to cite the image and check copyrights
- [done] Spans don't actually define the position of the information in the hierarchy of the page; if the only reason you're using <span> is to style the element, write a complex CSS selector instead (or if it is a one-time thing, use the developer tool in your browser to get the selector)
- [done] With your portfolio, you're better off just putting those screenshots in a grid with defined widths, otherwise the layout gets all screwed up when you resize the browser or use a mobile device. You can integrate the responsive handling some time in the future when you have the free time.
- [done] Also, those screenshots need a border or some separation (like a different background color). A lot of them are white backgrounds, so they make traversing the grid a challenge. Since you have so many sites, you probably want to group them together by project type.
- [done] The alt-text on those images needs work--try to actually describe the object the person is looking at
- [no - sites changed since screenshots taken] Are you going to link to those sites so people can see them?
- [ok] The site is looking pretty good. You're a little over-reliant on your template, but I'm guessing that's something you're going to address as you continue to work on this site. Don't worry so much about bells and whistles at this point, e.g. favicon, custom 404 message, etc. Focus on the fundamentals and remember that you can keep adding to the site in the future.
