Using the above two codes, you can send and on or off signal to switch a device on or off. The code is implemented for the esp32 microcontroller.
The remote and the device both connect to the GCP using a private key stored in the ATECC508A and a JSON Web Token (JWT) with
a JSON Web Signature (JWS). But the catch is that you cannot directly run this code for ESP32, so you need to make sure you have excc08-with-esp32 added to your workspace. Real credit lies with PBearson for providing the repository, but I had to make a few changes to work for esp32. And then only you will be able to connect your devices to the cloud. After the authentication is completed, the communication is done using the MQTT, which is based on the pub-sub model.
You will need to add the secrets tab's details to make your details more secured and inaccessible to others. But before filling that, you need to register the devices on the GCP
IoT core and create topics and register the devices as subscribers or publishers according to your requirements.
