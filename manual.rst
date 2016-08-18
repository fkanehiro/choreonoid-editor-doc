=========================
 Choreonoid Model Editor
=========================

Architecture
============

Choreonoid model editor is realized as a plugin to extend the basic function of Choreonoid.

In Choreonoid, plugin developer can extend its function by defining new Items which appears in tree view of left panel.

Original Choreonoid only have "BodyItem" to load the simulation model. Choreonoid model editor adds "EditableBodyItem" which you can split the simulation model into joints and links, and change its properties.

From here, we explain each of those new Items.


EditableBodyItem
================

This item is created on top of all the items.

When you load your existing model, this item is created automatically.

Even when you create simulation model from scratch, you have to create this item and connect the other items as a child.


JointItem
=========

When you want to add a joint to your simulation model, you have to create this item as a child of EditableBodyItem or other joints.

After created, you can edit the property of the joint by double clicking the property panel.

translation
-----------

Specifies relative position with respect to the parent joint.


rotation
--------

Specifies relative rotation with respect to the parent joint.

Joint ID
--------

Specifies unique ID

Joint type
----------

Specifies type of joint from "free", "rotate", "slide", "fixed".

Joint axis
----------

Specifies direction of joint in [x, y, z] format.

Upper limit
-----------

Specifies upper limit of joint angle.

Lower limit
-----------

Specifies lower limit of joint angle.

Upper velocity limit
-----------

Specifies upper limit of joint velocity.

Lower velocity limit
-----------

Specifies lower limit of joint velocity.

Gear ratio
----------

Specifies gear ratio of this joint.

Rotor inertia
-------------

Specifies inertia of rotor of the motor which drives this joint.

Torque const
------------

Specifies torque constant of the motor which drives this joint.

Encoder pulse
-------------

Specifies the number of encoder pulse per round.


LinkItem
========

When you want to add a link to your simulation model, you have to create this item as a child of JointItem.

After created, you can edit the property of the link by double clicking the property panel.

Mass
----

Specifies mass.

Center of mass
--------------

Specifies location of mass center in [x, y, z] format.

Inertia
-------

Specifies moment of inertia in 3x3 matrix format.

SensorItem
==========

When you want to add a sensor to your simulation model, you have to create this item as a child of JointItem.

After created, you can edit the property of the sensor by double clicking the property panel.

translation
-----------

Specifies relative position with respect to the parent joint.


rotation
--------

Specifies relative rotation with respect to the parent joint.

Sensor ID
---------

Specifies unique ID of this sensor.

Sensor type
-----------

Specifies type of sensor from "camera", "range", "gyro", "force", "acceleration".

Once sensor type is selected, properties for each sensor type will appear.


PrimitiveShapeItem
==================

When you want to add a shape to your simulation model, you have to create this item as a child of LinkItem.

After created, you can edit the property of the sensor by double clicking the property panel.


translation
-----------

Specifies relative position with respect to the parent link.


rotation
--------

Specifies relative rotation with respect to the parent link.


Primitive type
--------------

Specifies type of link from "Box", "Cylinder", "Cone", "Sphere".

Once primitive type is selected, properties for each primitive type (e.g. color and radius for sphere) will appear.

MeshShapeItem
=============

When you want to add a shape to your simulation model, you have to create this item as a child of LinkItem.

After created, you can edit the property of the sensor by double clicking the property panel.

translation
-----------

Specifies relative position with respect to the parent link.


rotation
--------

Specifies relative rotation with respect to the parent link.

path
----

Specifies path of VRML97 file.
