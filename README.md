Simple app exemple showing how to upload image from gallery or from camera to Firebase with Firebase, AngularFire2-rc4 and Ionic 3.

<p align="center">
  <img src="https://j.gifs.com/Y693g0.gif" />
</p>

If you want test the project first type :
```
npm install
```
***Don't forget to change firebaseConfig in /src/app/app.module.ts***
```javascript
    export const firebaseConfig = {
      apiKey: 'YOUR_API_KEY',
      authDomain: 'YOUR_DOMAIN',
      databaseURL: 'YOUR_DATABASE_URL',
      storageBucket: 'YOUR_STORAGE',
      messagingSenderId: "YOUR_MSGINGID"
    };
```  
Make sure you have installed the Android SDK

Then install platform with
```
ionic cordova platform add android
ionic cordova run android
```
or make sure you have installed Xcode

```
ionic cordova platform add ios
ionic cordova run ios
```
You need to turn on anonymous login in your Firebase console in order to test it or change `firebase.auth().signInAnonymously()` from `src/pages/home/home.ts` to `firebase.auth().signInWithEmailAndPassword('newuser@mail.com', 'password')` or whatever signIn method you want.
