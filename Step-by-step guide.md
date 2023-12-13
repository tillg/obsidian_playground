Taken from [here](https://forum.obsidian.md/t/plugins-mini-faq/7737/25)
# A rough guide on getting started fiddling with plugins

-   Download [VS Code 13](https://code.visualstudio.com/) 
-   Set up [Node.js and NPM 23](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) **Done**: Node V17.8.-0 used with Node Version Manager nvm
-   Find a simple plugin on GitHub (the [sample plugin 20](https://github.com/obsidianmd/obsidian-sample-plugin) is a potential one, but it doesn’t really _do_ anything—maybe look for something that provides functionality similar to what you’d like to build) **Done** I will have a look at [Binary File Manager Plugin](https://github.com/qawatake/obsidian-binary-file-manager-plugin)
-   Download the plugin into a folder on your desktop [by _cloning_ it 8](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository) **Done**
-   Compile the downloaded plugin code
    -   Open your terminal
    -   Open the folder for the newly-downloaded plugin in the terminal (If you need help with the terminal, search the web for advice for your platform—the exact commands can be different depending on whether you’re using macOS/Windows/Linux/etc.
    -   Run `npm i` in the plugin folder
    -   Run `npm run dev` and the terminal will re-compile whenever the .ts file has changes saved
-   Open up the plugin’s folder in VS Code
-   Open the file `main.ts` and start changing things
-   Refer to the [Obsidian API 45](https://github.com/obsidianmd/obsidian-api) to understand what you can use
    -   In VS Code, you can hover over/select API elements and look up their definitions
-   Use `console.log(object)` or `console.log(variable)` to check the state/functioning of your plugin (see debugging below)
-   Drag the newly-created `main.js` and `manifest.json` files from the plugin folder into `Your-Vault/.obsidian/plugins/Some-Plugin-Folder`
-   (If loading the plugin for the first time, reload—or quit and relaunch—Obsidian)
-   (Unload and re)load the plugin in Obsidian’s Preferences → Community Plugins → the appropriate plugin toggle
-   Test it by invoking the features you’ve played with
-   Debug by using the Console tab in Obsidian’s Developer Tools (open dev tools with cmd/ctrl+shift+i, then select the console tab)