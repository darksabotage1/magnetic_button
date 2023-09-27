# Magnetic Button

The Magnetic Button is a custom Flutter widget that creates an interactive button with a "magnetic" effect. When you hover over the button, it moves in response to the mouse position, creating a unique and engaging user experience.

#### Platform Support

| Android | iOS | MacOS | Web | Linux | Windows |
| :-----: | :-: | :---: | :-: | :---: | :-----: |
|   ❓   | ❓  |  ✅   | ✅ |  ✅   |  ✅    |


![preview](https://github.com/darksabotage1/assets/assets/136040945/f1bb1ebf-2d10-4f20-badb-9f00e703e625)


## Untested Features

- **Mobile On-Hold Magnetic Effect(Undergoing Testing)**: We are currently in the testing phase for an on-hold magnetic effect specifically designed for mobile devices. This functionality is intended to enable buttons to maintain their movement in response to hold gestures, enhancing interactivity on mobile platforms."

## Features

- **Hover Effect**: The button moves in response to the mouse position when hovered over, creating a "magnetic" effect.
- **Return Duration**: When the mouse is not hovering over the widget, the button returns to its original position. The speed at which it returns is controlled by the `duration` property. This property is set in milliseconds, so a larger value will make the return slower, and a smaller value will make it faster.
- **Customizable**: You can customize the child widget of the Magnetic Button to fit your needs.
- **Max Movement**: You can control the maximum movement of the button in response to the mouse position using the mx and my properties.
- **Distance to Trigger**: A customizable parameter that determines the proximity at which an animation for a widget is initiated.

## Usage

1. Create a `MagneticButton` widget and pass in your desired child widget:

   ```dart
   Offset values = const Offset(0, 0);
   MagneticButton(
          duration: const Duration(milliseconds: 100),
          onChanged: (Offset value) {
            setState(() => values = value);
          },
          child: Container(
            decoration: BoxDecoration(
                borderRadius: const BorderRadius.all(Radius.circular(40)),
                color: Colors.white,
                border: Border.all(color: Colors.black)),
            width: 160,
            height: 80,
            child: Center(
              child: Transform.translate(
                offset: Offset(values.dx / 4, values.dy / 4),
                child: const Text(
                  'Explore',
                  style: TextStyle(
                    fontWeight: FontWeight.w400,
                    fontSize: 19,
                  ),
                ),
              ),
            ),
          ),
        ),

## Future Features

We have successfully integrated all the proposed features for the Magnetic Button, except ‘Mobile On-Hold Magnetic Effect’ feature, which is currently undergoing testing. At this point, we have no additional features planned for future implementation. However, we welcome feedback and suggestions from our users. If you have an idea for a feature that you’d like to see in Magnetic Button, please let us know! 🙂. 