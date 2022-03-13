# kali-meta-docker
Docker compose for Kali Linux and Metasploitable 2

<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This project builds a Metasploitable 2 and Kalilinux containers over docker. It was implemented during an assignment due to the fact that the new M1 mac Apple Sylicon
chips are not able to virtualize AMD64 because they are ARM. Finally, some functionalities are lost and a huge number of troubles are encountered while trying to make things
work properly.

As part of the work, iptables firewall is employed for closing all ports except 22, 80, 443. If you want to play and exploit Metasploitable 2 vulnerabilities, just delete
the content in the [cortafuegos]() file, and the iptables rules are disabled.
<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

* [Docker](https://www.docker.com/)
* [Docker-compose](https://docs.docker.com/compose/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

Getting started is simple. Just download or clone the repository and satisfy prerequisites.

### Prerequisites

Yoy need the following prerequisites installed in order to correctly run the software:
* docker
* docker-compose


<!-- USAGE EXAMPLES -->
## Usage

Follow the next steps for executing:

* Go to the folder where you have the docker-compose and run the following command to build the images:

```sh
 docker-compose build
 ```
 
* Make sure the images are built with:

```sh
docker image ls
```
 
* Run the containers with (detach mode):

```sh
docker-compose up -d
```

* Now, finally, for accesing the containers, run in two different terminals:

```sh
docker-compose run metasploitable /bin/bash
```

```sh
docker-compose run kalilinux /bin/bash
```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



tomvapon


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[forks-shield]: https://img.shields.io/github/forks/tomvapon/kali-meta-docker.svg?style=for-the-badge
[forks-url]: https://github.com/tomvapon/kali-meta-docker/network/members
[stars-shield]: https://img.shields.io/github/stars/tomvapon/kali-meta-docker.svg?style=for-the-badge
[stars-url]: https://github.com/tomvapon/kali-meta-docker/stargazers
[issues-shield]: https://img.shields.io/github/issues/tomvapon/kali-meta-docker.svg?style=for-the-badge
[issues-url]: https://github.com/tomvapon/kali-meta-docker/issues
[license-shield]: https://img.shields.io/github/license/tomvapon/kali-meta-docker.svg?style=for-the-badge
[license-url]: https://github.com/tomvapon/kali-meta-docker/blob/master/LICENSE.txt
