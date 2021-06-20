# Firebase Guide

I am making this application using a short YouTube video, but I do not want to have to rewatch the video each time, so I will go ahead and document stuff here.

## Setup

### Create project and install tools
```npx create-react-app {appname}```
```code {appname}```
``` npm install firebase react-firebase-hooks```

### Import tools to app.js
Delete most of the boiler plate then import the following in the app.js file

Firebase SDK
```
import firebase from 'firebase/app';
import 'firebase/firestore';
import 'firebase/auth';
```

Firebase Hooks
```
import {useAuthState} from 'react-firebase-hooks/auth';
import {useCollectionData} from 'react-firebase-hooks/firestore';
```

### On Firebase
1. Use the firebase console to create a new project
2. Enable the authentication you would like
3. Enable a database (I started in production mode, but you do you)
4. Setup a javascript web app, ignore hosting for the time being. Copy the values into the app.js file
What to copy:
```
apiKey: "AIzaSyAGcBV10o4u-XeSwNF1U306C60Q49nJu5s",
authDomain: "superchat-18caf.firebaseapp.com",
projectId: "superchat-18caf",
storageBucket: "superchat-18caf.appspot.com",
messagingSenderId: "566867100496",
appId: "1:566867100496:web:e0c136c02add83212d6255"
```

### Scroll into view tip
create a ref to a component and then scroll into view will automatically scroll the page to that reference!!!, that is huge

```<div ref={dummy}></div>```
```const dummy = useRef()```
```dummy.current.scrollIntoView({behavior: 'smooth'});```
