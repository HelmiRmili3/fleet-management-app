# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started


##

App configuration create this file "app.config.ts" in route folder of your the app 


past this code :


import { ConfigContext, ExpoConfig } from "@expo/config";
import "dotenv/config";

export default ({ config }: ConfigContext): ExpoConfig => {
  const APP_IP_EMULATOR_DEVICE = "10.0.2.2";
  const APP_IP_REAL_DEVICE = "172.27.128.1";
  const BASE_URL = `http://${APP_IP_EMULATOR_DEVICE}:8000/api/v1`;

  return {
    ...config,
    name: "MyApp",
    slug: "my-app",
    extra: {
      API_URL: process.env.API_URL || "https://default-api.com",
      APP_ENV: process.env.APP_ENV || "development",
      APP_IP_EMULATOR_DEVICE,
      APP_IP_REAL_DEVICE,
      APP_STORAGE_URL: `http://${APP_IP_EMULATOR_DEVICE}:8000/storage`,
      BASE_URL,
    },
  };
};





##

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.
