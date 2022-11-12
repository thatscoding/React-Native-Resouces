# React-Native-Resouces

## Project setup 
 ###  npx create-expo-app AwesomeProject

 ###  cd AwesomeProject
 ###  npm start 
  
  ## Tailwind Setup
  
  ##    https://www.nativewind.dev/quick-starts/react-native-cli
  
  ###  npm i nativewind
  ###  npm i --dev tailwindcss
  ###  npx tailwindcss init
  
# Step-2

// tailwind.config.js

/** @type {import('tailwindcss').Config} */

module.exports = {
   content: ["./App.{js,jsx,ts,tsx}", "./src/screens/**/*.{js,jsx,ts,tsx}","./src/components/**/*.{js,jsx,ts,tsx}" ],

  theme: {
    extend: {},
  },
  plugins: [],
}

 
 # Step-3
 
// babel.config.js
module.exports = function (api) {
  api.cache(true);
  return {
    presets: ["babel-preset-expo"],
+   plugins: ["nativewind/babel"],
  };
};


## React Navigation
https://reactnavigation.org/docs/getting-started/

###   npm install @react-navigation/native
###   npx expo install react-native-screens react-native-safe-area-context
###    npm install @react-navigation/native-stack


// In App.js in a new project

import * as React from 'react';
import { View, Text } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';

function HomeScreen() {
  return (
    <View style={{ flex: 1, alignItems: 'center', justifyContent: 'center' }}>
      <Text>Home Screen</Text>
    </View>
  );
}

const Stack = createNativeStackNavigator();

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}

export default App;


  # Heroicons & SVG
  npm i react-native-heroicons react-native-svg

### Usage

import { SparklesIcon as SparklesIconOutline } from "react-native-heroicons/outline";
// ...
<SparklesIconOutline color="red" fill="black" size={42} />;


#Vector icons for react native

### https://oblador.github.io/react-native-vector-icons/

npm i react-native-vector-icons

import Icon from "react-native-vector-icons/FontAwesome5";
<Icon name="directions" size={15} color="green" />


