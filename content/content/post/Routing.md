+++
author = "Raihan Ali"
title = "Routing Static"
date = "2024-04-01"
description = "Lorem Ipsum Dolor Si Amet"
tags = [
    "markdown",
    "text",
]
weight = 10
+++

Configuring static routing in MikroTik RouterOS is quite straightforward. Here's how you can do it using the WinBox GUI:

1. **Login to your MikroTik router**: Open the WinBox application, enter the IP address of your MikroTik router in the Connect To field, and click on Connect. Then enter your credentials to log in.

2. **Navigate to IP > Routes**: On the left-hand side menu, go to IP and then Routes.

3. **Add a static route**: Click on the "+" icon to add a new static route.

4. **Configure the static route**:
   - Destination: Enter the network address you want to reach via this static route.
   - Gateway: Enter the IP address of the next hop router or the interface where the destination is reachable.
   - Select your routing mark if needed.
   - Select your routing table if needed.
   - Distance: You can set the administrative distance. A lower value indicates a preferred route if multiple routes to the same destination exist.
   - Scope: Choose the scope of the route.
   - Target Scope: Define the target scope.
   - Routing Mark: Define the routing mark for the route if needed.
   - Routing Table: Define the routing table for the route if needed.
   
5. **Click Apply** to save the configuration.

Here is an example:
- Destination: 192.168.2.0/24
- Gateway: 10.0.0.1

This will route traffic destined for the network 192.168.2.0/24 through the gateway with the IP address 10.0.0.1.

Once configured, the MikroTik router will start forwarding traffic to the specified destination network via the configured gateway. Make sure your firewall rules allow traffic to pass through accordingly if necessary.

You can also achieve the same configuration through the command-line interface (CLI) using SSH or Telnet if you prefer CLI over GUI.
