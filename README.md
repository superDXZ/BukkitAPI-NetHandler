# BukkitAPI-NetHandler
Defines the protocol between Lunar Client and servers supporting it

# LCPacketTeammates
This packet will display arrows over player heads for the receiver of the packet. The structure of the packet should go as follows:

Leader:
Any UUID, this value isn't read
LastMS:
The current time in millis
Players:
* PlayerId-A
  * "x": X-Coord (`3.2D`)
  * "y": Y-Coord (`72.0D`)
  * "z": Z-Coord (`10.3D`)
  * "world": WorldName (`"world"`)
* PlayerId-B
  * "x": X-Coord (`30.2D`)
  * "y": Y-Coord (`3.0D`)
  * "z": Z-Coord (`15.0D`)
  * "world": WorldName (`"world_the_end"`)

The player can recieve itself in the players map. In this example, if the player receiving the packet is in the same world as PlayerId-B it will only display that player, since PlayerId-A isn't in the world. 
