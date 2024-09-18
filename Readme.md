---

# Node-RED Random Quote Generator

## Project Overview

The **Random Quote Generator** is a Node-RED flow that integrates with the [API-Ninjas Quotes API](https://api-ninjas.com/) to fetch random quotes based on specific categories. The quotes are displayed on a Node-RED dashboard, and the flow can be configured to save quotes into a MySQL database for later use.

This project is perfect for users who want to learn about API integration and build an interactive, customizable quote generation tool.

## Installation Instructions

### 1. Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or above)
- [Node-RED](https://nodered.org/) (v2.x or above)
- [MySQL](https://www.mysql.com/) (optional, if you plan to save quotes)
- An API key from [API-Ninjas](https://api-ninjas.com/).

### 2. Install Node-RED

If you haven’t installed Node-RED yet, follow the [official installation guide](https://nodered.org/docs/getting-started/) for your operating system.

### 3. Clone the Repository

```bash
git clone https://github.com/udaykiran887/random-quote-generator-node-red.git
cd random-quote-generator-node-red
```

### 4. Install Dependencies

You’ll need to install the required Node-RED nodes:

```bash
npm install node-red-dashboard
npm install node-red-node-mysql (optional)
```

### 5. Configure the API Key

Open the flow in Node-RED and configure the `http request` node with your API-Ninjas key:

```
DyDwTNTPaktweamTNKw15w==aQzOSF8YLndWkFFp
```

You can generate your API key from [API-Ninjas](https://api-ninjas.com/).

### 6. Configure MySQL (Optional)

To save the fetched quotes in a MySQL database, you’ll need to configure the MySQL node with your database credentials:

```json
{
    "host": "localhost",
    "port": "3306",
    "user": "your-db-username",
    "password": "your-db-password",
    "database": "quotes_db"
}
```

### 7. Import the Flow

- Open Node-RED in your browser (`http://localhost:1880`).
- Go to the menu in the top-right and select **Import**.
- Paste the JSON flow from the `flow.json` file located in this repository.

### 8. Deploy the Flow

Click the **Deploy** button to activate the flow.

### 9. Access the Dashboard

Navigate to the Node-RED dashboard in your browser to start receiving random quotes:

```
http://localhost:1880/ui
```

## Usage

- The dashboard will display a random quote each time the flow is triggered.
- You can select different categories of quotes via the input options on the dashboard.
- If integrated with MySQL, all fetched quotes will be stored in the database for later use.

## Example Flow Structure

- **Input Node**: Allows users to select a quote category.
- **HTTP Request Node**: Fetches quotes from the API-Ninjas API.
- **Dashboard Node**: Displays the quote on the Node-RED UI.
- **MySQL Node** (optional): Saves the quotes to a database.

## Contributing

Contributions are welcome! If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

Feel free to suggest improvements, submit bug reports, or request new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact Information

For any questions or issues, you can reach the project maintainer at:

- **Email**: [Gmail](udaykirankothagattu.com)
- **GitHub**: [udaykiran887](https://github.com/udaykiran887)

---
