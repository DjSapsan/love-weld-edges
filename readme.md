![](https://media.discordapp.net/attachments/474705430434807819/1105919503692476489/Peek_2023-05-07_22-14.gif)

Custom modification of the Box2D and LÖVE code for special purposes.
Modification affects only Weld joints.

New Weld joint must be created in the following way:

	j = love.physics.newWeldJoint(body1, body2) -- skip all other parameters

Bodies are instantly connected edge-to-edge (according to the current relative position).
Also, it supports dynamic changes to shape radius.
For example:

	myFixture:getShape():setRadius(10)
	myFixture:UpdateWeldJointAnchors()	-- new method to update anchors (connection points) to be on circle edges


TODO:
- safer behavior
- dynamic joints breaking
