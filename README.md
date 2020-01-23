# Make a traffic light

## Introduction @unplugged

In this session we're going to use the @boardname@ to build a traffic light

![STOP:bit](https://raw.githubusercontent.com/belmont-admin/TrafficLight/master/docs/static/trafficLight.png)

## Step 1 @fullscreen

Add a ``||basic:forever||`` block so that the traffic light will run forever

```blocks
basic.forever(() => {
})
```
Click **Advanced** to show the other types of blocks available. Expand the ``||pins:Pins||`` section and find the ``||pins:digitalWritePin||`` block.

### ~hint

#### Pins for the lights
* Pin 0 is the red light
* Pin 1 is the amber light
* Pin 2 is the green light

#### Values for on and off
* A value of 0 means Off
* A value of 1 means On

### ~

Add a ``||pins:digitalWritePin||`` block to switch on the red light connected to pin 0.


```blocks
basic.forever(() => {
    pins.digitalWritePin(DigitalPin.P0, 1);
});
```
## Step 2 @fullscreen

Connect your @boardname@, pair it and then use the ``||Download||`` button to send your code to the @boardname@ and check the red light turns on.

## Step 3 @fullscreen

Now add a ``||basic:Pause|`` block to wait for for half a second before turning the red light off again using another ``||pins:digitalWritePin||`` block.

```blocks
basic.forever(() => {
    pins.digitalWritePin(DigitalPin.P0, 1);
    basic.pause(500);
    pins.digitalWritePin(DigitalPin.P0, 0);
});
```
## Step 4 @fullscreen

Use the ``||Download||`` button to send your new code to the @boardname@ and check what happens. Was it what you expected? If it wasn't how can you fix it?

## Step 5 @fullscreen

Now write code so that your lights cycle through the standard traffic light sequence.

When you have finished don't forget to **save** your code.

![Traffic light animation](https://github.com/belmont-admin/TrafficLight/raw/master/docs/static/traffic-lights-min.gif)

## Step 6 @fullscreen

Improve your traffic lights by creating a **delay** variable using the ``||variables:set delay to||`` block so you can easily adjust the length of the ``||basic:pause||`` and alter how quickly the lights change. 

```blocks
let delay = 500
```
Make it so you can change the delay up and down using the A and B buttons.

```blocks
input.onButtonPressed(Button.B, function () {
    delay += 100
})
input.onButtonPressed(Button.A, function () {
    delay += -100
})
```

## Step 7 @fullscreen

Now see if you can use the ``||basic:showLeds||`` block to use the LEDs on the @boardname@ itself to add a pedestrian crossing animation.

Remember the @boardname@ is turned on its side so you'll need to rotate the pixels 90 degrees.

## Step 8 @fullscreen

If you're feeling adventurous then finally add a countdown as well. Here's a link to a video of what it might look like:

https://youtu.be/GEoKefzK3mk