# space.api
The [Space API](https://spaceapi.io/) endpoint for the Amman Valley MakerSpace.

![image](https://user-images.githubusercontent.com/564768/180646227-e5a9dec4-6eba-4ac0-867f-9a7d7889ea16.png)

## Usage

If the button is on or off, the scripts will upload the current status.
Since the scripts run each minute once, see crontab and
GitHub refreshes the page every 5 minutes, it can take up to 
**6 minutes** until an update arrives on the website.

### The App

To install the app [MyHackerspace][mhs]:

1. Head over to [f-droid.org](https://f-droid.org/).
2. Download the F-Droid app and install it.
3. Search in it for [MyHackerspace][mhs]: "hacker"
4. Install the app. ([Direct Download](https://f-droid.org/repo/ch.fixme.status_21.apk))
5. Choose `Amman Valley MakerSpace`
6. If you want the widget:  
    ![image](https://user-images.githubusercontent.com/564768/180646507-8ecbb045-6ed7-4cce-a769-90427883f696.png)
    1. Long-click on the background of your Android Phone
    2. Choose `Widgets`
    3. Choose `MyHackerspace`
    4. Choose the `Amman Valley MakerSpace`
    5. Choose to display the text and the transparent background.
    6. You will see a button but soon it will have refreshed.

[mhs]: https://f-droid.org/en/packages/ch.fixme.status/

## Server Installation

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
