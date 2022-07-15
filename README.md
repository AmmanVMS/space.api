# space.api
The [Space API](https://spaceapi.io/) endpoint for the Amman Valley MakerSpace.

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
    ```
5. Add crontab with `crontab -e`:
    ```
    * * * * * /home/pi/space.api/check_status.job
    ```
