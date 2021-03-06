# Forge Networking Remastered Issue #201
## RPCs causing clients to disconnect from server
Unity Project for simplified reproduction of Forge Networking Remastered Issue #201 https://github.com/BeardedManStudios/ForgeNetworkingRemastered/issues/201

## ISSUE RESOLVED: 
Resolution to disconnecting after too many RPC calls
https://github.com/BeardedManStudios/ForgeNetworkingRemastered/commit/ff31f675f553a326ad2be04d21a97b894ecea5fd

## How to use
First **[DOWNLOAD](https://github.com/ForgeUser2018/Forge-Networking-Remastered-RPC-Issue-Test/raw/master/Forge%20Networking%20Remastered%20RPC%20Issue%20Test.unitypackage)** the Unity Package and import it into a fresh Unity project. Then continue with the following steps:

1. Open the "Build Settings" window
2. Add the "MultiplayerMenu" scene and then the "CubeForgeGame" scene to the "Scenes In Build" list
3. Click on "Build" and select a save location
4. Run it and start the host
5. Then run a couple of clients. Start at least 6 clients to see the issue kick in fast.
6. Just let everything run. The RPCs are also sent when there is no user input for demonstration purpose.
   - After a short amount of time, the clients will be disconnected and return to the MultiplayerMenu scene.

###### Additional Info
The standard forge cube example has been modified to use RPCs for the networked cameras to send their position across the network.
The RPC calls are sent in the NetCam.cs script located in Assets/Bearded Man Studios Inc/Examples/Cube Forge/Scripts.

Forge Networking Remastered source ([master repo](https://github.com/BeardedManStudios/ForgeNetworkingRemastered/tree/master) cloned on 2018-11-17) is used in this project for easier debugging.

*Created on 2018-11-17 by ForgeUser2018*
