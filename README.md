# Let's Encrypt Certificate with Nginx, Certbot, and Docker
### Overview
This project provides a streamlined setup for securing your web applications with Let's Encrypt certificates using Nginx, Certbot, and Docker. By leveraging these tools, you can easily deploy, manage and `auto renew` SSL/TLS certificates for your Nginx-based applications in a Dockerized environment.

### Prerequisites
Before getting started, ensure that you have the following prerequisites installed on your system:

Docker: [Install Docker](https://docs.docker.com/engine/install/)

### Getting Started
1. Clone this repository to your machine:

   ```
   git clone https://github.com/rasulv/secure-nginx.git
   ```
   ```
   cd secure-nginx
   ```
2. Configure nginx:
    ```
    cp nginx/site.conf.example nginx/site.conf
    ```
    and edit it

3. Configure certbot:
    ```
    cp init-letsencrypt.sh.example init-letsencrypt.sh
    ```
    and change example.com to your domain and set the staging and email variables in the init-letsencrypt.sh

4. Get ssl certificates:
   ```
   bash ./init-letsencrypt.sh
   ```
5. Run the Docker Compose:
    ```
    docker-compose up --build
    ```

### Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.


### License
This project is licensed under the MIT License - see the [LICENSE](?tab=License-1-ov-file) file for details.