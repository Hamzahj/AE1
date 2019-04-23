# Intro 
This project aims to produce a web app that will allow results for tourist hotspots to be shown in a visually pleasing way. The issue lies in the fact that when visiting another country or city, you end up having to search for specified tourist hotspots individually. For example, if you wanted to go skiing, based on user interviews many have to search on google to get these results. The fact is that many people want to know all the options when it comes to tourism and exclude the concept of having to search it up. This app will consume data from the autora api and allow for all tourist hotspots to be displayed along with all the necessary information. 

# Background 
Can search results be displayed in a visually attractive way? The gravity of this problem varies as depending on the demographic for different search engines it can be a big issue or a small issue. Many major search engines and websites such as google have a problem where results will only appear with links but no images to visual images to accompany them. As shown below the links are simple, however if images were to accompany them it would be slightly more attractive. Although not a necessity the single page app will be a tourism website where results will appear on a page. The single page application will be designed to simplify results to make results pleasing to view.  This article will focus on many things such as CSS grids, using Vue js, APIs, methods, wire framing, design inspiration, user research and user testing.  


![](1.png)

# Aim 
The aim is to simplify the way results appear on websites accompanying to potential consumers of the market based on qualitative and quantitative research. The website will mostly be desktop based, however not limited as mobile first will also be considered. 
Objectives 
•	Investigate UX issues and other issues in displaying data 
•	Explore how Vuejs and routing can be implemented
•	Base wireframes and UX on qualitative/quantitative research
•	User testing 

# Methods
Workflow
Preparation (10 hours)
Wireframing, sketches and research will need to be completed, this will approximately take around 10 hours. Sketches will be done, wireframe.cc will also be used to create medium fidelity wireframes and adobe xd will be used for high fidelity wireframes. The high-fidelity wireframes will need to be like the single page application. Design inspiration will be gained from various websites. Planning will take around 10 hours to complete. 
Research (20hours) 
Research will be conducted on, responsive designs, CSS grids, media queries, Vue js, routing, design inspirations. This will take around 20 hours 
Implementation (30 hours)
After research is conducted the implantation will begin, the techstack being used will be cloud9, GitHub, frameworks such a Vue.js. The implementation process will require getting data from the Autora Api, routing, Vue.js cards and CSS will be used heavily to accompany the designs. Based on research a CSS grid will also need to be considered along with media queries. This will allow users to use the SPA on many devices such as mobiles. Although it isn’t a necessity as the tourism website is desktop based it will be useful to have a responsive design. Any user surveys or interviews conducted will need to be taken into consideration when designing the SPA. 
Testing the app (2 hours)
The app will be tested by potential users and different browsers, to ensure compatibility and to gain good/bad feedback so that it can be improved in the future. 


# Implementation (Design)
You will explore:
•	User research (e.g. interviews, surveys and focus groups)
•	Design inspiration
•	UX/Wireframes
•	Hi-Fidelity Wire Frames
•	User Testing, (must be done with a realistic sample demographic, not your friends)


# Research 
A Survey was conducted and questions asked that were necessary to ensure when designing the SPA, the designs would accompany the user’s needs. The answers from the survey allowed to understand what to implement and what users would prefer in a tourist web app. Around 20 responses were recorded which was enough to understand what different demographics preferred. 









































# Design inspiration
https://www.awwwards.com/websites/scrolling/, inspired me to apply scrollable parallax features to the single page app as based on the user interviews this design was found to be the most attractive feature and the most modern. bing.com was also  analysed and the search engines most attractive feature was the stretched background image as it was eye-catching. 

 

# UX colour
According to https://optinmonster.com/11-hacks-to-keep-visitors-on-your-pages-longer/ UX can be one of the differences between someone spending less than a minute or more than a minute on your website. In 2017, Google changed the way their search results appeared and it had a massive impact as users took a heavy dislike of the new change. When the links were clicked, there was no indication that they had been clicked. For example when links in the search engine results were clicked, they changed colour from blue to purple to indicate that the link was clicked on already. Google testing something so small had a big impact on users. Fortunately, for google, they realised that this was not a good change and reverted it back to normal. Below shows, the two different colours that google used and the picture to the left has a very bland feel to it whereas the picture to the right has feels how google should feel.



# Wireframes











# Implementation 
A github repository was set to ensure version control and along with this dependencies were installed. Node modules were made and although certain problems installing these dependencies occurred such as updating the modules, they were finalised to start the project. 
Web responsiveness 
Responsive web design is a technique that allows screen size to adjust automatically, so that when resizing the page, all elements will move with it. This is where CSS grids come into place and this will allow elements to be redefined using media queries. Firstly a 12 column CSS grid was created to ensure responsiveness as some users might be using different size laptops or computers.  However, since the tourist information website is based on desktops it is not a necessary but would be pleasant for users when it comes to using smaller devices. Media queries were used to ensure that when a browser is minimised it will adjust to the size of the page. A 12-column grid was made in CSS and along with this break points were made to ensure that when the browser is resized, you can still view all the content on the page. 
Once the grid was made, a Vue.js card template was used from the official vue website. The json file from the Autora api that was needed for placeholder data was implemented. 

SPA (multi page applications) and routing
The official VUE js documentation states that it is recommended that routing is used on an SPA, as this allows for websites to re render themselves without making request to the server. This allows for webpages being loaded in an instant and can be useful for forms and single page applications. 
To do routing on a single page application, a router is required and in the router there can be multiple paths.
Firstly the router needed to be installed, to do this a simple command was run in the terminal and creating the vue project. Node.js was also installed to make sure vue-cli could be used to make a project. A template was automatically created inside the app.vue file and this is where routing would take. Firstly vue and also the vue router was imported. Then next vue was told to use the vue router. After this a router was finally configured. In the main.js file vue would need to be imported again and the third line was importing the router setup. 
A new routes.JS file was made so that the 2 components could be imported using an array of objects. The first default component was just a simple backslash to set the path location. This was the homepage that was created. The next was the add data page where all the api results would be displayed in their cards. 
“<router-link :to="'/'">”  was the tag used to set up the navigation bar so that the paths for the different files were accessible. This would allow for the different links to be clicked when viewing the pages. Once the routing was set up, two pages were left with templates inside. These were the components made earlier ready to be edited. 
Consuming apis
Consuming the 

Pure css was used to create a parallax feature using no frameworks whatsoever as this would be simple to create. The css was 














# Evaluation (Design)
You will have to show that you have tested your site and ideas with representative users
