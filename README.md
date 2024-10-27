# ESP32 Based Webserver for Measurement of Temperature & Humidity

### Objective
Create a webserver using the ESP32 board that displays temperature and humidity from a DHT11 sensor. If the temperature exceeds a given threshold, an alert will get triggered on email

### Tools/Components Required For this Project

* Arduino IDE (software)

* Breadboard

* USB Cable

* ESP32 Feather Board

* Jumper Wires

* DHT11 Sensor




### Step 1 - Constructing our Hardware (Physical Setup) 

<img src="https://github.com/user-attachments/assets/e564b78d-a983-4107-926a-9dcfbc8de1fd" width="500">



The connectivity between ESP32 and the DHT11 Sensor is fairly easy as it only has three pins. To connect them, plug the VCC and GND of the sensor to their respective pins (of ESP32). However, for the last pin; you will notice that my approach differs from the blueprint image. This is because my demo setup had a different configuration, hence in this setup we are going to connect the data pin of the sensor to GPIO13.

<img src="https://github.com/user-attachments/assets/e1de449c-e52a-40b0-89f0-76f8911d3c62" width="300">


<img src="https://github.com/user-attachments/assets/7f280610-8c31-424e-9c77-9032a0543eb3" width="300">

### Step 2 - Setting Up a Trigger by Using IFTTT - If This
IFTTT is a web-service that creates conditional statements to trigger actions on platforms like Gmail, SMS, and more. We will use this to alert us once the threshold to the weather patterns has exceeded

2.1 Login or signup on [IFTTT](https://example.com)

2.2 After signing in, you will be introduced to an "Explore" page. In the searchbar, type "webhooks" and select it from the result. Then on the next page, click on the "Create" button

<img width="355" alt="image" src="https://github.com/user-attachments/assets/5a68f6ea-6fc2-40fc-9ce1-358bafc99363">

2.3  In the next step, click "Add" for the "If This" condition. In the search panel, search for "webhooks" again

<img width="355" alt="image" src="https://github.com/user-attachments/assets/31dc0cdd-728a-40bc-b887-36924eaefe2f">

2.4 Choose the "Receive a Web Request" and type "temp_event" on the next page to create a trigger (NB! Pro membership is required)

<img width="334" alt="image" src="https://github.com/user-attachments/assets/319b11be-6e55-45e8-b004-42fdc13f5480">



### Step 3 - Confirming the action - Then That
3.1 With the trigger set, we can move over to "Then that" section. Here we will specify what platform the action will get sent to. We will choose "Email"

<img width="348" alt="image" src="https://github.com/user-attachments/assets/75284614-6daf-4e8c-965a-ce4f15cdb451">

3.2 After selecting "send me an email", fill out the subject and body as shown in the image below and create

<img width="431" alt="image" src="https://github.com/user-attachments/assets/64d4ddc7-5e50-4bb0-8a6b-36138aaf6ab4">

3.3 Finish to complete setup, if done correctly it should look like this

<img width="238" alt="image" src="https://github.com/user-attachments/assets/c1dd7872-2be5-43f6-9d92-f8efdf107169">



### Step 4 - Arduino 

<img width="190" alt="image" src="https://github.com/user-attachments/assets/9c677e0d-1a3b-4e82-8bf1-20b4b35296b3">



