# space.api
The [Space API](https://spaceapi.io/) endpoint for the Amman Valley MakerSpace.

## Usage

If the button is on or off, the scripts will upload the current status.
Since the scripts run each minute once, see crontab and
GitHub refreshes the page every 5 minutes, it can take up to 
**6 minutes** until an update arrives on the website.

## Installation

1. Install git.
2. Create SSH-Key. 
    ```
    ssh-keygen
    ```
3. Add the `~/.ssh/id_rsa.pub` as deploy key to the repo or add it to the GitHub account.
4. Clone the repo
    ```
    git clone git@github.com:AmmanVMS/space.api
    cd space.api
    git config --local user.email "pi@raspi"
    git config --local user.name "pi"
    ```
5. Add crontab with `crontab -e`:
    ```
    * * * * * /home/pi/space.api/check_status.job
    ```

## Hardware setup

See [Using Switch with Raspberry Pi – Python](https://electrosome.com/using-switch-raspberry-pi/).

![image](https://user-images.githubusercontent.com/564768/179254745-3d816c42-57bd-415f-a971-402d4f052f74.png)
