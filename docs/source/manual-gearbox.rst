Manual Gearbox
===================================

Inside the Manual Gearbox you have a wide range of customization options to make LC work better for you. This is also where you can reveal advanced sliders and handles in the Add-on UI and 3D viewport.

..  figure:: img/IMG_ManualGearbox.jpg
    :alt: Manual Gearbox UI
    :class: with-shadow
    :width: 350px
    :align: center
    
    *The Manual Gearbox in the N-Panel* 


.. _rig-setup-mode:
Garage Mode
-----

.. image:: gif/DOC_GarageMode.gif
    :alt: Garage Mode Gif
    :class: with-shadow
    :width: 600px
    :align: center
|

Changing the mode to Garage Mode will get your vehicle ready for new tires, change track width or other model changes.
In the "Garage" all animations will be disabled temporarily and the vehicle is moved to the center of the scene. Blender also enters "Local View", so all other objects will be temporarily hidden until you go to "Race Mode" again.

Body, Wheel, Brake, Headlight and Steering Wheel attachment bones and setup controls for wheel-base length, track-width length, wheel radii, and roll center can be found in this mode. Enter "Pose Mode" and select and move the handles to start adjusting.
You can manually parent meshes, nulls and armatures to the body or wheels. 

.. note::
    The vehicle will temporarily be put into the center of the scene and all animations disabled. All animations will be restored when "Race Mode" is entered again.  

|
*Reset all!*
Will reset all LC properties for the active vehicle to their default value.

|
.. _view:
View
-----

The View Panel has options for what will be shown in the 3D View over and around the Vehicle.

..  figure:: img/IMG_View_02.png
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *View Panel in the Manual Gearbox UI* 

|
.. _enable_extra_handles:
Expanded UI
^^^^^^^^
Enables extra :ref:`animation-handles` and Sliders in the 3D view above and around the vehicle.

..  figure:: img/IMG_ExtraAnimationHandles02.jpg
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Add Extra Handles to control more things!* 

|
.. _enable_camera_hooks:
Camera Hooks
^^^^^^^^
Shows two Camera Hooks hovering above the active vehicle. Go into "Pose Mode" to select them and parent your camera to them.
The "Follow Cam" will track the general motion of the vehicle without taking the suspension into account, while the "Mounted Cam" will be attached to the body of the vehicle, following its every move

Alternatively, you can create hooked cameras with 1 Click in the :ref:`cameras` section.

..  figure:: img/IMG_CamHooks.jpg
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Attach your 3D Cams here* 

|
.. _enable_grid_viz:
Detection Grid
^^^^^^^^
Turn the visibility of the :ref:`ground-detection` debug grid ON/OFF.

..  figure:: img/IMG_DetectionGrid.jpg
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Useful for Debugging the Ground Detection* 

|
.. _enable_acc_viz:
G-Force Visualizer
^^^^^^^^
Enable an G-Force Visualizer in the viewport to see the force calculated and used by the :ref:`real-time-physics`.

..  figure:: gif/GIF_G-Force.gif
    :alt: Custom Physics
    :class: with-shadow
    :width: 350px
    :align: center

    *The G-Forces which are working on the vehicle*

|
.. _enable_vel_viz:
Velocity Visualizer
^^^^^^^^
Enable a Velocity Visualizer in the viewport to see the velocity calculated and used by the :ref:`real-time-physics`.

..  figure:: img/IMG_VelViz.jpg
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *The Velocity of the vehicle*

|
.. _settings:
Settings
-----

The Settings Panel controls how the :ref:`ground-detection`, :ref:`animation-handles`, Driving Path behave. You can also enter ":ref:`rig-setup-mode` here to adjust the vehicle and add new meshes to it.

..  figure:: img/IMG_Settings.jpg
    :alt: Settings
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Settings Panel in the Manual Gearbox UI* 

|
Update Driving Path
^^^^^^^^
See: :ref:`update-driving-path`

.. _snap-driving-path:
Snap Driving Path
^^^^^^^^
Automatically snap the Control Points of the Driving Path to the Ground Detection Meshes.

..  |pic1| image:: img/IMG_SnapOFF.jpg
    :alt: View
    :class: with-shadow
    :width: 48%


..  |pic2| image:: img/IMG_SnapON.jpg
    :alt: View
    :class: with-shadow
    :width: 48%

|pic1| |pic2|

*Driving Path Snap OFF and ON. A quick way to match the path to the ground.* 


.. note::
    The threshold for the vehicle detecting the ground is 4 m. If the vehicle is further away than this, it will instead stick to the path.


|
.. _ground-colliders:
Ground Colliders
^^^^^^^^

..  figure:: img/IMG_GroundColliders.png
    :alt: Colliders
    :class: with-shadow
    :width: 350px
    :align: center
    
    *List of meshes contributing to the Ground Detection* 

Launch Control uses automated :ref:`ground-detection`.
To make any mesh contribute to the ground detection you can either add it to the collection "LaunchControl -> GroundDetection" or simply select it, and hit the "+ Add Selected" button.
To remove a mesh, select it and hit the "- Remove Selected" button. 
The "x" button removes all meshes from the Ground Collders list.

|
.. _detection-grid:
Detection Grid
^^^^^^^^
See: :ref:`enable_grid_viz`

|
.. _detection-resolution:
Resolution
^^^^^^^^
Change the resolution of the detection grid which is projected onto the geometry inside the "Ground Detection" collection.

..  |pic3| image:: img/IMG_Res_01.jpg
    :alt: View
    :class: with-shadow
    :width: 48%

..  |pic4| image:: img/IMG_Res_02.jpg
    :alt: View
    :class: with-shadow
    :width: 48%

|pic3| |pic4|
    
*Detection Resolution 1 for smooth motion, 2+ for detailed motion* 

|
.. _use-true-ground:
Use True Ground
^^^^^^^^
Use the actual objects inside the collection 'GroundDetection', instead of a projected grid. This can be useful for complex loops or twisting roads built of 1 solid mesh.

..  figure:: img/IMG_TrueGround.jpg
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Use actual meshes for Ground detection* 

.. warning::
    Will generally give a visually worse result and can introduce 'flickering' in the detection on 'layered' surfaces.

|
.. _legacy-ground-detection:
Legacy Ground Detection
^^^^^^^^
By default LC will use an updated model for the ground detection. This model works better with banked surfaces and erratically bumpy surfaces. Disable to get the old ground detection back.


|
.. _limit-sliders:
Limit Animation Sliders
^^^^^^^^
To allow full control all the Viewport UI sliders can be "unlocked" so you can over-crank them and get whatever craziness you want.

..  |pic5| image:: img/IMG_LimitOn.jpg
    :alt: View
    :class: with-shadow
    :width: 48%
    

..  |pic6| image:: img/IMG_LimitOff.jpg
    :alt: View
    :class: with-shadow
    :width: 48%

|pic5| |pic6|
    
*Default: Locks the sliders inside the best range, check to unlocks the sliders* 

|
.. _wheel-shake-rate:
Wheel Shake Rate
^^^^^^^^
How fast the wheel shake is. Higher value produces faster shake.



|
.. _dcc-bridge:
DCC Bridge (Pro Feature)
------

The DCC Bridge streamlines the exporting workflow for studios and manufacturers when needing to pipe the Launch Control animation data into other 3D software.
Set the Export Path and select the File Format you need from the dropdown and LC is ready to export. The vehicle will be exported with animation subframes by default. This can be altered by expanding the "Settings".

..  figure:: img/IMG_DccBridge.jpg
    :alt: DCC Bridge
    :class: with-shadow
    :width: 350px
    :align: center
    
    *DCC Bridge Panel in the Manual Gearbox UI* 

Export Path:
    * Set the path as desired. Leaving it blank will export the file as "*vehicle_name*.FORMAT" relative to the saved .blend file.

File Format:
    * Export to Alembic, FBX, USD, glTF, UE5 Skeletal Mesh (FBX), Datasmith or a Baked Blend File

Settings:
    * Check to show the extra export settings

Animation Subframes (inside Settings):
    * LC exports the amount of subframes per frame of animation indicated here. The fewer subframes, the faster. Too few subframes can cause reverse-spinning wheels. For some file formats this is not supported and the animation will instead be exported in slow motion to avoid issues.

Quality (inside Settings):
    * Export either the Full Mesh in the scene or the Generated Proxy. This can be useful for working with a :ref:`lp-hp-workflow`

Apply Transforms (inside Settings):
    * Applying Transforms can fix transform issues in the exported data. It's always best to manually apply all scales and rotations before attempting to export.

Include (inside Settings):
    * Whether to include on the Active Vehicle or the Full Scene in the exported data.



UE5 Skeletal Mesh Exclusive Settings:

Create Unreal Asset (inside Settings):
    * Select to export both the Mesh data and Animations to the FBX or only the Animation data. This is useful when importing to UE, "Animation Only" will add just the animation assets, reducing import time compared to "Mesh and Animation".


.. note::
    "Rebase bones" are exported with the rig, which can be used inside UE5 to bind static meshes to the exported LC rig.



|
.. _lp-hp-workflow:
LP to HP Workflow
------

When working with manufacturers datasets, performance can suffer a lot. It can be next to impossible to handle all the data during animation, so it's often better to use a proxy model for the animation and then relink the High Quality data in the end before rendering.
Depending on which software the animation will be rendered in, this process will be slightly different.

For Cinema4D, 3Ds Max, Houdini or Maya:
Export a proxy (LP) version of the vehicle using the .abc format from the ":ref:`dcc-bridge`". If rigging was done using the ":ref:`cad-data-setup`", the origins should stay consistent and you can parent the nulls containing the HP wheels, HP brake calipers and HP body to the corrosponding LP wheels, brake calipers and body.


For Unreal Engine 5.2:
Export a proxy (LP) version of the vehicle using the "UE5 Skeletal Mesh (FBX)" format from the ":ref:`dcc-bridge`". Thanks to "Rebase bones" inside the Launch Control rig, it's possible to connect Static Meshes from inside UE5 to the imported LP Skeletal Mesh.



|
.. _proxy-tool:
Proxy Tool (Pro Feature)
------

The Proxy tool is used to automatically create a proxy of the vehicle model for faster playback in the viewport.

Proxy:
    * Show only the Generated Proxy model in the viewport

Full Mesh:
    * Show only the full Mesh in the viewport

Overlay:
    * Show both the Proxy and the Full Mesh in the viewport


|
.. _quick-export:
Quick Export
------

The Quick Export handles export of the animation to other DCCs such a Unreal Engine, Omniverse, Cinema 4D, Maya, and more. It can also export a baked Blend file for render farms.

..  figure:: img/IMG_QuickExport.jpg
    :alt: Quick Export
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Quick Export Panel in the Manual Gearbox UI (Datasmith Export is no longer available)* 

Export Path:
    * Set the path as desired. Leaving it blank will export the file as "*vehicle_name*.FORMAT" relative to the saved .blend file.

Animation Subframes:
    * LC exports the amount of subframes per frame of animation indicated here. The fewer subframes, the faster. Too few subframes can cause reverse-spinning wheels.



FBX Exclusive Settings:

Include Ground Colliders:
    * Includes all the ground detection meshes in each of the exported file.

Include Animations:
    * When checked, LC will export the meshes, the rig and animations. When unchecked, LC will only export the meshes and the rig.

Only Animations:
    * When checked, LC will NOT export the meshes, which results in much faster export speeds. However, it will still export the rig and the animations. 
This is especially useful when importing to Unreal Engine, where the "Only Animation FBX files" will be read as animation assets, which fit a previously exported "skeletal mesh" (an FBX with the meshes and the rig)


.. note::
    "Rebase bones" are exported with the rig, which can be used inside UE 5.3 to bind static meshes to the exported LC rig.


.. warning::
    UE 5.4+ causes animation jitter on imported FBX skeletal meshes due to Bone Compression. This can be fixed by changing the "Bone Compression Settings" inside the "Animation Sequence Object -> Asset Details -> Compression -> Bone Compression Settings" to the "DefaultRecorderBoneCompression".

|
.. _headlights:
Headlights
-----

The Headlights Panel help you quickly adjust and render Headlight Beams in front of the vehicle

.. note::
  Only Beams are set up here, not any emitting lamps or meshes inside the headlight geometry.

..  |pic7| image:: gif/GIF_Headlights.gif
    :alt: Headlights
    :class: with-shadow
    :width: 48%

..  |pic8| image:: img/IMG_Headlights.jpg
    :alt: Headlights
    :class: with-shadow
    :width: 48%

|pic7| |pic8|
    
*Headlights Panel in the Manual Gearbox UI* 

Headlights will automatically be rigged if detected in the model. If not, you can manually parent them to the "body" of the vehicle.

Different texture presets can be picked for the light beam. Low Beam and High Beam can be toggled and more settings can be dialed in.


|
.. _skidmarks:
Skidmarks
-----

The Skidmarks Panel helps you generate skidmarks from the tires of the vehicle.

.. note::
  Skidmarks currently only support pressure to calculate the intensity. Wheel-spin or Wheel-locking does not currently affect the generated Skidmarks

..  |pic9| image:: gif/GIF_Skidmarks.gif
    :alt: Skidmarks
    :class: with-shadow
    :width: 48%

..  |pic10| image:: img/IMG_Skidmarks.jpg
    :alt: Skidmarks
    :class: with-shadow
    :width: 48%

|pic9| |pic10|
    
*Skidmarks Panel in the Manual Gearbox UI* 



|
.. _jump-trajectories:
Jump Trajectory
-----

With the Jump Trajectory Panel, you can generate a realistic jump path for your vehicle.

..  |pic11| image:: gif/GIF_Jump.gif
    :alt: Jump
    :class: with-shadow
    :width: 48%

..  |pic12| image:: img/IMG_JumpGenerator.jpg
    :alt: Jump
    :class: with-shadow
    :width: 48%

|pic11| |pic12|
    
*Jump Trajectory Panel in the Manual Gearbox UI* 

Calculates spline-points of a realistic car jump depending on the input speed. 

To use it, go into edit-mode on the "DrivingPath" and select the last point, which has to be the very end of the "ramp" the car is going to jump from. This last point needs to have a handle. The angle of the handle will be the take-off angle and the "Jump Speed" (Speed of the car at take-off point) must be defined in the Add-on UI. If you prefer Imperial Units, you can check the check-box in the Add-on UI. The calculation will always expect the end of the jump is on Z=0. 


|
.. _cameras:
Cinematographer
-----

The Cinematographer Panel will help you quickly set up Cameras for your Animation.

..  figure:: img/IMG_CamSetup.jpg
    :alt: View
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Using the Cinematographer panel to quickly create cameras*


Click the "Follow Camera" or "Mounted Camera" to generate a camera from the 3D view hooked to the active vehicle.
The "Follow Camera" will track the general motion of the vehicle without taking the suspension into account, while the "Mounted Camera" will be attached to the body of the vehicle, following its every move


|
.. _rig-info:
Rig Info
-----

The Rig Info Panel will show you if the rigged vehicle which is currently active is compatible with the version of the Launch Control Addon you have installed.

..  figure:: img/IMG_RigInfo.jpg
    :alt: Rig Info
    :class: with-shadow
    :width: 350px
    :align: center
    
    *Rig Info Panel in the Manual Gearbox UI* 

You can also "Update Vehicle Rig" to automatically unrig your 1.5+ vehicle and rig it with the rig armature that matches the installed version of LC. 
In the process, LC will store the animtion data, driving path, ground detection, all the physics settings and rig setup settings and apply them after the re-rigging is done. 
Depending on the versions some data might not be possible to apply, so expect loss of data if you are updating an old file.

If you have a file with a "Legacy Rig" (Rigged in LC 1.0-1.3), you can try to "Update Vehicle Rig" too, but the successrate will be lower.

If a new version of the Launch Control Add-on is available, a box will pop up here notifying you about this. You can either pick to "Ignore" and not get this notification anymore, or head "To Download Page" to update your version of the add-on. Make sure you are logged into the selected download page and that you picked the right page inside the Add-on Preferences for Launch Control.