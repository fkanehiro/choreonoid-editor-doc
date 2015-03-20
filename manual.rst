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

When you want to add a joint to your simulation model, you have to create this item.

After created, you can edit the property of the joint by double clicking the property panel.

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

LinkItem
========

When you want to add a joint to your simulation model, you have to create this item.

After created, you can edit the property of the joint by double clicking the property panel.

Primitive type
--------------

Specifies type of link from "Mesh", "Cylinder", "Cone", "Sphere".

Once primitive type is selected, property for each primitive types (e.g. color and radius for sphere) will be appeared.

Mass
----

Specifies mass.

Center of mass
--------------

Specifies location of mass center in [x, y, z] format.

Inertia
-------

Specifies moment of inertia in 3x3 matrix format.
