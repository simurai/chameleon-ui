## Chameleon UI theme

> Warning: This is still experimental (see FAQ). Only use this theme together with the Chameleon syntax theme (see under Install).

A color shifting UI theme for Atom.

![Chameleon theme](https://cloud.githubusercontent.com/assets/378023/20452572/64e8d14a-ae50-11e6-8fb4-137d2e85ea1f.gif)


## Examples

Instead of using the color picker, you can also edit your `config.cson` file.

![Chameleon dark](https://cloud.githubusercontent.com/assets/378023/20453670/c7a97de2-ae6f-11e6-96bf-405f418cc90a.png)

```cson
"chameleon-syntax":
  color:
    ac: "#49ff94"
    bg: "#383747"
    fg: "#7093a8"
```


![Chameleon dark brown](https://cloud.githubusercontent.com/assets/378023/20453672/d05a6410-ae6f-11e6-9778-283a9ce1a13b.png)

```cson
"chameleon-syntax":
  color:
    ac: "#ffc465"
    bg: "#36302d"
    fg: "#71966c"
```


![Chameleon light](https://cloud.githubusercontent.com/assets/378023/20453674/d644d504-ae6f-11e6-8d38-3d3dec2c902b.png)

```cson
"chameleon-syntax":
  color:
    ac: "#5a5aff"
    bg: "#fffcf9"
    fg: "#8c847b"
```


### Install

This theme isn’t published. But you can still try it out by installing it from Atom’s settings. Go to __Settings > Install__ and then enter `simurai/chameleon-ui` and click on the "Themes" button. It should show a card with an "Install" button. Don’t forget to also install `simurai/chameleon-syntax` since they depend on each other.

Then switch to the "Themes" tab and pick **Chameleon** for both, UI and Syntax.


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

