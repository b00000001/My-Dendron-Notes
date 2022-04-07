---
id: aqC9hgjcukewMHrV47bVC
title: AppSetup
desc: ''
updated: 1642224856739
created: 1642224590036
---

1. Create a new project
2. install typescript `npm install typescript`
3. run tsc --init to create a tsconfig file.
4. edit tsconfig (generally edit outdir as this will determine what directory your compiled files are placed in the naming convention is generally dist/. Also edit sourcedir, this will pinpoint where your source files are located.)
5. run [tsc](https://www.typescriptlang.org/docs/handbook/compiler-options.html) to compile your source files or run tsc -w to have compiler run in watch mode.

[[Back|Typescript]]
