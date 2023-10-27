# Disclaimer
This payload is for academic research and testing. The package is password-protected. By decrypting the package, you agree not to use Revenge-Ratv0.3-complied maliciously.

Password: infected

# Configuring the Revenge-Rat C2 Server
Unzip the password-protected zip file and open the Revenge-RAT v3 - NYANxCAT folder. 
Execute the Revenge-RAT v0.3.exe File.
- In the popup windows, you can create a Socket Key, which you can see from the example below, is the value that will be used to separate the different segments of the data being received from the clients. Example: InformationRevenge-RATTnlhbkNhdFJldmVuZ2U=Revenge-RATX0QwMjk0QUYwRevenge-RAT192.168.75.102
  - It is important to make this value unique to help avoid detection from prebuilt rulesets. It is also important to note that the same Socket Key will be used to build the client.
- Enter the port you would like the Revenge-Rat C2 server to communicate on.
- Once configured, click the Start Listening Button. Note: You may be prompted to add Firewall rules to allow the Clients to connect. 

# Building an Agent
Once the C2 server is configured, we can now build our client. To do this, we can use the Client Builder function built into the C2 Interface, or we can use the Builder.exe file located in the folder. Let's use the internal Client Builder. 
- Click on the Client Builder within the C2 interface.
  - Under the Network Settings drop-down, right-click on the IP address from the loopback (127.0.0.1) and remove that IP address.
    - In the text box, type the IP address of the C2 server and the port the C2 server is listening on, then press the Add icon.
  - Under the Basic Settings, change the client Identifier.
  - Under the install settings, you can change the Drop Path (The location where you want the executable to live) and the name of the Executable file. If the user has the appropriate permissions, you can easily set persistence by clicking on the Registry Box and adding a Registry value name.
  - Under the Assembly settings, we can change the meta-data that will be appended to the end of the file once it is compiled. It is important to note that the default values will be added to the file once complied. To avoid detection from default Yara rules, you may want to change those values.
  - Finally, we can click on the box to Agree to the TOS and then click on the Compile button.
