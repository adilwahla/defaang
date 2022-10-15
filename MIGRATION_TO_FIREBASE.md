[ ] How to do migrations?

Step 1: Create a Firebase project and register your app
### Creating a Firebase project
To setup Firebase, use the following steps:

First, go to the [Firebase console](https://console.firebase.google.com/) and Add project. Enter the preferred name of your project, i.e., Defaang-app. Then click continue.

Then Configure Google Analytics and click continue.

Create a project and give it some time to complete the process. When the project is ready, click Continue.
Adding a Firebase app
The next step is to create a Firebase app. We can implement this functionality using the code below:

On the newly created project page, click the web icon (</>).

Enter your preferred app name, i.e., Defaang-app. Then click Register app and Continue to console.

In the next step, we will set up Firestore.

Setting up Firestore
To set up Firestore, follow the steps below:

In the Firebase App, navigate to the left menu, under build, and click Firestore Database then Create database.

Since we are not building a production application, select the start in test mode and move to the Next step.

Choose the Cloud Firestore location from the list of options available and then click Enable to set the selected location.

In the resulting page, we will start by creating a Collection to be populated from our  application.

Click Start Collection and add the Collection id as todos and move to the Next step.
//will discuss with ykdojo ...!
**Setting up Next.js app**
Step 2: Install the SDK and initialize Firebase
>npm install firebase

With Firebase installed, run the following command to start the development server:

>npm run dev

Step 3: Access Firebase in your app


Initialize Firebase in defaang and create a Firebase App object
```
import { initializeApp } from 'firebase/app';

// TODO: Replace the following with your app's [Firebase project configuration](https://firebase.google.com/docs/web/learn-more#config-object)
const firebaseConfig = {
  //...
};

const app = initializeApp(firebaseConfig);
```

In simple terms, initializing a Firebase app means connecting the Firebase database instance/SDK so that we can work and scale the Next.js application.

This simply involves collecting the Firebase credentials that are specific to our Firebase application.

To initialize it, we will use the following steps:

Create an env.local file in your project root folder. This will host the environmental variables.

In your Firebase dashboard, navigate to the project settings. Scroll down to your apps section and then to the SDK setup and configuration.

In the app settings, we will take firebaseConfig object. Extract its contents to the .env.local file, as demonstrated below:
>NEXT_PUBLIC_FIREBASE_API_KEY = "your_api_key"
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN = "your_auth_domain"
NEXT_PUBLIC_FIREBASE_PROJECT_ID = "your_project_id"
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET = "your_storage_bucket"
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID = "your_messaging_sender_id"
NEXT_PUBLIC_FIREBASE_APP_ID = "your_app_id"
NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID = "your_measurement_id"
Replace every environment with the credentials listed in the firebaseConfig object.

Next, create a new firebase directory inside the project root folder.

Inside the firebase folder, create a file clientApp.ts.

We will configure the Firebase instance in clientApp.ts file, as demonstrated below:

Start by importing initializeApp from the Firebase package.

>import {initializeApp} from "firebase/app";

Call the initializeApp function and pass in your credentials as listed in the env.local file:

```
initializeApp( {
   apiKey:process.env.NEXT_PUBLIC_FIREBASE_API_KEY,
   authDomain:process.env.NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN,
   projectId:process.env.NEXT_PUBLIC_FIREBASE_PROJECT_ID,
   storageBucket:process.env.NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET,
   messagingSenderId:process.env.NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID,
   appId:process.env.NEXT_PUBLIC_FIREBASE_APP_ID,
   measurementId:process.env.NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID
});
```
Import getFirestore from firebase.

>import {getFirestore} from "firebase/firestore";

Create a Firestore instance.

>const firestore = getFirestore();

Export firestore so that it can be accessible by the files that we will create later in this project.

>export {firestore};

Since we have environmental variables, we will have to restart the development server.

Press ctrl + c to close it, and then npm run dev to start it.

//TODO: yet working ....!

Further readings

[firebase web setup](https://firebase.google.com/docs/web/setup)
[Next.js Firebase full course](https://fireship.io/courses/react-next-firebase/)
