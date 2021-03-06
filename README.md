# ClimateForNINJA
[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)


## Contents

1. [Short description](#short-description)
1. [Demo video](#demo-video)
1. [The architecture](#the-architecture)
1. [Long description](#long-description)
1. [Solution roadmap](#solution-roadmap)
1. [Getting started](#getting-started)
1. [Contributing](#contributing)
1. [Using IBM Cloud Services or IBM Systems](#using-ibm-cloud-service-or-ibm-systems)
1. [Authors](#authors)


## Short description

A tool for developers confronting climate change


## Demo video
[![Watch the video](https://github.com/RyogaTakao/ClimateForNinja/blob/master/fig/Video_Image.png)](https://youtu.be/CShJTAtQW3c)

## The architecture
<img src="https://github.com/RyogaTakao/ClimateForNinja/blob/master/fig/Architecture.png" width=100%>

1. Measure room temperature with Raspberry Pi and temperature sensor every hour.
1. Format the acquired data with Node-RED in Raspberry Pi and send the data to IBM Watson IoT Platform.
1. Load the data posted to IBM Watson IoT Platform with Node-RED on IBM Cloud.
1. Store the loaded data and outdoor temperature retrieved from The Weather Company API in IBM cloudant with Node-RED on IBM Cloud.
1. Format the data stored in IBM cloudant into JSON format.
You can get the JSON by sending an Http/Get request.
1. Send an Http/Get request to the above to get the data.
Display a graph of the data and a JSON string as a web application


## Long description

According to IBM global study conducted by Morning Consult , Eight out of  ten respondents agree with the idea that “people want to do something to help combat climate change, but don't know where to start.”
What can we do to support for them? To solve this problem, we made API, essential tool around developers, which turns the abstract word, ‘Climate Change’ into more concrete one for them to use.
We focused on  ‘Air conditioner’, because we’ve faced and will face environmental problems such as overusing fossil fuels causing climate change. For instance, International Energy Agency states that around 2/3 of the world’s households could have an air conditioner by 2050. In addition, energy demand for space cooling will more than triple by 2050. Thus, we address to Air Conditioner, one of the most familiar household appliances in our lives. 
Climate for NINJA measures temperature while operating air conditioner and allows users to visualize the fluctuation of room temperature and outside temperature at the same time. 
Furthermore, it converts the sensing data into JSON file, which allows developers to utilize the data more frequently. That is because, it is easy to find the data they want with JSON file and transfer it to other systems.

Developers can create following services with our API :
- Service that urges users to turn off the air conditioner when there is little difference between measured room temperature and outside temperature.
- When internal temperature at home or stopped car with the elderly or small child expects to get higher considering outside temperature, services that notify their parents or carers and automatically turn on the air conditioner.
- Machine learning services using measured temperature that urge customers to use air conditioner appropriately.

Like these, this solution brings many positive outcomes. The more developers make use of this solution, the more customer demand we can responded to. Also, we utilized Node-RED in developing API, which allows us to introduce it to many companies at low cost due to its ease of distribution. 
API has more potential than a single product or service because it can be transformed to anything by benefiting from excellent developers.



## Roadmap
![Roadmap](https://github.com/RyogaTakao/ClimateForNinja/blob/master/fig/Roadmap.png)


## Getting started
1. Git clone this repository
```
$ git clone <This Repository>
```
2. Import JSON files into your Node-RED

## Contributing
Climate for NINJA gives developers various ideas.
If it is used by many developers, it will create a solution for more environments.
It is a tool for many developers to solve environmental problems.

Climate for NINJA is full of possibilities.


## Using IBM Cloud Services or IBM Systems

- [Node-RED](https://nodered.org/)
- [IBM Watson IoT Platform](https://www.ibm.com/jp-ja/marketplace/internet-of-things-cloud)
- [IBM Cloudant](https://www.ibm.com/jp-ja/cloud/cloudant)
- [The Weather Company API](https://callforcode.weather.com/)


## Authors
- [RyogaTakao](https://github.com/RyogaTakao)
    - Faculty of Science and Technology, Meijo University
    - Back-end engineer
- [YoshiharuSenna](https://github.com/YoshiharuSenna)
    - Faculty of Science and Technology, Meijo University
    - Front-end engineer
- [OkazakiTatsuya](https://github.com/TatsuyaOkazaki324)
    - Faculty of Science and Technology, Meijo University
    - Embedded engineer
- [Miyu Oba](https://github.com/mlieynua)
    - Faculty of Foreign Languages, Nanzan University
    - planner
