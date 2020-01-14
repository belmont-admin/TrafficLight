# Make a traffic light

## Introduction @unplugged

Use the micro:bit to build a traffic light

## Step 1 @fullscreen

Add a ``||basic:forever||`` block to that the traffic light will run forever

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

Add a ``||pins:digitalWritePin||`` block to light the Red LED on pin 0


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


