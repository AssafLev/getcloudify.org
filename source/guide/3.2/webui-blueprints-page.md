---
layout: bt_wiki
title: The Blueprints Page
category: Web Interface
publish: true
abstract: Blueprint Page Reference
pageord: 110

terminology_link: reference-terminology.html
node_types_link: dsl-spec-node-types.html
relationships_link: dsl-spec-relationships.html
---
{%summary%}This is a view of a single blueprint in Cloudify's User Interface{%endsummary%}.

When clicking on the `Blueprints` tab and choosing a blueprint you will be able to choose one of the following:

# Topology
The [Topology]({{page.terminology_link}}#topology) is an application’s graph of nodes and their relationships, which describes the lifecycle events or other operations that each node and relationship exposes for use in workflows.<br>
Each of the blueprint's nodes is displayed as a square container, which can contain other nodes. Each node has a title describing its name, and an icon to indicate the [node's type]({{page.node_types_link}}).<br>
[Relationships]({{page.relationships_link}}) between nodes are marked with arrows, starts from the connected node and ends at the target node.<br>
The topology view shows only the application nodes and not the network nodes. If a node has a network dependency, it will be displayed as a bullet icon in the node's title.<br>
The number of [node instances]({{page.terminology_link}}#node-instance) is marked in a bullet beside the node's type icon.<br>

![Blueprint topology]({{ site.baseurl }}/guide/images/ui/ui-blueprint-topology.png)

Clicking a node's title will open a side panel with details of the selected node.<br>

![Blueprint node details]({{ site.baseurl }}/guide/images/ui/ui-blueprint-floating-panel.png)

# Network
A map of networks topologies according to the blueprint's topology contains internal and external networks, hosts, routers.<br/>
The network's name is displayed as a grey title, each network contains sub-networks displayed as colored lines underneath.
Network devices, such as hosts & routers, are displayed as icons, each icon indicates the device's type.
Connections between sub-networks and devices are marked with a colored line, by the color of the connected sub-network.<br>
Clicking a device will open a side panel with details of the selected device.<br>

![Blueprint networks]({{ site.baseurl }}/guide/images/ui/ui-deployment-networks.jpg)

# Nodes
A list of nodes according to the blueprint topology.<br/>
For every node, its type, number of instances, and relationships are shown. By clicking the magnifier icon, a side panel will be opened with the selected node's details.
![Blueprint's nodes]({{ site.baseurl }}/guide/images/ui/ui-deployment-nodes.jpg)

# Source
Displays highlight blueprint source code, Python plugins and other text files includes in your blueprint package.<br/>
![Blueprint source code]({{ site.baseurl }}/guide/images/ui/ui-blueprint-sourcecode.jpg)
