# BpmApp

This project is a comprehensive system that integrates a Spring Boot application with Keycloak for robust authentication and authorization purposes. Alongside authentication features, the application facilitates functionalities for managing processes, cases, and tasks, in addition to offering extensive history services. Moreover, it seamlessly interacts with various APIs, all conveniently accessible from a React-based front-end interface.
## Table of Contents

- BpmApp
    - Description
    - Table of Contents
    - Technologies Used
    - Setup
        - Prerequisites
        - Installation
        - Running the Application
    - API Reference
    - Environment Variables


## Technologies Used

- Spring Boot
- Keycloak
- PostgreSQL
- pgAdmin
- ActiveMQ
- React
- typescript


## Setup
### Prerequisites

- Docker
- Node.js

### Installation
1 - Clone the repository:

```bash
    git clone <repository_url>
```

2 - Navigate to the project directory:

```bash
    cd <project_directory>
    cd Docker
```

3 - start docker \
4 - run docker-compose 

```bash
    docker-compose up --build
```


## API Reference
some of process api
#### Get all processes Definition

```http
  GET process-api/definitions
  Authorization: Bearer {your_access_token}
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `Authorization` | `string` | **Required**. Access token obtained from Keycloak

#### Start process

```http
  POST process-api/start?processDefinitionKey=processDefinitionKey
  Authorization: Bearer {your_access_token}
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `processDefinitionKey` | `string` | **Required**. Process definition key
| `Authorization` | `string` | **Required**. Access token obtained from Keycloak


## Environment Variables

To run this project, you will need to add the some environment variables to your .env files

/Docker/.env \
src/main/resources/flowable-ui/.env

