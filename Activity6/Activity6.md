# Activity 6: React Music App API Data

## Part 1: External Source Data
**Screenshot 1: Our main page now has the albums from our database. You can see that there is a search bar on top as well so that the user can find a specific term in the albums. The image shows about the card, with the description below it.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/1.1.png)

**Screenshot 2: Here we have the card based off what was searched in the search bar. The term Help was used and the album was filtered to be the only one showed.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/1.2.png)

**Screenshot 3: Here we are in our dev tools so that we can see that the album has been filtered properdly, with the array returing in the console, as well as the term that was searched.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/1.3.png)

# Summary of Part 1
In this part of the activity, we transition from managing album data within the application to utilizing an external JSON file. The album list, initially housed in the state initialization of App.js, is relocated to albums.json. This move sets the stage for integrating an Express Music API in the next phase of development. By importing the JSON file into App.js and utilizing useState and useEffect hooks, we establish a streamlined process for updating and rendering album data, setting the groundwork for further functionality expansion within the React Hook Lifecycle.

## Part 2: Mini App # 2 - Routing Application Demo

**Screenshot 1: When we run the application, we get sent to this page where we can see the navbar we created. We can also see a list of friends below the navbar.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/2.1.png)

**Screenshot 2: Before we can see the About page, we first have to login in. There is a sentence stated that you must login in first, and all you have to do is just click the Login Here button.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/2.2.png)

**Screenshot 3: In this screenshot, we can see the About Statement after we click the Login Here Button.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/2.3.png)

**Screenshot 4: In this screenshot, we are now in the Contact Us page, where we have some information such as the name of the Comapny, the address of the company, as well as a phone number of the company.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/2.4.png)

**Screenshot 5: In this screenshot, we are now in the Ned Navigator after we click on the link in the navbar. We can see a Hello Ned message to indicate that we have indeed have click said link.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/2.5.png)

**Screenshot 6: In this screenshot, we can see that we are now in the Login page, after clicking the Login tab in the navbar. There is a button on the page which says Login Here and when you click it you will be logined in.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/2.6.png)

# Summary of Part 2
In the "Mini App #2 - Routing Application Demo" section, we dove into demonstrating the capabilities of React's react-router-dom library within our music application. We set up various routes like /about and /contact, allowing us to render different components based on the browser's URL, simulating a multi-page application experience within a single-page application framework. Key steps included starting a fresh project, installing the routing library, and creating the essential components for navigation, such as AboutUs, ContactUs, LoginPage, and a PrivateRoute for authorized access, effectively showcasing the dynamic routing and navigation features of React.

## Part 3: Navigation Routing

**Screenshot 1: In this screenshot, we can now see a better search bar on top of the cards, as well as a header with the title My Music. Everything runs more smoother and the cards still look good in there place.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/3.1.png)

**Screenshot 2: We filtered the albums for the term Rubber Soul, which was in two different albums. The search os more smoother and runs perfectly.**
![](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity6/Images/3.2.png)

## Summary of Part 3
In this part of our activity, we focused on enhancing the music application by integrating navigation routing. After installing react-router-dom, we refactored the renderedList method into a new AlbumList component to manage the display of Card components, adhering to React's best practices of component-based architecture. This restructuring allowed us to create cleaner code in App.js, offloading responsibilities to SearchAlbum and AlbumList components, setting the stage for more advanced features like routing and album editing, while still maintaining App.js as the stateful core of our application.
















