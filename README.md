# DXFX 1
It's a simple browser based overlay with editable capabilities.

![screenshot](https://raw.githubusercontent.com/cssmfc/dx1/main/dx1.png)

The purpose of this project was to use it as browser based overlay in OBS Studio.
Two web pages using **broadcast channel** (reference info here [Broadcast Channel API MDN](https://developer.mozilla.org/en-US/docs/Web/API/Broadcast_Channel_API) ).

## Functionality (windows OS)*
**How it works?**
First of all, the overlay is showing a [bottom bar](https://cssmfc.github.io/dx1/browser-overlay.html) with 3 editable text elements. For the sake of rendering the best quality over live stream, the bottom bar and text elements are part of a single SVG
Because it is a pain in the ass to make editable text in SVG (don't try `contenteditable="true"` ([reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable) because it doesn't work will go with the next best thing, `javascript`
The second html file named [panel.html](https://cssmfc.github.io/dx1/panel.html) has the options to interact with browser overlay mentioned above via **broadcast channel** API 
Bottom line (because I'm not good at explaining stuff) texts from one web page can be changed from another web page.
Based on this functionality and due to the fact that **OBS Studio** [reference](https://obsproject.com/download) is flexible enough, we can use the bottom bar overlay in live stream and panel as controller in custom browser Docks

## Install & Use
Both online and offline versions work pretty good. Emmm... yes, you can use the sources as they are right now in this repository, or you can download both HTML files on your device.
1. Open OBS and add a new Browser Source (local file if you go with this option, or copy the url of the [browser-overlay.html](https://cssmfc.github.io/dx1/browser-overlay.html) ) and add the source.
2. Go to **View** tab (OBS navigation bar at the top) go to **Docks** , select **Custom Browser Docks...** . When the box pops up, in the first field type a name, in the second box paste the URL of the [panel.html](https://cssmfc.github.io/dx1/panel.html) . Click Apply  after you see a new panel with some options inside.  Drag the panel and dock it wherever you want in OBS (sides or next to auto mixer panel... up to you)
3. Type text in panel fields and click the **View** button to see changes in browser overlay.  

**Panel**
- input text fields 
- view button to apply changes
- hide button to toggle the bar on/off
- skin 1/ skin 2 are options to swap between svg colors

Each time an interaction is made in Panel, to apply those changes, click the View button.
That's it.

## To do
- [ ]  make those side icons able to change... 
- [ ]  add option to swap between multiple SVGs
- [ ]  add option to change color of the font
- [ ]  add option to change font face

PS: a relatively cute version but image based (using HTML2PNG) can be found on [Tools CGC](https://toolscgc.camgirl.cloud/overlays/social-panel-overlay-maker-bottom-bar/)

__________________
(*) - MAC from what I know doesn't support OBS/Docker or something like that... a known issue 
