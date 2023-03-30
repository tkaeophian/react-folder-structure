When it comes to structuring a React.js application, there are several best practices to follow that can help improve organization, maintainability, and scalability of your codebase.

## 🙃 Basic Folder Structure

Use a flat structure for small projects: For smaller applications, a flat folder structure can be sufficient, where you can have components, styles, assets, and pages in the same level directory.

[Show me the code](basic)

## 😊 Intermediate Folder Structure

Follow a component-based architecture: Create separate folders for components, containers, and pages. Components folder should contain small and reusable components. Containers folder should contain components that have stateful logic and interact with external data sources. Pages folder should contain components that represent a full screen or a route in your application.

[Show me the code](intermediate)

## 😇 Advanced Folder Structure

Separate concerns based on feature or function: Divide your application into smaller modules based on their feature or function, and group them in folders with clear and concise names. For example, you can have folders for authentication, user management, dashboard, etc.

Use an index.ts file to export modules: Use an index.ts file in each folder to export the modules from that folder. This can help to simplify imports and make your code more readable.

Most of the code lives in the `src` folder and looks like this:

```sh
src
|
+-- components        # shared components used across the entire application
|
+-- features          # feature based modules
|
+-- hooks             # shared hooks used across the entire application
|
+-- lib               # re-exporting different libraries preconfigured for the application
|
+-- providers         # all of the application providers
|
+-- stores            # global state stores
|
+-- utils             # shared utility functions
```

Lets dive further into the `features` folder, a feature could have the following structure:

```sh
src/features/awesome-feature
|
+-- api         # exported API request declarations and api hooks related to a specific feature
|
+-- components  # components scoped to a specific feature
|
+-- hooks       # hooks scoped to a specific feature
|
+-- stores      # state stores for a specific feature
|
+-- index.ts    # entry point for the feature, it should serve as the public API of the given feature and exports everything that should be used outside the feature
```

[Show me the code](advanced)

## Extras

Remember, the most important aspect of organizing your React.js application is to make it easy to navigate, understand, and maintain. So, choose a structure that works best for your application and team, and ensure consistency throughout the project.
