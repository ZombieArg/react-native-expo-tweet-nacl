# React Native Expo Tweet NaCl [<img src="https://www.tomsquest.com/img/posts/2018-10-02-better-npm-ing/npm_logo.png" width="50"/>](https://www.npmjs.com/package/tweet-nacl-react-native-expo)

### This package is a Fork from @rajtatata [repo](https://github.com/rajtatata/react-native-expo-tweet-nacl) that contains modified files from [TweetNaCl.js](https://github.com/dchest/tweetnacl-js) that work with react native expo

#### The original repo from @rajtatata is using `expo-random` that is deprecated and the current available library to generate randomBytes it's `expo-crypto`. The intention of this package is to create an up to date implementation of React Native Expo Tweet NaCl.

##### Example App: [Tweet NaCl Demo (React Native Expo)](https://github.com/ZombieArg/react-native-tweet-nacl-expo-example)
##### Tweet NaCl documentation: [TweetNaCl.js Docs](https://github.com/dchest/tweetnacl-js#documentation)

# Modifications

-  Modified nacl-fast.js in order to replace the method for generating random bytes

- Used [getRandomBytesAsync](https://docs.expo.dev/versions/latest/sdk/crypto/#cryptogetrandombytesasyncbytecount) from [expo-crypto](https://docs.expo.dev/versions/latest/sdk/crypto/) in order to generate random bytes

- Since getRandomBytesAsync is async the following methods have become async
    - nacl.randomBytes
    - nacl.box.keyPair
    - nacl.sign.keyPair
    - nacl.sign.keyPair.fromSeed

- nacl-util.js contains useful functions to encode/decode UTF8 and Base64

#