### Continuous Integration with Travis CI

[![Build Status](https://travis-ci.org/WeRockStar/AndroidTravisCI.svg?branch=master)](https://travis-ci.org/WeRockStar/AndroidTravisCI)

``` yml
language: android
jdk: oraclejdk8
env:
  matrix:
    - ANDROID_TARGET=android-24 ANDROID_ABI=x86
android:
  components:
  - platform-tools
  - tools
  - build-tools-24.0.3
  - android-24
  - extra-google-m2repository
  - extra-android-m2repository

script:
  # Unit Test
  - ./gradlew test
```