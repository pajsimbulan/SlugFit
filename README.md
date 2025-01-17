# Slugfit
`Slugfit` is a fitness app inspired by the block-based UI of Notion. It's a cross-platform (iOS and Android) app built using React Native. The app is designed to cater to users with both some experience in fitness and to little to no experience.  It provides features for creating, saving, and editing workouts, as well as social interactions and workout analysis.

## Features
 - Create and manage workouts with a block-based UI
 - Add and edit exercises within workouts
 - Create user profiles with profile pictures
 - Social media features to view friends' workouts and add them to your own
 - Automatic workout sharing with friends
 - Workout analysis based on past performance
 - Integrated calendar to keep track of workouts
 - Built with `TypeScript`, `Figma` (UI), `Supabase` (PostgreSQL database), `Expo` (development), `Yarn` (package manager), and `StoryBook` + `Jest` (testing)
 <br /><br />

# Environment Setup
 - Install Node:
 - https://nodejs.org/en/download/
 - Install Yarn:
 - https://classic.yarnpkg.com/lang/en/docs/install/
 - Setup Supabase
 - https://supabase.com/
 <br /><br />

# App Installation
1. Clone this repository
2. Set githooks with `git config core.hooksPath ./.githooks`
3. Navigate to the root of the repository and run `yarn` to install all dependencies
4. Initialize your Supabase account. (https://supabase.com/)
5. Setup Supabase database by creating a file `environment.ts` and copy your very own `SupabaseURL key` and `SupabaseAnonKey` and paste it in this file 

```
/*****************************
 * environment.js
 * path: '/environment.js' (root of your project)
 ******************************/

import Constants from 'expo-constants';
import { Platform } from 'react-native';

// const localhost = Platform.OS === "ios" ? "localhost:8080" : "10.0.2.2:8080";

const ENV = {
  dev: {
    supabaseUrl: 'Your Supabase URL',
    supabaseAnonKey: `Your Supabase Anon Key`
  },
  staging: {
    supabaseUrl: 'Your Supabase URL',
    supabaseAnonKey: `Your Supabase Anon Key`,
  },
  prod: {
    supabaseUrl: 'Your Supabase URL',
    supabaseAnonKey: `Your Supabase Anon Key`,
  },
};

const getEnvVars = (env = Constants.manifest!.releaseChannel) => {
  // What is __DEV__ ?
  // This variable is set to true when react-native is running in Dev mode.
  // __DEV__ is true when run locally, but false when published.
  return ENV.dev;
  // if (__DEV__) {
  //   return ENV.dev;
  // } else if (env === "staging") {
  //   return ENV.staging;
  // } else if (env === "prod") {
  //   return ENV.prod;
  // }
};

export default getEnvVars;

```

4. Run `yarn start` to begin the development server
5. If you have XCode installed and an iPhone simulator, press `i` to open the simulator and run the app. Otherwise, install the Expo Go app on your phone and scan the QR code from the terminal with your camera to run the app on your phone in Expo Go. Make sure your phone and laptop are connected to the same Wi-Fi network to use the latter option.
<br /><br />

# Commands
 - `yarn start` to begin the development server
 - `yarn ios` to run iOS simulator
 - `yarn android` to run Android simulator
 - `yarn lint` to lint code
 - `yarn lint:fix` to fix simple linting errors
 - `yarn` format to format code according to style guide
 - `yarn test` to run unit tests
<br /><br />

# Figma Design 
Available to view with this link - https://www.figma.com/file/4CGETWt2tr1R8Sk35EiPHF/Slugfit_copy?node-id=0%3A1&t=HcRYZOTF8WiNvHja-1

<img src="./screenshots/figma_design.jpg" alt="Description of the screenshot" width="400px">
<br /><br />

# Architecture

<img src="./screenshots/slugfit_architecture.jpg" alt="Description of the screenshot" width="400px">
<br /><br />

# Screenshots
<div style="display: flex; flex-direction: row; flex-wrap: wrap;">

<figure style="display: flex; flex-direction: column; align-items: center;">

  <img src="./screenshots/signin.PNG" alt="Description of the screenshot" width="200px">
 
</figure>
<figure style="display: flex; flex-direction: column; align-items: center;">

  <img src="./screenshots/home.PNG" alt="Description of the screenshot" width="200px">
  
</figure><figure style="display: flex; flex-direction: column; align-items: center;">

  <img src="./screenshots/social_media.PNG" alt="Description of the screenshot" width="200px">
  
</figure><figure style="display: flex; flex-direction: column; align-items: center;">

  <img src="./screenshots/start_workout_card.PNG" alt="Description of the screenshot" width="200px">
</figure>
</div>

### **More screenshots available on the ./screenshots directory or visit https://paulsimbulan.com**

# Video Demo
<video width="600px" controls>
  <source src="./demovideo/slugfit_demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### if video doesn't load or show above, try this link https://youtu.be/2OFljDC_c74

# Contributing

Contributions are welcome! Please feel free to submit pull requests or create issues to report bugs or suggest improvements.

# License
This project is open-source and available under the MIT License.
