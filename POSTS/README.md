## FUSION 360 Post Processor

This currently only works in inches. I'd need to do more coding to make it work for metric.

**Adjust post for your tool pocket locations.**


var numberOfToolSlots = 7;

/// Tool Changer positions in machine coordinates

var yTcPos = [0,-41.648,-35.148,-28.648,-22.148,-15.648,-9.148,-2.648];

var Xpos = -.097;

var TCZPickup = -5.71;

var TCZDropOff = -5.62;
