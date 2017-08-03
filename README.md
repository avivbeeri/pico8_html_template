# PICO8 Templage HTML file

**Supergood touch controls + standalone detection + offline-cache for your PICO8 games!**


## Live Demo: [PICO8 demo game!](https://headjump.github.io/pico8_html_template/)

[<img src="http://headjump.github.io/headjump_website/g/rockkid_demo.jpg">](https://headjump.github.io/pico8_html_template/)

Open it on your smartphone, it works great :)


## About and why

In my opinion [PICO8](https://www.lexaloffle.com/pico-8.php) is the perfect fit for mobile devices - with it's small resolution, input restrictions and good performance. The square screen leaves enough space for touch controls.

The existing HTML-export however, by the time of writing, doesn't come with touch controls. Also, the touch controls provided on the PICO8 site itself never really worked for me.


## File structure

The template file is a single HTML file with inline styles, javascripts and svg-images.

This is so you don't need additional tools to build the code or link a lot of files. I tried my best to provide a good code scructure and comments - so it should be easy to follow what is going on.

The only files you have to change are 'game.js' and 'icon.png' and add your game name to 'index.html'.


## Current limitations

The HTML template only supports the horizontal axis, only left and right. **No up and down.**

You will see in the embedded JS that the y-position for the touch input is already captured but not yet used for vertical input.

Why? - I want the touch controls to feel "perfect", but for vertical movement I haven't found a proper implementation yet. Feel free to help :)




## Tipps

If your game only uses a single button, you should only display a single button for the touch controls. Why confuse the user?

If your game is still under heavy development and you frequently update it, you should remove the link to the manifest-file in the html-tag until you are "done". Otherwise you have to update the manifest each time you want to test your game.


## iOS Tipps/Problems

Current iOS unfortunately reloads the page when used as webapp everytime you switch back to the the webapp from another app (while multitasking).

This means, your PICO8 game restarts everytime you switch back to the app. The only workaround at the moment is to save and restore the players progress within the game. At minimum you should save the current level number and accumulated score and restore it on gamestart (or give the player the option to continue the game).
