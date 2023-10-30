Launch Control Core
===================================
The Main Features part is split into 3 segments: "Rigging, Animation, and Physics".
Let's go over each of those here.


.. _rigging:
One-Click Rigging
------
LC uses :ref:`rigging-tags` to detect the parts of the vehicle. If the naming convention of the 3D model is supported by LC, the rigging can be done with one click. 

:ref:`quick-tag-tool` can be used to prepare unsupported 3D models to work with LC with a few clicks.

:ref:`custom-tags` can be used to optimize LC for your own naming convention.


.. _rigging-tags:
Rigging Tags
^^^^^^^^^^


If all required car parts are found, LC can rig the car.

Required car parts:
    * *Car Body*
    * *Front Right Wheel*
    * *Front Left Wheel*
    * *Rear Right Wheel*
    * *Rear Left Wheel*


If any of the optional car parts are found they will be rigged - If not, they will be ignored. This behavior can be changed inside "User Preferences -> :ref:`rigging-preferences`"

Optional car parts:
    * *Front Right Brake Caliper*
    * *Front Left Brake Caliper*
    * *Rear Right Brake Caliper*
    * *Rear Left Brake Caliper*
    * *Right Headlight*
    * *Left Headlight*


Multiple tags are being searched for when LC is detecting the objects. The full list for each object/location is:

    * **Wheels:**   *["Tire", "Wheel", "Wheels", "Tires", "Rad", "Räder", "tire", "wheel", "wheels", "tires", "rad", "räder", "tyre", "Tyre", "tyres", "Tyres"]*
    * **Body:**   *["Body", "body", "hull", "Hull"]*

    * **Brake:**   *["Brake", "brake", "Brakes", "brakes", "Calliper", "calliper", "Caliper", "caliper", "Callipers", "callipers", "Calipers", "calipers", "Bremse", "bremse"]*
    * **Headlight:**   *["headlight", "headlamp", "headbulb", "front_light", "front_lamp", "front_bulb", "front_emitter", "Headlight", "Headlamp", "Headbulb", "Front_light", "Front_lamp", "Front_bulb", "Front_emitter",]*

    * **Rear, Left:**   *["RL", "RearLeft", "BkL", "Bk.L", "Bk_L"]*
    * **Rear, Right:**   *[RR", "RearRight", "BkR", "Bk.R", "Bk_R"]*
    * **Front, Right:**   *["FR", "FrontRight", "FtR", "Ft.R", "Ft_R"]*
    * **Front, Left:**   *["FL", "FrontLeft", "FtL", "Ft.L", "Ft_L"]*


.. _quick-tag-tool:
Quick-Tag Tool
^^^^^^^^^^
You can quickly tag Car Parts that needs renaming to be compatible with LC using the Quick-Tag Tool. Select a Car Part (for instance the Car Body) in the viewport, and hit, "body", to tag the selected object as the body of your car. Do the same for wheels and the brake calipers and headlights if desired. 

"FL, FR, RL and RR" referes to the location of the car part and respectively means: "Front Left, Front Right, Rear Left and Rear Right".

..  figure:: img/IMG_QUICK_TAG_TOOL.jpg
    :alt: Quick-Tag Tool
    :class: with-shadow
    :width: 350px
    :align: center

    *The Quick-Tag Tool in the Interface* 


.. _native_lc_support:
Asset Packs for LC
^^^^^^^^^^

Many Vehicle models have supported naming conventions out of the box. Some Asset Packs that are natively supported are:
    * `Car Transportation <https://blendermarket.com/products/transportation>`_
    * `Car Teleporter <https://blendermarket.com/products/car-teleporter>`_
    * `Traffiq Car <https://blendermarket.com/products/car-library-traffiq-vehicles-for-blender>`_


.. _troubleshoot_rigging:
Troubleshoot Rigging
^^^^^^^^^^


Custom rigging and parenting can be done using the :ref:`rig-setup-mode`

.. _animation-presets:
Animation Presets
------

.. _user-path:
User Path
------

.. _real-time-physics:
Real-Time Physics
------

.. _postfx:
PostFX
------
