# Setting up EXC-1553UNET/P2-M as a Remote Terminal (RT) Simulator 🚀

[The Device](./device_image.jpeg)

## Prerequisites 📋
- Fresh Windows 10 installation 💻
- EXC-1553UNET/P2-M device 🔧
- Excalibur Installation CD 💿
- Provided cables and power supply 🔌

## Installation and Setup 🛠️

1. Install the Excalibur Software Tools: 💾
   1. Insert the Excalibur Installation CD into your computer's CD drive.
   2. The InstallShield Wizard should appear. If not, browse to the CD drive and run the setup file.
   3. Follow the on-screen instructions to complete the installation. ✅

2. Connect the cables: 🔗
   1. Connect the MIL-STD-1553 I/O connectors of the EXC-1553UNET/P2-M to the MIL-STD-1553 bus using the provided triax cables.
   2. Connect the USB Communication port of the EXC-1553UNET/P2-M to a USB port on your host computer using the provided Micro-B USB to Standard-A USB cable.
   3. If additional power is needed, connect the USB Power port of the EXC-1553UNET/P2-M to another USB port or a wall outlet using the provided USB power supply.

3. Install the USB driver: 🚗
   1. Windows should automatically find and install the driver. If not, open the Device Manager, right-click on the unknown USB device, and select "Update Driver Software."
   2. Choose the option to browse your computer and select the folder: C:\Excalibur\1553UNET\USB Driver.
   3. Click Next to install the driver. ✅

4. Assign a device number: 🔢
   1. Run ExcConfig by clicking Start > All Programs > Excalibur > ExcConfig Board Setup Utility.
   2. Double-click on an empty cell (e.g., Device #1).
   3. In the Excalibur Configuration Wizard, select EXC-1553UNET/Px.
   4. Choose USB Connection and enter the serial number located on the back of the device (if using multiple devices).
   5. Click OK - Finished Modifying, then click Save to Registry. ✅

5. Test the connection: 🔌
   1. Run UNETTool by clicking Start > All Programs > Excalibur > 1553UNET > UNET Utilities > UNET GUI Tool.
   2. Select the device number assigned in step 4 and click Test Connection To UNET.
   3. If successful, the LED will turn green, and the device's IP address, MAC address, and serial number will be displayed. 🎉

6. Configure the EXC-1553UNET/P2-M as an RT: ⚙️
   1. Open the Merlin+ software by clicking Start > All Programs > Excalibur > Merlin+ > Merlin+.
   2. Click Settings > Project Settings and select the device number assigned in step 4.
   3. In the Mode dropdown, select Remote Terminal.
   4. Configure the RT settings, such as RT Address, Subaddress, Data Buffers, etc., according to your requirements.
   5. Click Apply and then OK. ✅

7. Define the RT's response to command words: 💬
   1. In Merlin+, navigate to the Subaddress tab.
   2. For each subaddress, define the data buffer and configure the RT's response (e.g., transmit data, status word, etc.).
   3. You can also set up error injection and other advanced settings if needed.

8. Start the RT simulation: 🏁
   1. Click the Run button in Merlin+ to start the RT simulation.
   2. The EXC-1553UNET/P2-M will now respond to command words as configured. 🎉

9. Monitor and debug: 🔍
   1. Use Merlin+ to monitor the bus traffic and debug any issues.
   2. You can also use the Discrete Generator (Start > All Programs > Excalibur > Discrete Generator > Discrete Generator Tool) to test the discrete I/O functionality.

This setup will allow you to simulate an RT with the EXC-1553UNET/P2-M device, configure its response to command words, and monitor the bus traffic using the provided Excalibur software tools on a Windows 10 system. 🚀✨
