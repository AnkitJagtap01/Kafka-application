# Kafka Application

This project is a Kafka-based application that demonstrates the usage of KafkaJS, a modern Apache Kafka client for Node.js. It includes the implementation of both Kafka producers and consumers, showcasing how to handle message production and consumption using KafkaJS.

## Table of Contents

- [Kafka Application](#kafka-application)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Usage](#usage)
    - [Running the Producer](#running-the-producer)
    - [Running the Consumer](#running-the-consumer)
  - [Troubleshooting](#troubleshooting)
  - [Contributing](#contributing)
  - [License](#license)
  - [Contact](#contact)

## Features

- Kafka producer that sends messages to a specified topic.
- Kafka consumer that reads messages from a specified topic.
- Configurable retry and timeout settings for robust message handling.
- Example usage of KafkaJS for connecting to Kafka brokers.

## Prerequisites

- [Node.js](https://nodejs.org/) (version 12.x or later)
- [Apache Kafka](https://kafka.apache.org/) (running broker)
- [KafkaJS](https://kafka.js.org/)

## Installation

1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/AnkitJagtap01/Kafka-application.git
   cd Kafka-application
   \`\`\`

2. Install the dependencies:
   \`\`\`bash
   npm install
   \`\`\`

## Configuration

Configure the Kafka broker connection settings in the \`config.js\` file:
\`\`\`javascript
module.exports = {
  clientId: 'my-app',
  brokers: ["<PRIVATE_IP>:9092"],
  topic: 'your-topic-name',
  connectionTimeout: 10000,
  retry: {
    retries: 5
  }
};
\`\`\`

## Usage

### Running the Producer

To start the Kafka producer and send messages to the topic:
\`\`\`bash
node producer.js
\`\`\`

### Running the Consumer

To start the Kafka consumer and read messages from the topic:
\`\`\`bash
node consumer.js
\`\`\`

## Troubleshooting

### Common Errors and Solutions

- **KafkaJSConnectionError: Connection timeout**
  - Ensure the Kafka broker is running and reachable.
  - Check your network configuration and broker settings.
  - Increase the \`connectionTimeout\` and \`retries\` in the configuration.

- **KafkaJSNumberOfRetriesExceeded**
  - Verify the broker address and port.
  - Ensure there are no network policies blocking the connection.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or inquiries, please contact [Ankit Jagtap](mailto:jagtap.an@northeastern.edu).
