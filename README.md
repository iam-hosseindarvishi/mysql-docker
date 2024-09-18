# Docker Compose for MySQL and phpMyAdmin

This repository contains a `docker-compose.yml` file that sets up a **MySQL** database alongside **phpMyAdmin** for easy database management.

## Prerequisites

Before using this project, ensure that you have the following installed on your system:

- [Docker](https://www.docker.com/products/docker-desktop)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Services

This setup includes the following services:

1. **MySQL**: A MySQL latest database.
2. **phpMyAdmin**: A web-based tool to manage your MySQL database.

### MySQL Configuration

- **MySQL Root Password**: `rootpassword`
- **Database Name**: `exampledb`
- **MySQL User**: `exampleuser`
- **MySQL User Password**: `examplepass`

The MySQL data will be persisted in a volume at `./mysql_data` in your project directory.

### phpMyAdmin Configuration

- **Access URL**: [http://localhost:8080](http://localhost:8080)
- **Login**: Use the `root` user and the `rootpassword` set in the environment variables.

## Usage

To run the project, clone the repository and navigate to the directory containing the `docker-compose.yml` file. Then, follow the steps below:

### Clone the Repository

```bash
git clone https://github.com/yourusername/your-repository.git
cd your-repository
```
### Start the Containers

Run the following command to start the MySQL and phpMyAdmin containers:
```bash
docker-compose up -d
```
This will start both MySQL and phpMyAdmin in detached mode (running in the background).

### Access phpMyAdmin
Open your browser and go to http://localhost:8080 to access phpMyAdmin. Use the following credentials to log in:
-  **Username**: `root`
- **Password**: `rootpassword`

### Stop the Containers
```bash
docker-compose down
```
This will stop and remove the containers but retain the database data in the ./mysql_data volume.

### Volumes
The data stored in MySQL is saved in the ``./mysql_data`` directory. This ensures that even if the containers are stopped or removed, the data remains intact.

### Customization
To change the MySQL root password, database name, or any other environment variables, you can modify the ``docker-compose.yml`` file as needed.
