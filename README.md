# <p align="center">MiroTalk WebRTC Admin</p>

<hr />

<p align="center">
    <a href="https://webrtc.mirotalk.com">webrtc.mirotalk.com</a>
</p>

> **Note**
> Enter a `valid email`, username and chosen password, `confirm the email` and enjoy!

<hr />

<p align="center">Manage and scheduling all the MiroTalk's WebRTC rooms:</p>

<br/>

| `MiroTalk`                                               | Description                                                                                                                                                                                |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 🚀 [P2P](https://github.com/miroslavpejic85/mirotalk)    | `Peer to peer` real-time video conferences, optimized for small groups. Unlimited time, unlimited concurrent rooms each having 5-8 participants.                                           |
| 🏆 [SFU](https://github.com/miroslavpejic85/mirotalksfu) | `Selective forwarding unit` real-time video conferences, optimized for large groups. Unlimited time, unlimited concurrent rooms each having 8+ participants.                               |
| ✨ [C2C](https://github.com/miroslavpejic85/mirotalkc2c) | `Cam to cam` (peer to peer) real-time video conferences, optimized for one to one. Unlimited time ,unlimited concurrent rooms each having 2 participants.                                  |
| 📡 [BRO](https://github.com/miroslavpejic85/mirotalkbro) | `Live broadcast` (peer to peer) live video, audio and screen stream to all connected users (viewers). Unlimited time, unlimited concurrent rooms each having a broadcast and many viewers. |

<br>

![mirotalk-webrtc-admin](./frontend/Images/mirotalk-web.png)

<hr />

<p align="center">
    For questions, discussions, help & support, join with us on <a href="https://discord.gg/rgGYfeYW3N">discord</a>
</p>

<hr />

<details open>
<summary>Quick start</summary>

<br/>

Install [NodeJs](https://nodejs.org/en/blog/release/v18.16.0).

## Quick start

```bash
# Clone the project repo
$ git clone https://github.com/miroslavpejic85/mirotalkwebrtc.git

# Go to project dir
$ cd mirotalkwebrtc

# Copy .env.template to .env and customize it according to your needs
$ cp .env.template .env

# Copy config.template.js to config.js and customize it according to your needs
$ cp backend/config.template.js backend/config.js
```

---

### MongoDb

![mongo-db](./frontend/Images/mongodb.png)

`Local MongoDb` deployment using [docker-compose](https://docs.docker.com/compose/install/): If you prefer to run MongoDb locally using docker-compose, execute the following command::

```bash
$ npm run mongo:up
# npm run mongo:down to stop container
```

`Cloud MongoDb` deployment (Optional): Alternatively, you have the option to deploy MongoDb in the cloud, specifically through [MongoDb Atlas](https://www.mongodb.com/). Please remember to update the credentials in the `.env` file accordingly.

```bash
# MongoDB Configuration (https://www.mongodb.com/)
MONGO_URL=mongodb://${MONGO_USERNAME}:${MONGO_PASSWORD}@${MONGO_HOST}:${MONGO_PORT}
MONGO_DATABASE=mirotalk
```

---

### Email verification

![email](./frontend/Images/email.png)

`User email verification` (Optional): By default, user email verification is `enabled`. If you prefer to disable it, set `EMAIL_VERIFICATION` to `false` in the `.env` file. If you choose to keep enabled, configure the email settings as follows:

```bash
# Email Configuration (https://support.google.com/mail/answer/185833?hl=en)
EMAIL_VERIFICATION=true
EMAIL_HOST=emailHost
EMAIL_PORT=emailPort
EMAIL_USERNAME=emailUsername
EMAIL_PASSWORD=emailPassword
```

---

### Install dependencies and start the server

```bash
# Install dependencies
$ npm install

# Start the server
$ npm start
```

Open in browser: http://localhost:9000

</details>

<details open>
<summary>Docker</summary>

<br/>

![docker](./frontend/Images/docker.png)

Install [docker](https://docs.docker.com/engine/install/) and [docker-compose](https://docs.docker.com/compose/install/).

```bash
# Copy .env.template to .env and edit it
$ cp .env.template .env
# Copy config.template.js to config.js and edit it
$ cp backend/config.template.js backend/config.js
# Copy docker-compose.template.yml in docker-compose.yml and edit it if needed
$ cp docker-compose.template.yml docker-compose.yml
# Get official image from Docker Hub
$ docker pull mirotalk/webrtc:latest
# Create and start containers (-d as daemon)
$ docker-compose up
```

[Docker official image](https://hub.docker.com/r/mirotalk/webrtc)

</details>

<details>
<summary>Migrations</summary>

<br/>

For MongoDB migrations follow [this README](./database/README.md).

</details>

<details>
<summary>API</summary>

<br/>

You can check the swagger document at http://localhost:9000/api/v1/docs, or live [here](https://webrtc.mirotalk.com/api/v1/docs).

</details>

<details>
<summary>Self hosting</summary>

<br/>

To self-hosting MiroTalk WEB, just follow [this steps](./docs/self-hosting.md).

</details>

<details open>
<summary>Support</summary>

<br/>

You can show your support for MiroTalk's projects by considering sponsorship. By sponsoring MiroTalk on platforms like GitHub Sponsors, you can contribute to our ongoing work and help us continue to develop and improve the projects.

To support MiroTalk's projects, you can visit the sponsorship page at https://github.com/sponsors/miroslavpejic85. There, you will find the different sponsorship tiers available. You can choose a sponsorship level that suits your budget and desired level of support.

Sponsoring MiroTalk's projects not only helps us financially but also encourages our motivation and dedication to creating valuable software. Your sponsorship can enable us to allocate more time and resources towards the projects, leading to further enhancements, bug fixes, and new features.

Thank you for considering supporting MiroTalk's projects. Your sponsorship can make a positive difference and contribute to the success of our endeavors.

</details>

<details>
<summary>License</summary>

<br/>

![AGPLv3](./frontend/Images/AGPLv3.png)

MiroTalk is free and can be modified and forked. But the conditions of the AGPLv3 (GNU Affero General Public License v3.0) need to be respected. In particular modifications need to be free as well and made available to the public. Get a quick overview of the license at [Choose an open source license](https://choosealicense.com/licenses/agpl-3.0/).

For a MiroTalk license under conditions other than AGPLv3, please contact us at license.mirotalk@gmail.com or [purchase directly via CodeCanyon](https://codecanyon.net/item/a-selfhosted-mirotalks-webrtc-rooms-scheduler-server/42643313).

Thank you!

</details>
