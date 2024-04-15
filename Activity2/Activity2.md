# Activity 2: Angular Tools & First App

**Screenshot 1: Running the TestApp of the new Angular Application**
![Caption for Image 1: Angular CLI Installation Success](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity2/Images/2.1.png)

**Screenshot 2: Changed the Heading tag and added a new message to the app**
![Caption for Image 2: Running Angular Test Application](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity2/Images/2.2.png)

## Research and Insights

### Project Structure and Purpose
The `node_modules` folder is crucial for storing npm packages required by the project. The `src` directory holds the application's source code: `src/app` contains the application's logic and components; `src/assets` is used for static assets like images; `src/environments` contains environment-specific settings. Configuration files include `angular.json` for Angular CLI project settings, `package.json` for tracking dependencies and scripts, and `tsconfig.json` for TypeScript compiler options, outlining the project's compilation strategy.

### Generation of the Default Page
Angular's default page comes to life through a well-orchestrated use of several files. `main.ts` is the application's entry point, initiating the root module, `AppModule`. Styling is specified in `app.component.css`, while `app.component.html` provides the HTML template. `app.component.ts` drives the component's logic, including variable declarations like `title` and `message`. The `app.module.ts` file declares the AppModule, integrating components and modules, showcasing Angular's modularity and its dependency injection mechanism.
