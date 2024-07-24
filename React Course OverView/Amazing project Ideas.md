

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
  
Step 1: Set up the project

- Use the pages folder and index.js file within the api folder
- Delete the contents of index.js and add a single div tag
- Use the ES7+ React/Redux/React-Native extension for VS Code (RAFCE)

Example:

import React from 'react';
const index = () => {
  return (
    <div>index</div>
  )
}
export default index


Step 2: Set up the babel file and ESLint

- Create a .babelrc file in the root directory
- Add the @babel/preset-react preset to the .babelrc file(import syntax of react js is needed. )
- Install the @babel/preset-react package using npm
- Create an eslintrc.json file in the root directory

Step 3: Rename the index.js file to Home.js

- Rename the index.js file to Home.js
- Update the contents of Home.js to include the Head component and styles from Home.module.css

Example:

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


Step 4: Set up the styles

- Go to the styles folder and find the globals.css and Home.module.css files
- Update the Home.module.css file to include styles for the Home component

Step 5: Set up the components

- Create a new components folder and add component files within it
- Create an index.js file in the components folder to export all the components
- Add the following exports to the index.js file:
    - Footer
    - Layout
    - Navbar
    - Product
    - HeroBanner
    - FooterBanner

Step 6: Set up the Sanity client

- Create a new folder named LIB and add a file named client.js
- Add the following contents to the client.js file:

Example:

import sanityClient from '@sanity/client';
import imageUrlBuilder from '@sanity/image-url';
export const client = sanityClient({
  projectId: "",
  dataset: "",
  apiVersion: "",
  useCdn: true,
  token: process.env.NEXT_PUBLIC_SANITY_TOKEN
})
const builder = imageUrlBuilder(client);
export const urlFor = (source) => builder.image(source);


Step 7: Connect to Sanity

- Go to the sanity/ecommerce folder and run sanity manage
- Create a .env file in the root directory and add the NEXT_PUBLIC_SANITY_TOKEN env key
- Import the client from ../lib/client in the Home.js file
- Add the getServerSideProps function to the Home.js file to fetch data from Sanity

**format the content from here.** 
 
Step 8: Implementing each components one at a time. 

- outer div gets the class name "hero-banner-container"
- creating template and dummy text to display dynamic value
- create all the links needed.
- connect the application with sanity. 
- create a folder named lib, add a new file named client.js and add the contents, this you need to do only once in your project and can reuse it multiple times. 
- go back to index.js and import the client file from lib folder. 
- In next js to fetch data use getServerSideprops. 

export const getServerSideProps = async () => {
const query = to get all the products from sanity. 
get products, use one more query for banner. 
and get the banner details. 

return {
props: {products, banner}
}
}


Step 8: second component build up.

- 
- point






















