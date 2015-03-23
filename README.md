# Linkage Editor
This is a UI for making N-bar linkage systems with one degree of freedom and any number of rotary inputs. 

To try it out, first install [npm](https://www.npmjs.com/), clone this repository, then run:

```
$ sudo npm install
$ npm run-script build
```

Then open `index.html` with a browser (I've only tested in the lastest versions of Chrome). You should see a single, loney rotary input that looks like this:

![Image of basic linkage](http://i1077.photobucket.com/albums/w463/rjnevels/Screen%20Shot%202015-02-22%20at%208.53.07%20PM_zpskplyty5t.png)

Here are the controls so far:
* Press `space` to toggle pause
* When paused:
  * Click and drag a ground point to move it around
  * Some ground points are used as references for rotary inputs, so clicking and dragging them will change the phase the input
  * Hover over any bar*, and press `w` or `s` to change its length
  * To add an additional ground point connected to the linkage, click twice at different places on the background, then click on a point on the linkage
  * To add additional bars, click a bar, or on any two points on the linkage, then click once on the background
  * To add a new rotary input, hold down `r` and then click somewhere on the background
  * To select a rotary input, click the point that the bar is rotating around
* When unpaused:
  * Press `w` or `s` to increase or decrease the speed of a selected rotary input, or `t` to reverse its direction. If a rotary input is not selected, these changes in speed will apply to all of them.
  * To parts of the linkage, click on a point, then press `d`. Note that this only work if other parts of the linkage don't depend on the segments attached to the point.
  * To trace a point, click on the point, then press `space` to unpause

\* any bar except ones between rotary inputs and reference points

Rotary inputs will automatically reverse if they're about to put the linakge into an impossible configuration.

This is based from my [boilerplate](https://github.com/robz/boilerplate) repository.
