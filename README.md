### Chat Application: Real-Time Multi-Client Messaging System

#### Overview
This is a real-time chat application that enables multiple clients to connect to a centralized server and exchange messages with each other. The application supports basic functionalities such as nickname registration, message broadcasting, and user disconnection handling. It is built using Python's `socket` and `threading` modules, providing a simple and efficient way to create a chat server and client.

#### Features

- **Multi-Client Support**: Allows multiple clients to connect and communicate simultaneously with the server.
- **Nickname Registration**: Each user is prompted to enter a nickname, which is displayed alongside their messages.
- **Message Broadcasting**: Messages sent by any user are broadcast to all connected clients.
- **Secondary Connection**: The client manages two separate connections to the server, enhancing the reliability of message delivery.
- **Response Time Measurement**: The client measures and records the response time for each message sent, providing data for performance analysis.
- **Performance Analysis**: Generates metrics such as average, minimum, and maximum response times, which can be exported and visualized for further insights.
- **Graceful Disconnection**: Users can exit the chat gracefully by typing `/exit`, ensuring proper resource cleanup and disconnection.
- **Private Messaging**: Implement private chat functionality between users.

#### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/chat-application.git
   cd chat-application
   ```

2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the server:
   ```bash
   python server.py
   ```

4. Run the client(s):
   ```bash
   python client.py
   ```

#### Usage

- **Server**: The server script (`server.py`) listens for incoming connections and handles message forwarding between clients.
- **Client**: The client script (`client.py`) connects to the server, allows the user to send and receive messages, and measures response times.

#### Performance Metrics

The client application captures and logs the response time for each message sent. This data can be used for analyzing network performance under different conditions such as packet loss, delay, and varying bandwidth. The metrics are stored in CSV files and visualized using graphs and statistical summaries.

#### Future Enhancements
- **File Sharing**: Add support for file transfer between clients.
- **Advanced Performance Monitoring**: Include more granular metrics like network jitter and packet retransmissions.

#### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
