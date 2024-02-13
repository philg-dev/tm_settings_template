# Tampermonkey template for persistent settings

This is a little template project for anybody who is interested in having persistent settings for their Tampermonkey scripts.

It's made as an example project and stores values to the local storage of Tampermonkey using the `GM.setValue` and `GM.getValue` functionality.
It also comes with a very basic GUI to change and save those settings. The settings are loaded when the script runs after page load. If no settings have been saved, it will use hard-coded default values.

## Usage

In order to properly use the example project, you will need either the Tampermonkey or the Greasemonkey browser extension.
If you want to have the CSS separate from the Javascript, you might also want the Stylus browser extension.

- `./src/settings_template_standalone.user.js`
  - can be used with Tampermonkey and contains everything you need
  - when using this file, you don't need any of the other files
  - for more details what the files do read below
- `./src/settings_template.user.css`
  - can be imported in the Stylus extension
  - includes basic styles for a modular settings dialog and a fixed position for the cog wheel icon
- `./src/settings_template.user.js`
  - can be used with Tampermonkey
  - includes a well documented example for a basic infrastructure to save and load values from Tampermonkey's local storage
  - creates and adds the necessary DOM elements to display the settings
  - adds event handlers to interact with the settings panel
- both will be applied on `google.com` for test / demonstration purposes
  - a <span style="color:magenta">magenta</span> colored cog wheel icon will appear in the top left of `google.com`
  - the settings panel will resize to it's content
  - the modular dialog can be quit by clicking the background outside or the 'cancel' button