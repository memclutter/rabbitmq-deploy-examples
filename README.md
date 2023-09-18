# Rabbitmq Deploy Examples

This repository provides a simple example of running RabbitMQ using Docker Compose. It includes a configuration for a single-node RabbitMQ instance.

## Prerequisites

Before you begin, make sure you have the following prerequisites installed on your system:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### Clone the Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/memclutter/rabbitmq-deploy-examples.git
cd rabbitmq-deploy-examples
```

### Customize Environment Variables

In the single-node directory, you will find a .env.dist file. Copy this file to .env and customize the environment variables as needed. You can set the RabbitMQ username and password in this file.

```bash
cp single-node/.env.dist single-node/.env
```

Edit single-node/.env to set your desired RabbitMQ credentials:


```bash
RABBITMQ_USER=your_username
RABBITMQ_PASS=your_password
```

### Run RabbitMQ with Docker Compose

Now you can start RabbitMQ using Docker Compose. Run the following command from the root directory of the repository:

```bash
cd single-node
docker-compose up -d
```

This command will start a single-node RabbitMQ instance in the background.

### Access RabbitMQ Management

You can access the RabbitMQ Management web interface at http://localhost:15672 in your web browser. Use the credentials you set in the .env file to log in.

## Cleanup

To stop and remove the RabbitMQ container, run:

## License

This project is licensed under the MIT License - see the LICENSE file for details.
