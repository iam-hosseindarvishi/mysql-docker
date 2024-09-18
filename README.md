# Docker Compose for MySQL and phpMyAdmin

This repository contains a `docker-compose.yml` file that sets up a **MySQL** database alongside **phpMyAdmin** for easy database management.

## Prerequisites

Before using this project, ensure that you have the following installed on your system:

- [Docker](https://www.docker.com/products/docker-desktop)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Services

This setup includes the following services:

1. **MySQL**: A MySQL 8.0 database.
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
git clone https://github.com/iam-hosseindarvishi/mysql-docker.git
cd your-repository

### Start the Containers

Run the following command to start the MySQL and phpMyAdmin containers:

```bash
docker-compose up -d

