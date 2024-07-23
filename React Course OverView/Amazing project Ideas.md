

JavaScript Video reference, https://www.youtube.com/watch?v=XxXyfkrP298


45min video, 

-> Finish a project, and then try finishing the project. Practically and then only move to next project. 


Project Creation

- Create a new folder on the desktop for the project (e.g., "Ecommerce")
- Drag and drop the folder into Visual Studio Code (VS Code)
- Open the terminal in VS Code by going to "View" > "Terminal"

Initializing the Project

- Run the command npx create-next-app to create a new Next.js project
- Proceed with the installation by typing Y
- Enter the project name: "Ecommerce"
- The app is initialized, and the files are created

Important Folders and Files

- The most important folder is pages, which contains the application's routes and [[pages]]

Installing Dependencies and Packages

- Currently installed:
    - Next.js
    - React
    - React DOM
- Additional packages to install:
    - Sanity
    - Sanity/image-url
    - Stripe/stripe-js (payment gateways)
    - Canvas-confetti
    - React-hot-toast
    - React-icons
    - Traverse

Installing Packages

- Navigate to the project folder: cd .\ecommerce\
- Run the command: npm install --legacy-peer-deps

npm Install Flags

- npm install (without the flag): Strict installation, ensuring peer dependencies match the specified version ranges in package.json.
- npm install --legacy-peer-deps: Lenient installation, allowing peer dependencies to be installed even if they don't match the specified version ranges.

 Spinning up the Application

1. Run npm run dev to start the development server.
2. Terminate the batch job by pressing Ctrl + C and clear the console using cls or clear.

Setting up Sanity CLI

1. Install Sanity CLI globally using npm install -g @sanity/cli.
2. Initialize a new Sanity project using sanity init --coupon javascriptmastery2022 (press Enter one more time to confirm).
3. Add Google authentication credentials.
4. Choose a project name (e.g., "ecommerce").
5. Use the default dataset configuration.
6. Create a new dataset.
7. Choose a project template.

Configuring Git Ignore

1. Open the .gitignore file.
2. Ignore the node_modules directory by changing the line from /node_modules to node_modules.

Starting Sanity Studio

1. Run sanity docs to open the Sanity documentation.
2. Run sanity manage to open the Sanity manager.
3. Traverse to the Sanity studio (e.g., "sanity_ecommerce" or rename it to "ecommerce").
4. Run sanity start to spin up the Sanity studio.

Creating Schemas

1. Go to the schema folder in your Next.js project.
2. Create schema files for banner and product.
3. Open the Sanity studio and see the added data models. 
4. Add dummy data to test the schema.

Front end: we will be using react.js(Technically next.js)

   1. Use the pages folder and index.js file within the api folder in pages folder. 
   2. Delete all the contents of index.js file(just keep one div tag - or you can delete the entire thing and keep this content.


   Use ES7+ React/Redux/React-Native extension for VS code. (RAFCE)

   ```javascript
import React from 'react';
const index = () => {
return (
<div>index</div>
)
}

export default index
```


    run npm run dev from next js ecommerce folder to see the project running. 

    start using the VScode and the browser side by side to see the changes.

   3. Set up the babel file within the styles folder also the [[eslintrc.json]]. 
   4. going back to the Index.js file, rename the index.js file to home. 

   Example:      
```javascript
import Head from 'next/head';
import styles from '../styles/Home.module.css';

export default function Home() {
  return ( 
    <>
      HeroBanner
      <div>
      <h2>Best selling products</h2>
      <p>speakers of many variations</p>
      </div>

      <div>
      ['product 1', 'product 2'].map((product) => product)
      </div>
      Footer
   </> 
  );
}
```


   5. Working on the styles, go to the folder named [[styles]]. you will find two folders globals.css and Home.modules. 











 










 



























   







