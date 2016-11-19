## Chameleon UI theme

A color shifting UI theme for Atom.

> Warning: This is still experimental. Only use this together with the Chameleon syntax theme (see under Install).

![Chameleon UI theme](https://cloud.githubusercontent.com/assets/378023/20452091/96804838-ae45-11e6-8e72-917b5cfd6e43.gif)

### Install

This theme isn’t published. But you can still try it out by installing it from Atom’s settings. Go to __Settings > Install__ and then type `simurai/chameleon-ui` and hit enter. Don’t forget to also install `simurai/chameleon-syntax` since they depend on each other.

Then switch to the Themes tap and pick **Chameleon** for both, UI and Syntax.

### Settings

![Theme settings](https://cloud.githubusercontent.com/assets/378023/15923548/cb3dc7ce-2e68-11e6-8a51-10801fb483bf.png)

In the theme settings you can change the __Font Size__ to scale the whole UI up or down.

Switch between 3 __Layout Modes__:

1. `Auto` (default) - In Auto mode, the UI and font size will automatically change based on the window size.
2. `Compact` - The UI stays compact to leave more space for the editor.
3. `Spacious` - The UI is expanded, giving some breathing room.

And pick a __Tab Sizing__ mode:

1. `Auto` (default) - In Auto mode the tabs switch based on the window size.
2. `Minimum` - In Mimimum mode the tabs will be as small as possible.
3. `Even` - In Even mode all tabs will be the same size.

### Customize

It's also possible to resize only certain areas by adding the following to your `styles.less` (Use the DevTools to find the right selectors):

```css
.theme-chameleon-ui {
  .tab-bar { font-size: 18px; }
  .tree-view { font-size: 14px; }
  .status-bar { font-size: 12px; }
}
```

### FAQ

__Why isn’t this theme published?__
This theme is pretty experimental and not all packages get updated with the right colors.

By convention, Atom themes have to define a list of Less variables that other packages will use to make their package look consistent with the rest of the UI. This theme uses custom properties (CSS variables) for its colors which unfortunately aren’t compatible with Less variables.

You can certainly use it, but there might be issues where certain areas are red. See next question.

__I see red?__
If you see red somewhere it means that package still needs to be overridden. Feel free to make an issue, but no guarantee that it will be fixed everywhere.

