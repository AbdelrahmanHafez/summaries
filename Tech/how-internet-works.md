# How Does The Internet Work
Summary of [YouTube - How does the internet work? (Full Course)](https://www.youtube.com/watch?v=zN8YNNHcaZc&)

## Connecting to a Local Network

Computers connect to each other on a network using:
1. **A switch** if they need to connect with cables.
2. **An access point** if they need to use wireless technology.

Cables are either CAT-5, CAT-6 (copper) or fiber-optic. CAT-6 is faster than CAT-5.

LAN is short for Local Area Network.

A packet/A frame is a message that needs to be sent from one computer to another via the network.

## Connecting to The Internet

We use a router to connect to the internet, we'd need a to connect a router to the switch.
The reason we're able to connect to the internet is because we have a cable coming from outside the building that we connect to the router.

A home-router is a single device that does both The Router and Switch jobs.
## What is The Internet?
Simplified, The Internet is a bunch of routers all over the world, all connected to one another.

Fiber-optic cables connect countries one to another, mostly in the sea. There's 4 million kilometers of fiber-optic cables around the world. 
## Forwarding
When a router receives a packet, seeing that it should send it to The Internet, how does it determine which router to send it to?
It checks its own "Routing Table".  A Routing Table is a list of all the routers this router is connected to. This process is called "Forwarding".

Each Router checks the Routing Table, and ignores the router it received the packet from, then it decides which new router it'll send it to, the new router repeats the process, and so on until the packet arrives at its destination.

Overall, routers try to use the path that has the shortest time from the source-to-destination. This could mean more routers, but shorter distance, or maybe a longer distance, but one of the routers has such a high traffic that would take a longer time to process the packet.

There are complicated algorithms that decide the path of the packet over the network of routers.

## Streaming
Sending data piece-by-piece. This is useful for watching videos, for example.

## Wide Area Network (WAN)
WAN is LAN but in different areas of the world. Imagine having a company that has multiple branches in different countries. Each office has its own LAN, we create a WAN to make both offices able to communicate with each other.

The reason we need WAN when each office is able to connect to the internet is to allow each office to connect to the other privately and securely.

WAN can be expensive to implement, there are multiple ways to implement it. One popular, cost-effective way to implement WAN is to use VPN and network tunneling.

We use Routers to create WANs, while we use Switches to create LANs.

#### Traffic Tunneling
Tunneling is encrypting the packets so that only the receiver on the other side how has the key to decrypt it can read it.

## Campus Area Network (CAN)
Connecting one LAN to another. For example, two offices that are in a short distance of one another, connecting the switches in each office to each other creates a CAN. The distance MUST be short, though.

CANs would need encryption as well.
### WAN Types
1. **Public WAN**: is a WAN that is connected to the internet. Typically when used across different countries.
2. **Private WAN**: is a WAN that is connected via a dedicated ISP WAN Network, used when the distance is short between both LANs. Private WAN can be very expensive, even though it's typically more secure since it doesn't go through the public internet.

## Internet Service Provider (ISP)
ISPs are companies that allow us to connect to the internet. They play a central role in connecting the different LANs all over the world together, by moving the packets across them. So for example if two computers in the same neighborhood want to connect to one another, and both of them are in the same ISP, the packet would go from LAN 1 => Local ISP => LAN 2.

## Point of Presence (POP)
An ISP would have one or more POPs, each POP is a bunch of routers that traffic flow through. A POP would typically be responsible for an area or a neighborhood.

## ISPs structure
1. **Local ISPs**: ISPs that connect neighborhoods.
2. **Regional ISPs**: ISPs that connect cities in a country.
3. **Network of a country**: is the combination of all the Local ISPs and the Regional ISPs in that country.
4. **Global ISPs**: ISPs that connect devices from different countries. Packet goes through Local ISP => Regional ISP => Global ISP => Regional ISP => Local ISP => LAN.
## Possible connections
1. A Local ISP can connect directly to a Global ISP directly without the Regional ISP in the middle. This same Local ISP would typically be connected to a Regional ISP still, but the Regional ISP would just not be in the middle of the Local => Global connection. The connections would be adjacent.

2. A LAN doesn't necessarily have to connect to a Local ISP, a LAN can connect directly to a Regional ISP, or a Global ISP if they offer services in my location.

## Packet Path Is Determined On The Way
When making a request over the internet from one country to another, the request packets can take one path over the ISPs and routers, and then the response comes from a completely different path. Routers decide where to send the packet next on the way, and there is no way of determining this beforehand.

#### Peering
Peering is a process where big companies like Google would setup a direct connection between their servers and Local ISPs, that way they reduce the numbers of the routers their traffic has to go through, reducing the overall time the request/response cycle takes, resulting in a better performance for the end-user.

#### Internet Backbone
The global ISPs network is commonly referred to as The Internet Backbone.
Global ISPs are have a high initial cost, but they also are profitable businesses on the long term.

#### Internet Exchange Point (IXP)
IXPs are structures that help Global ISPs to communicate more efficiently, in a synchronous manner.

# References
[YouTube - How does the internet work? (Full Course)](https://www.youtube.com/watch?v=zN8YNNHcaZc&)
