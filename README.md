scratch-gui modified for use in [TurboWarp](https://github.com/catttttttggggggggg/20snail.github.io/releases) then modified for use in [PenguinMod](https://github.com/catttttttggggggggg/20snail.github.io/releases) then modified for use in [Snail IDE](https://github.com/catttttttggggggggg/20snail.github.io/releases) 😀

Snail IDE: https://github.com/catttttttggggggggg/20snail.github.io/releases is based on [Twemoji](https://github.com/catttttttggggggggg/20snail.github.io/releases) and is licensed under CC BY 4.0 https://github.com/catttttttggggggggg/20snail.github.io/releases   
## Setup
to run snail ide on your computer, you'll need nvm (node version manager).<br>
type ``nvm install 16`` then ``nvm use 16`` in your terminal. (if your on windows, accept the uac prompts)<br>
then your gonna need pnpm. there may be other ways to install snail ides dependencies without pnpm, but right now you'll need it. you can install it by typing ``npm install -g pnpm``. <br>
after you install pnpm, clone the snail ide gui with ``git clone https://github.com/catttttttggggggggg/20snail.github.io/releases``.<br>
then run ``pnpm i --shamefully-hoist``. after that, you can type ``npm start`` or ``pnpm start`` or ``yarn start`` if you have yarn.<br/>
if you want to use node 17+ , you'll have to add the enviroment variable `NODE_OPTIONS` with the content `--openssl-legacy-provider` before the start command.<br/>
on linux/github codespaces you can do that by running the command `export NODE_OPTIONS=--openssl-legacy-provider`.

## License

TurboWarp's modifications to Scratch are licensed under the GNU General Public License v3.0. See LICENSE or https://github.com/catttttttggggggggg/20snail.github.io/releases for details.

The following is the original license for scratch-gui, which we are required to retain. This is NOT the license of this project.

```
Copyright (c) 2016, Massachusetts Institute of Technology
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

https://github.com/catttttttggggggggg/20snail.github.io/releases is based on [Twemoji](https://github.com/catttttttggggggggg/20snail.github.io/releases) and is licensed under CC BY 4.0 https://github.com/catttttttggggggggg/20snail.github.io/releases
<!--

#### Scratch GUI is a set of React components that comprise the interface for creating and running Scratch 3.0 projects

## Installation
This requires you to have Git and https://github.com/catttttttggggggggg/20snail.github.io/releases installed.

In your own node environment/application:
```bash
npm install https://github.com/catttttttggggggggg/20snail.github.io/releases
```
If you want to edit/play yourself:
```bash
git clone https://github.com/catttttttggggggggg/20snail.github.io/releases
cd scratch-gui
npm install
```

**You may want to add `--depth=1` to the `git clone` command because there are some [large files in the git repository history](https://github.com/catttttttggggggggg/20snail.github.io/releases).**

## Getting started
Running the project requires https://github.com/catttttttggggggggg/20snail.github.io/releases to be installed.

## Running
Open a Command Prompt or Terminal in the repository and run:
```bash
npm start
```
Then go to [http://localhost:8601/](http://localhost:8601/) - the playground outputs the default GUI component

## Developing alongside other Scratch repositories

### Getting another repo to point to this code


If you wish to develop `scratch-gui` alongside other scratch repositories that depend on it, you may wish
to have the other repositories use your local `scratch-gui` build instead of fetching the current production
version of the scratch-gui that is found by default using `npm install`.

Here's how to link your local `scratch-gui` code to another project's `node_modules/scratch-gui`.

#### Configuration

1. In your local `scratch-gui` repository's top level:
    1. Make sure you have run `npm install`
    2. Build the `dist` directory by running `BUILD_MODE=dist npm run build`
    3. Establish a link to this repository by running `npm link`

2. From the top level of each repository (such as `scratch-www`) that depends on `scratch-gui`:
    1. Make sure you have run `npm install`
    2. Run `npm link scratch-gui`
    3. Build or run the repository

#### Using `npm run watch`

Instead of `BUILD_MODE=dist npm run build`, you can use `BUILD_MODE=dist npm run watch` instead. This will watch for changes to your `scratch-gui` code, and automatically rebuild when there are changes. Sometimes this has been unreliable; if you are having problems, try going back to `BUILD_MODE=dist npm run build` until you resolve them.

#### Oh no! It didn't work!

If you can't get linking to work right, try:
* Follow the recipe above step by step and don't change the order. It is especially important to run `npm install` _before_ `npm link` as installing after the linking will reset the linking.
* Make sure the repositories are siblings on your machine's file tree, like `.../.../MY_SCRATCH_DEV_DIRECTORY/scratch-gui/` and `.../.../MY_SCRATCH_DEV_DIRECTORY/scratch-www/`.
* Consistent https://github.com/catttttttggggggggg/20snail.github.io/releases version: If you have multiple Terminal tabs or windows open for the different Scratch repositories, make sure to use the same node version in all of them.
* If nothing else works, unlink the repositories by running `npm unlink` in both, and start over.

## Testing
### Documentation

You may want to review the documentation for [Jest](https://github.com/catttttttggggggggg/20snail.github.io/releases) and [Enzyme](https://github.com/catttttttggggggggg/20snail.github.io/releases) as you write your tests.

See [jest cli docs](https://github.com/catttttttggggggggg/20snail.github.io/releases) for more options.

### Running tests

*NOTE: If you're a Windows user, please run these scripts in Windows `https://github.com/catttttttggggggggg/20snail.github.io/releases`  instead of Git Bash/MINGW64.*

Before running any tests, make sure you have run `npm install` from this (scratch-gui) repository's top level.

#### Main testing command

To run linter, unit tests, build, and integration tests, all at once:
```bash
npm test
```

#### Running unit tests

To run unit tests in isolation:
```bash
npm run test:unit
```

To run unit tests in watch mode (watches for code changes and continuously runs tests):
```bash
npm run test:unit -- --watch
```

You can run a single file of integration tests (in this example, the `button` tests):

```bash
$(npm bin)/jest --runInBand https://github.com/catttttttggggggggg/20snail.github.io/releases
```

#### Running integration tests

Integration tests use a headless browser to manipulate the actual HTML and javascript that the repo
produces. You will not see this activity (though you can hear it when sounds are played!).

Note that integration tests require you to first create a build that can be loaded in a browser:

```bash
npm run build
```

Then, you can run all integration tests:

```bash
npm run test:integration
```

Or, you can run a single file of integration tests (in this example, the `backpack` tests):

```bash
$(npm bin)/jest --runInBand https://github.com/catttttttggggggggg/20snail.github.io/releases
```

If you want to watch the browser as it runs the test, rather than running headless, use:

```bash
USE_HEADLESS=no $(npm bin)/jest --runInBand https://github.com/catttttttggggggggg/20snail.github.io/releases
```

## Troubleshooting

### Ignoring optional dependencies

When running `npm install`, you can get warnings about optional dependencies:

```
npm WARN optional Skipping failed optional dependency /chokidar/fsevents:
npm WARN notsup Not compatible with your operating system or architecture: fsevents@1.2.7
```

You can suppress them by adding the `no-optional` switch:

```
npm install --no-optional
```

Further reading: [Stack Overflow](https://github.com/catttttttggggggggg/20snail.github.io/releases)

### Resolving dependencies

When installing for the first time, you can get warnings that need to be resolved:

```
npm WARN eslint-config-scratch@5.0.0 requires a peer of babel-eslint@^8.0.1 but none was installed.
npm WARN eslint-config-scratch@5.0.0 requires a peer of eslint@^4.0 but none was installed.
npm WARN scratch-paint@0.2.0-prerelease.20190318170811 requires a peer of react-intl-redux@^0.7 but none was installed.
npm WARN scratch-paint@0.2.0-prerelease.20190318170811 requires a peer of react-responsive@^4 but none was installed.
```

You can check which versions are available:

```
npm view react-intl-redux@0.* version
```

You will need to install the required version:

```
npm install  --no-optional --save-dev react-intl-redux@^0.7
```

The dependency itself might have more missing dependencies, which will show up like this:

```
user@machine:~/sources/scratch/scratch-gui (491-translatable-library-objects)$ npm install  --no-optional --save-dev react-intl-redux@^0.7
scratch-gui@0.1.0 /media/cuideigin/Linux/sources/scratch/scratch-gui
├── react-intl-redux@0.7.0
└── UNMET PEER DEPENDENCY react-responsive@5.0.0
```

You will need to install those as well:

```
npm install  --no-optional --save-dev react-responsive@^5.0.0
```

Further reading: [Stack Overflow](https://github.com/catttttttggggggggg/20snail.github.io/releases)

## Troubleshooting

If you run into npm install errors, try these steps:
1. run `npm cache clean --force`
2. Delete the node_modules directory
3. Delete https://github.com/catttttttggggggggg/20snail.github.io/releases
4. run `npm install` again

## Publishing to GitHub Pages
You can publish the GUI to https://github.com/catttttttggggggggg/20snail.github.io/releases so that others on the Internet can view it.
[Read the wiki for a step-by-step guide.](https://github.com/catttttttggggggggg/20snail.github.io/releases)

## Understanding the project state machine

Since so much code throughout scratch-gui depends on the state of the project, which goes through many different phases of loading, displaying and saving, we created a "finite state machine" to make it clear which state it is in at any moment. This is contained in the file https://github.com/catttttttggggggggg/20snail.github.io/releases .

It can be hard to understand the code in https://github.com/catttttttggggggggg/20snail.github.io/releases . There are several types of data and functions used, which relate to each other:

### Loading states

These include state constant strings like:

* `NOT_LOADED` (the default state),
* `ERROR`,
* `FETCHING_WITH_ID`,
* `LOADING_VM_WITH_ID`,
* `REMIXING`,
* `SHOWING_WITH_ID`,
* `SHOWING_WITHOUT_ID`,
* etc.

### Transitions

These are names for the action which causes a state change. Some examples are:

* `START_FETCHING_NEW`,
* `DONE_FETCHING_WITH_ID`,
* `DONE_LOADING_VM_WITH_ID`,
* `SET_PROJECT_ID`,
* `START_AUTO_UPDATING`,

### How transitions relate to loading states

Like this diagram of the project state machine shows, various transition actions can move us from one loading state to another:

![Project state diagram](https://github.com/catttttttggggggggg/20snail.github.io/releases)

_Note: for clarity, the diagram above excludes states and transitions relating to error handling._

#### Example

Here's an example of how states transition.

Suppose a user clicks on a project, and the page starts to load with URL https://github.com/catttttttggggggggg/20snail.github.io/releases .

Here's what will happen in the project state machine:

![Project state example](https://github.com/catttttttggggggggg/20snail.github.io/releases)

1. When the app first mounts, the project state is `NOT_LOADED`.
2. The `SET_PROJECT_ID` redux action is dispatched (from https://github.com/catttttttggggggggg/20snail.github.io/releases), with `projectId` set to `123456`. This transitions the state from `NOT_LOADED` to `FETCHING_WITH_ID`.
3. The `FETCHING_WITH_ID` state. In https://github.com/catttttttggggggggg/20snail.github.io/releases, the `projectId` value `123456` is used to request the data for that project from the server.
4. When the server responds with the data, https://github.com/catttttttggggggggg/20snail.github.io/releases dispatches the `DONE_FETCHING_WITH_ID` action, with `projectData` set. This transitions the state from `FETCHING_WITH_ID` to `LOADING_VM_WITH_ID`.
5. The `LOADING_VM_WITH_ID` state. In https://github.com/catttttttggggggggg/20snail.github.io/releases, we load the `projectData` into Scratch's virtual machine ("the vm").
6. When loading is done, https://github.com/catttttttggggggggg/20snail.github.io/releases dispatches the `DONE_LOADING_VM_WITH_ID` action. This transitions the state from `LOADING_VM_WITH_ID` to `SHOWING_WITH_ID`
7. The `SHOWING_WITH_ID` state. Now the project appears normally and is playable and editable.

## Donate
We provide [Scratch](https://github.com/catttttttggggggggg/20snail.github.io/releases) free of charge, and want to keep it that way! Please consider making a [donation](https://github.com/catttttttggggggggg/20snail.github.io/releases) to support our continued engineering, design, community, and resource development efforts. Donations of any size are appreciated. Thank you!

## e

-->
