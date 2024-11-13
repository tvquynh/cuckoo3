## Cuckoo3 Quick Start Guide <p>
For full documentation, please visit: https://cuckoo-hatch.cert.ee/static/docs/installing/quickstart/ <br>
## Prepare Fresh Ubuntu 22.04 LTS
## Step 1: Run the Installation Script <br>

1. Open your terminal. <br>

2. Run the following command to download and execute the Cuckoo3 installation script. This may take some time, depending on your internet connection speed. <br>
```
  curl -sSf https://cuckoo-hatch.cert.ee/static/install/quickstart | sudo bash <br>
```

3. When prompted, select "y" for all questions. <br>

4. If prompted to create a user, enter "cuckoo" as the username. <br>

5. After the script completes, run these additional commands to set up permissions for the helper script: <br>

    sudo chmod +x helper_script.sh

## Step 2: Reboot the Server

1. Reboot the server to finalize setup.

sudo reboot

2. After the server reboots, log in with a user account that has sudo permissions.

3. Run the helper script:

    cd ~ && ./helper_script.sh

## Step 3: Finalize Cuckoo3 Setup

1. Switch to the cuckoo user:

sudo su cuckoo

2. Clean up old socket files (if any exist):

rm /home/cuckoo/.cuckoocwd/operational/sockets/*.*

3. Activate the Python virtual environment for Cuckoo3:

source /home/cuckoo/cuckoo3/venv/bin/activate

4. Start Cuckoo3 in debug mode to ensure everything is working correctly:

    cuckoo --debug

## Step 4: Access the Cuckoo3 Web Interface

Open a web browser and navigate to:

http://<server_IP>:8080

Replace <server_IP> with your server's IP address.







