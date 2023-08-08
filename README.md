# Event Driven Architecture with RabbitMQ 📌

## Contents:
1. [Structure:](#structure)
2. [Usage:](#usage)
    a. [Environment:]()
    b. [Command:]()
    c. [Services:]()
3. [License](#license)
4. [Author](#author)

---

## Structure:

```
.
├── README.md
├── consumer
│   ├── Dockerfile
│   ├── main.py
│   ├── manager.py
│   └── requirements.txt
├── docker-compose.yml
├── environment
│   ├── broker.env
│   ├── mysql.env
│   └── worker.env
└── producer
    ├── Dockerfile
    ├── main.py
    ├── manager.py
    ├── producer.py
    └── requirements.txt
```

## Usage:
#### Environment:

```
# Tree
├── environment
     ├── broker.env
     ├── mysql.env
     └── worker.env
```

```dotenv
# broker.env
RABBITMQ_DEFAULT_USER=rabbitmq    
RABBITMQ_DEFAULT_PASS=rabbitmq123
```

```dotenv
# mysql.env
MYSQL_DATABASE=main
MYSQL_USER=root
MYSQL_PASSWORD=1234
MYSQL_ROOT_PASSWORD=1234
```

```dotenv
# worker.env
RABBIT_MQ_URI=amqp://rabbitmq:rabbitmq123@localhost:/broker-mq
MYSQL_URI=mysql://root:1234@db/main
```

#### Command:

```
# Start Services
docker compose up -d
```

#### Services:

- RabbitMQ Management UI: [http://localhost:](http://localhost:)
- RestAPI Producer: [http://localhost](http://localhost:)

## License:
MIT

## Author:
Lê Trường Thịnh (Fxbite)

 

   
