# Annoying Popups
Need to test what happens to your system or application when
popups happen?  This works pretty good!  And is very annoying!


## Getting Started
Simply clone down this repository, install dependencies, and get started on your application.

The use of the [yarn](https://yarnpkg.com/) package manager is **strongly** recommended, as opposed to using `npm`.

```bash
# create a directory of your choice, and copy template using curl
mkdir new-electron-webpack-project && cd new-electron-webpack-project
curl -fsSL https://github.com/electron-userland/electron-webpack-quick-start/archive/master.tar.gz | tar -xz --strip-components 1

# or copy template using git clone
git clone https://github.com/electron-userland/electron-webpack-quick-start.git
cd electron-webpack-quick-start
rm -rf .git

# install dependencies
yarn
```

## Stopping the annoying popups when they start
On Windows this can be especially challenging.  You will need to
open Task Manager (ctrl-alt-del) and show the expanded view.

Try to find "annoyingpopups" in the "background tasks" section.  You need to
try to catch it and end the task before it vanishes.  What fun!

Alternately, you can start the program via a shell script set to "wait"
(ex: ``START /wait annoyingpopups.exe ``).  If you kill the console window,
you kill the annoyingpopups process with it.

### Development Scripts

```bash
# run application in development mode
yarn dev

# compile source code and create webpack output
yarn compile

# `yarn compile` & create build with electron-builder
yarn dist

# `yarn compile` & create unpacked build with electron-builder
yarn dist:dir
```
