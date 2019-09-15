# ProPresenter-OBS

Uses the ProPresenter Stage Display websocket to feed current slide text into a OBS browser source lower third.

The original code was from https://github.com/cgarwood/ProPresenter-vMix and made for vMix.

In ProPresenter you must Enable Network and Stage Display App under preferences.  Set a password under Stage Display App.

Rename config.js.example to config.js and update the values to match your environment.  Use the port listed under Enable Network not the port under the Stage Display App. Use the password under Stage Display App.

In OBS, add a new browser source, check "Local File", navigate to index.html, then set width, height, and FPS to match your stream settings. Edit stylesheet.css to customize your lower thirds setup.

Set the slide notes to `no-obs` on a slide to prevent it from being sent to OBS (useful for slides with more text than you would want in a lower third).

Set the slide notes to `verse` on a slide with bible verses, and it will display the bible verse. In ProPresenter, if you have the bible verse broken out into newlines, you will see some very weird formatting. This is because the CSS expects the last line to be the to be the Book and Chapter. If you have the bible verse continue as a single line and let ProPresenter handle it rest, it works perfectly.
