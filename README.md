# INCEPTION

### GOAL
42 project to discover the utilisation of Dockers by the creation of a Wordpress server.
___
You will have to learn how to create a Dockerfile, a configuration file and some script to create a docker image and run it as a container.

## Requirements
This project uses docker and docker-compose to works.
So if you want to know how it works, it is better to have some knowledge about how these works.

```bash
sudo apt-get update
sudo apt-get install docker.io -y
sudo apt-get install docker-compose -y
```

___

You will also need a .env file to put in the ./srcs/ folder like the following :
```env
WP_HOST=your_wordpress_host
WP_URL=your_url /* (in this project 'login.42.fr') */
WP_TITLE=your_wordpress_title

WP_ADMIN_LOGIN=your_admin_login
WP_ADMIN_PASSWORD=your_admin_password
WP_ADMIN_EMAIL=your_admin_email

WP_USER_LOGIN=your_user_login
WP_USER_PASSWORD=your_user_password
WP_USER_EMAIL=your_user_email
```

___

If you want the project to work when accessing your url put in the .env file, it is mandatory that you add it in the /etc/hosts file of your machine.

Like the following :
`127.0.0.1 login.42.fr`

## HOW DOES IT WORK
To start the project you just have to use the command `make` or `make re` this will launch the commands `docker-compose up` with the **--build** flag, this will build the container's images and run them.

When it is done, you can access your Wordpress website with your url.

The website is just a WordPress template where you can see how WP works and customize it via `login.42.fr/wp-admin/` like below :

![wpimage](https://github.com/user-attachments/assets/6c71547e-8af1-40fd-923c-b6d65cec03a0)
