<h1 align="center">
  <br>
  <a href="https://github.com/Steccas/stecCA"><img src="https://raw.githubusercontent.com/Steccas/stecCA/main/img/logo.png" alt="StecCA" width="256"></a>
  <br>
    StecCA
  <br>
</h1>

<h4 align="center">An easy to deploy Certificate Authority using <a href="https://github.com/cloudflare/cfssl" target="_blank">CFSSL</a>, <a href="https://github.com/Netflix/lemur" target="_blank">Lemur</a> and <a href="https://www.docker.com/" target="_blank">Docker</a> magic!</h4>

<br>

<p align="center">
  <a href="https://github.com/Steccas/stecCA/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://github.com/Steccas/stecCA/network/members"><img src="https://img.shields.io/github/forks/Steccas/stecCA.svg?style=for-the-badge"></a>
  <a href="https://github.com/Steccas/stecCA/issues">
      <img src="https://img.shields.io/github/issues/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://github.com/Steccas/stecCA/issues">
      <img src="https://img.shields.io/github/issues-closed/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://github.com/Steccas/stecCA/stargazers">
    <img src="https://img.shields.io/github/stars/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://github.com/Steccas/stecCA/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://GitHub.com/Steccas/stecCA/pull">
    <img src="https://img.shields.io/github/issues-pr/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://GitHub.com/Steccas/stecCA/pull">
    <img src="https://img.shields.io/github/issues-pr-closed/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://GitHub.com/Steccas/stecCA/commit">
    <img src="https://img.shields.io/github/last-commit/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://GitHub.com/Steccas/stecCA">
    <img src="https://img.shields.io/github/repo-size/Steccas/stecCA.svg?style=for-the-badge">
  </a>
  <a href="https://linkedin.com/in/lucasteccanella">
    <img src="https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555">
  </a>
  <a href="https://www.buymeacoffee.com/steccas" target="_blank">
    <img src="https://cdn.buymeacoffee.com/buttons/lato-yellow.png" alt="Buy Me A Coffee" height="27.8">
  </a>
</p>


<p align="center">
  <a href="#about-the-project">About</a> •
  <a href="#built-whit">Technologies</a> •
  <a href="#key-features">Key Features</a> •
  <a href="#getting-started">How To Use</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#support">Support</a> •
  <a href="#license">License</a>
</p>


<!-- ABOUT THE PROJECT -->
## About The Project

Ever wanted or had the need to manage certificates for your private homelabs? Worry no more this project provides a full working SSL and yes it has no errors!

This calls the need to have a Certificate Authority and with OpenSSL, the terminal, is not so fancy for some certificates so i had to check for better system, thanks to steccas here we are.

With the ease of using CFSSL CLI and the OSCP responder and its simple integration with lemur a merge of the two sounds inevitable. Ofcourse lemur provides the web UI for the management, issuing, revoking and tracking of certificates is straightforward.

Thanks to [Steccas]((https://github.com/steccas/stecCA/tree/main)) for bringing everything together and just like memorizing the alphabet all we need to do is just follow prompts and instructions.

*In minutes get your CA up n running!*

## Built with

This project uses the following technologies:

<a href="https://github.com/cloudflare/cfssl">
  <img alt="CFSSL" src="https://img.shields.io/badge/CFSSL-f48120.svg?&style=for-the-badge&logo=cloudflare&logoColor=white"/>
</a>
<a href="https://github.com/Netflix/lemur">
  <img alt="Lemur" src="https://img.shields.io/badge/lemur-%23CC0000.svg?&style=for-the-badge&logo=netflix&logoColor=white"/>
</a>
<a href="https://www.docker.com/">
  <img alt="Docker" src="https://img.shields.io/badge/docker-%230db7ed.svg?&style=for-the-badge&logo=docker&logoColor=white"/>
</a>
<a href="https://www.gnu.org/software/bash/">
  <img alt="Bash" src="https://img.shields.io/badge/bash-%23121011.svg?&style=for-the-badge&logo=gnu-bash&logoColor=white"/>
</a>
<a href="https://www.postgresql.org/">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/postgres-%23316192.svg?&style=for-the-badge&logo=postgresql&logoColor=white"/>
</a>
<a href="https://www.nginx.com/">
  <img alt="NGINX" src="https://img.shields.io/badge/nginx-%23009639.svg?&style=for-the-badge&logo=nginx&logoColor=white"/>
</a>

CFSSL acts as the core engine for SSL, being called upon the generation of CA and certificates while Lemur offers an integrated system with a web interface to make the management very very easy.

Everything is stored thanks to the PostgreSQL DB.

The deployment is done with docker and some bash scripting, it makes data persistence and deployment really fast and repeatable.

<!-- 
* [CFSSL](https://github.com/cloudflare/cfssl)
* [Lemur](https://github.com/Netflix/lemur)
* [Docker](https://www.docker.com/)
* [Bash](https://www.gnu.org/software/bash/)
-->

## Key Features

* Easy and fast deploy!
  - Thanks to docker and bash scripting deploying a fully working CA doesn't take hours anymore!
* Root CA and Intermediary CA
  - Root CA is not directly exposed, an Intermediate CA (signed by root) will be signing the user created certificates.
* Web Interface
  - Lemur provides an easy-to-use web interface to issue, manage and revoke certificates.
* Automation
  - Lemur provides various automated checks on certificates, some have already been enabled but many many more can be enabled depending on your needs.
* Persistence
  - The integration with PostgreSQL of both CSSL and Lemur allows to easily manage and make persistent all the data needed.
* OSCP Responder
  - CFSSL's OSCP responder has been set up, including automatic updates.
    (I'm Not sure if it is already working as I configured it, so any help is really appreciated)

<!-- GETTING STARTED -->
## Getting Started

Getting the CA up and running is fairly easy if you pay attention in following these little steps, the guide and the scripts are assuming that you are using a Windows Operating system.


### Prerequisites
As a prerequisite, you should just need an up and running Docker and Docker Compose installation. This will not be done by the script.

1. _Please refer to the [Docker install guide](https://docs.docker.com/engine/install/) and [Docker-Compose install guide](https://docs.docker.com/compose/install/) to complete this passage_.
  
It is very quick and simple, don't worry.

You need a working firewall, i suggest to
* Install UFW
  ```sh
  sudo apt update
  sudo apt install ufw
  ```
Otherwise, you need to edit lines 69 and 70 of [setup_cfssl.sh](https://github.com/Steccas/stecCA/blob/main/setup_cfssl.sh) to obtain the same firewall rules, this is very important or otherwise, the ROOT CA will be exposed in the network! (CFSSL Auth cannot be integrated with Lemur yet)

### Installation

I'm using nano in some commands, but you can use any editor you want of course!

1. Clone the repo
   
   _For the original repo by Steccas_
    ```sh
    git clone https://github.com/Steccas/stecCA.git
    ```
    _For this repo_
    ```sh
    git clone [https://github.com/Steccas/stecCA.git](https://github.com/Felix273/stecCA)
    ```
2.  Edit line 33 of [setup_cfssl.sh](https://github.com/Felix273/stecCA/blob/main/setup_cfssl.sh)  to have the right path to your go directory.

    ```sh
    /usr/local/go/bin/go install bitbucket.org/liamstask/goose/cmd/goose@latest
    ```
    
3.  Edit [cfssl-config.json](https://github.com/Steccas/stecCA/blob/main/cfssl-config.json) to have the right url for yor crl and oscp, it may be localhost. Leave the same ports.
   
    ```sh
    nano ./cfssl-config.json
    ```
    
5. Edit [csr_root_ca.json](https://github.com/Steccas/stecCA/blob/main/csr_root_ca.json) and [csr_intermediate_ca.json](https://github.com/Steccas/stecCA/blob/main/csr_intermediate_ca.json) to setup the right values for your root CA and intermediate CA, there are already exaple values, change them and you are good to go.
   
    ```sh
    nano ./csr_root_ca.json
    nano ./csr_intermediate_ca.json
    ```
7. Similiarly, edit [ocsp.csr.json](https://github.com/Steccas/stecCA/blob/main/ocsp.csr.json) to have the right informations for your OCSP.
    ```sh
    nano ./ocsp.csr.json
    ```
    
8. Edit [lemur.env](https://github.com/Steccas/stecCA/blob/main/lemur.env) to have the same informations available to Lemur. Don't touch the password, it will be set later automatically.
    ```sh
    nano ./lemur.env
    ```

9. Edit [creds.env](https://github.com/Steccas/stecCA/blob/main/creds.env) to setup username and password for DB and other services, they will be automatically changed in the other files and will be automatically used; so use a complicated one.
    ```sh
    nano ./creds.env
    ```
    CHANGE THEM, the one put in the files are meant to be a placeholder or a default password for testing at best!

10. Start the setup script as root, it will ask if you configured everything, but if you don't do and something doesn't work as expected or you leave the default password (that everyone in github will know) it is up to you! Also, before running make sure that you have the execute permission flag.
    ```sh
    chmod u+x ./setup_cfssl.sh
    sudo ./setup_cfssl.sh
    ```

11. The setup will ask at some point to paste the pem certs data at the bottom of [lemur.conf.py](https://github.com/Steccas/stecCA/blob/main/lemur.conf.py), it is important or Lemur WILL NOT WORK.
    ```sh
    nano ./lemur.conf.py
    ```
    and at the bottom look for these values and change them according to the outputted PEMs and your choosen url.
    ```py
    CFSSL_URL ="http://ca.example.lan:8888" #change this with machine ip or dns name
    CFSSL_ROOT ="""<insert root pem here>"""
    CFSSL_INTERMEDIATE ="""<insert intermediate pem here>"""
    ```
    After this it will start everything up and as a last passage it will ask to add this to crontab, of course set also your desired frequency, which wil be opened for you in 5 seconds.
    ```sh
    cfssl ocspdump -db-config /etc/cfssl/db_config.json> /etc/cfssl/ocspdump
    ```

12. Check the health of the containers with
    ```sh
    docker ps
    ```
    If they are not healty or something doesn't work, check every passage, open an Issue or check <a href="#support">Support</a>.

13. Enjoy
<!-- USAGE EXAMPLES -->
## Usage

You can now simply open Lemur at port 443 of your machine (using your IP, localhost, or DNS name) and log in with your defined credentials, the web interface password is defined in the `lempass` environment variable, the username is "lemur".

Of course, remember to add your CA to your OSes and browsers.

The interface is really easy, but please refer to [Lemur documentation](https://lemur.readthedocs.io/en/latest/) for better instructions.

If you need to reboot your server it is not a problem, docker-compose should bring services up again and thanks to data persistence everything will be there.

This means that if you backup your CFSSL data and Docker volumes you can easily migrate to another machine.

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create.

And this project can be greatly improved!

Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

You can also consider to help with a donation ❤️
<br>

<a href="https://github.com/sponsors/Steccas" target="_blank">
    <img src="https://img.shields.io/badge/sponsor-%23F5F5F5.svg?&style=for-the-badge&logo=github&logoColor=pink" alt="GitHub Sponsor">
</a>
<a href="https://www.buymeacoffee.com/steccas" target="_blank">
    <img src="https://cdn.buymeacoffee.com/buttons/lato-yellow.png" alt="Buy Me A Coffee" height="27.8">
</a>


## Support

This project comes without any warranty, you are responsible for the deployment.
If you encounter [open an issue](https://github.com/Steccas/stecCA/issues), consider [getting a sponsor plan](https://github.com/sponsors/Steccas) or contact me to get dedicated support.


<!-- LICENSE -->
## License

Distributed under the GNU GPL V3 License. See [LICENSE](https://github.com/Steccas/stecCA/blob/main/LICENSE) for more information.

---

> [linktr.ee](https://linktr.ee/steccas) &nbsp;&middot;&nbsp;
> GitHub [@Steccas](https://github.com/Steccas) &nbsp;&middot;&nbsp;
> LinkedIn [Luca Steccanella](https://linkedin.com/in/lucasteccanella)

<br>

![](https://estruyf-github.azurewebsites.net/api/VisitorHit?user=Steccas&repo=stecCA&countColorcountColor&countColor=%237B1E7A)
