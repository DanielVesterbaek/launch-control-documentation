User Preferences
===================================
.. _user-pref:

The Launch Control User Preferences can be used to alter certain behaviour in the Add-on.


Interface
-------------

Vehicle Gallery
  Shows or Hides the Gallery with the preset vehicles in the Add-on UI.

Animation Gallery
  Shows or Hides the Gallery with the preset animations in the Add-on UI.

Slider Labels
  Shows or Hides Labels above all the Animation and Setup Sliders above the Vehicle inside the 3D View.



Animation
-------------

.. _custom_library:
Custom Library (LC Pro Only)
  Add a path to a Custom Animation Preset Library on your System or Network. Animation Presets can then be saved and loaded from this location.

.. _use-impertial-units:
Use Imperial Units
  Uses "MPH" instead of "KMH" for the :ref:`speedometer` and the :ref:`jump-trajectories`.



Speed Segments
-------------
.. _show-hotkeys:
Show Hotkeys
   Show the Hotkey table in the 3D Viewport

.. _auto-convert-timeline:
Auto Convert Timeline into Graph Editor
   Allow LC to automatically turn your timeline into a graph editor when the Speed Segment Tool is activated. This makes sure that you can preview and debug the animation curve while using the Speed Segments in the viewport

.. _max-frames:
Max Frames
  Limit the max amount of frames the Speed Segments will allow animating across. Increasing this might drastically decrease performance!

.. _key-movement-increments:
Key Movement Increments
   Performance Optimization: Move Speed Keyframes in the 3D viewport in increments of this value. Higher values increase performance but decrease precision

.. _target-fps:
Target FPS
   Performance Optimization: Throttle FPS to allow smooth updates when moving the Speed Keys

.. _handle-undo:
Handle Undo
   Performance Optimization: Disabled undos for Speed Segment operations to improve performance.



Physics
-------------
.. _show-postfx-with-live-physics:
Show PostFX (Physics Overdrive) with Live Physics
  Allow PostFX (Physics Overdrive) to be changed while using the Live Physics in LC



Rigging
-------------
.. _auto-tire-pivot:
Automatic Tire Pivot
  Let LC automatically create new pivots for the tire meshes used for rigging. The new pivots will override any user set pivots. Uncheck to keep user pivots.

.. _garage_transform:
Garage Transform
   Set the vehicle Transforms you want LC to use when entering 'Garage Mode'

.. _custom-tags:
Custom Tags
  Allow the user to define custom search tags that LC will search for when rigging the car.

.. _rig_brakes:
Rig Brakes
  Force, Skip or Rig only if possible. Set this to "Force" if the brake calipers do not get rigged!

.. _rig_headlights:
Rig Headlights
  Rig only if possible or Never.

.. _rig_wheel-covers:
Rig Wheel Covers (Fenders for F1 Vehicles)
  Force, Skip or Rig only if possible. Set this to "Force" if the objects do not get rigged!

.. _quick_tag_rename:
Quick Tag Rename
   Select what the Quick Tag Tool should rename when using before rigging




.. note::
    Remember to "Save Preferences" before exiting. 


