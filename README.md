# SweetChatBot

This is a simple chatbot built using **Spring Boot** and **Spring AI**, which integrates with OpenAI's GPT models to generate responses based on user input.

## Features
- Uses **Spring Boot** for backend development.
- Integrates with **OpenAI API** to process and generate chat responses.
- Simple **REST API** for chatbot interaction.
- Maintains conversation history.

## Prerequisites
Before running the project, ensure you have:
- **Java 21+** installed
- **Maven** installed
- **An OpenAI API key** (Get it from [OpenAI](https://platform.openai.com/signup/))

## Installation
### 1. Clone the repository
```sh
git clone https://github.com/Jeremias16Dinzinga/SweetChatBot.git
cd SweetChatBot
```

### 2. Configure API Key
Edit `src/main/resources/application.properties` or `application.yml` and add your OpenAI API key:
```properties
spring.ai.openai.api-key=your-api-key-here
spring.ai.openai.model=gpt-3.5-turbo
```

### 3. Build and Run the Project
```sh
mvn spring-boot:run
```

## Usage
### API Endpoint
**POST** `/api/chat`

#### Example Request
```sh
curl -X POST "http://localhost:8080/api/chat?message=Hello!"
```

#### Example Response
```json
{
  "response": "Hello! How can I assist you today?"
}
```

## Project Structure
```
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── com.sweet-company.sweetChatBot
│   │   │   │   ├── controller
│   │   │   │   │   ├── ChatController.java
│   │   │   │   ├── service
│   │   │   │   │   ├── ChatService.java
│   ├── resources
│   │   ├── application.properties
│   │   ├── application.yml
├── pom.xml
└── README.md
```

## Future Improvements
- Integrate with **WhatsApp, Telegram, or Discord**
- Improve response formatting and error handling

## Author
[Jeremias António Dinzinga](https://www.linkedin.com/in/jeremias-dinzinga-a9867b221/)
