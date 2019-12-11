---
layout: post
title: /Notes/ PATH Environment Variable
---

_What in the heck is it?_

- Environment variables hold values related to the current environment, such as OS or user sessions
- The `PATH` environment variable specifies the directories in which executables are located on the machine
    - These can be started without knowing/typing the whole path to the file on the command line
    - on Mac, it usually holds all `bin` and `sbin` directories relevant for the current user
- In Windows and *nix, it's possible to create new environment variables whose values are then made available to all programs upon launch
- Installing Apache Maven:
    - Simple process of extracting the archive and adding the `bin` folder with the `mvn` command to the PATH