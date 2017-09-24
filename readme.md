| README |
|:---|
![](https://github.com/zeit/art/blob/525bd1bb39d97dd3b91c976106a6d5cc5766b678/hyper/repo-banner.png)

For more details, head to: https://nanoofficial.github.io/xhype

## Usage

[Download the latest release!](https://nanoofficial.github.io/xhype/#installation)

If you're on macOS, you can also use [Homebrew Cask](https://caskroom.github.io/) to download the app by running these commands:

```bash
brew update
brew cask install xhype
```

If you're on windows, you can use [chocolatey](https://chocolatey.org/) to install the app by running the following command (package information can be found [here](https://chocolatey.org/packages/xhype/)):

```bash
choco install xhype
```

**Note:** The version available on [Homebrew Cask](https://caskroom.github.io/) or [Chocolatey](https://chocolatey.org) may not be the latest. Please consider downloading it from [here](https://nanoofficial.github.io/xhype/#installation) if that's the case.

## Contribute

Regardless of the platform you are working on, you will need to have Yarn installed. If you have never installed Yarn before, you can find out how at: https://yarnpkg.com/en/docs/install.

1. Install necessary packages:
  * Windows
    - Be sure to run  `yarn global add windows-build-tools` to install `windows-build-tools`.
  * macOS
    - Once you have installed Yarn, you can skip this section!
  * Linux
    - RPM-based
        + `GraphicsMagick`
        + `libicns-utils`
        + `xz` (Installed by default on some distributions.)
    - Debian-based
        + `graphicsmagick`
        + `icnsutils`
        + `xz-utils`
2. [Fork](https://help.github.com/articles/fork-a-repo/) this repository to your own GitHub account and then [clone](https://help.github.com/articles/cloning-a-repository/) it to your local device
3. Install the dependencies: `yarn`
4. Build the code and watch for changes: `yarn run dev`
5. To run `xhype`
  * `yarn run app` from another terminal tab/window/pane
  * If you are using **Visual Studio Code**, select `Launch xHype` in debugger configuration to launch a new xHype instance with debugger attached. 
 
To make sure that your code works in the finished application, you can generate the binaries like this:

```bash
yarn run dist
```

After that, you'll see the binary in the `./dist` folder!

#### Known issues that can happen during development

##### Error building `node-pty`

If after building during development you get an alert dialog related to `node-pty` issues,
make sure its build process is working correctly by running `yarn run rebuild-node-pty`.

If you're on macOS, this typically is related to Xcode issues (like not having agreed
to the Terms of Service by running `sudo xcodebuild` after a fresh Xcode installation).

##### Error with `codesign` on macOS when running `yarn run dist`

If you have issues in the `codesign` step when running `yarn run dist` on macOS, you can temporarily disable code signing locally by setting
`export CSC_IDENTITY_AUTO_DISCOVERY=false` for the current terminal session.

## Related Repositories

- [Images](https://github.com/nanoofficial/nano-Resources)
- [Website](https://github.com/nanoofficial/nanoofficial.github.io)
- [Sample Extension](/samples/extension)
- [Sample Theme](/samples/theme)

