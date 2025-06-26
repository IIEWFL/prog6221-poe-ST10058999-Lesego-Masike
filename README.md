[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Q0H1VfQX)
# Cybersecurity Chatbot GUI

Welcome to the Cybersecurity Awareness Chatbot GUI! This application is a desktop tool designed to educate users on cybersecurity topics, manage tasks with reminders, conduct quizzes, and log activities. Below are the instructions to set up, run, and use the application.

## Prerequisites

Before running the application, ensure you have the following installed on your system:

- **Visual Studio 2022** (or later) with the .NET Desktop Development workload installed.
  - Download from: [https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)
- **.NET 6.0 SDK** (or higher) for building the WPF application.
  - Download from: [https://dotnet.microsoft.com/download/dotnet/6.0](https://dotnet.microsoft.com/download/dotnet/6.0)
- **Windows Operating System** (recommended for full compatibility with audio playback and WPF).

## Setup Instructions

1. **Clone the Repository**
   - Open a terminal or command prompt.
   - Navigate to your desired directory and run:
     - Replace `<repository-url>` with the URL of your Git repository.

2. **Open the Project in Visual Studio**
- Launch Visual Studio 2022.
- Select **Open a project or solution**.
- Navigate to the cloned repository folder and open `CybersecurityChatbotGUI.sln`.

3. **Add the Welcome Audio File**
- The application uses a `welcome.wav` audio file for the greeting.
- Place a `.wav` audio file named `welcome.wav` in the root directory of the project (same level as `Chatbot.cs` and `MainWindow.xaml.cs`).
- If no file is provided, the application will log an error but continue running.

4. **Restore NuGet Packages**
- In Visual Studio, right-click the project in Solution Explorer and select **Restore Packages** to ensure all dependencies are downloaded.

5. **Build the Solution**
- Go to **Build** > **Build Solution** in the Visual Studio menu.
- Resolve any build errors if they occur (check the Output window for details).

6. **Run the Application**
- Press **F5** or select **Start** from the Debug menu to run the application.
- The main window should appear with a logo and a greeting prompt.

## Usage Instructions

### Initial Setup
- Upon launching, the chatbot will display a logo and prompt you to enter your name.
- Enter your name and press Enter. If no name is entered, it defaults to "User".
- The chatbot will ask for your favorite cybersecurity topic (e.g., "password", "scam", "privacy"). Enter a topic or leave blank to proceed.

### Main Features
- **Chat Interaction**
- Type a cybersecurity topic (e.g., "password", "scam", "privacy") in the text box and click "Send" to get a response.
- Use natural language variations like "tell me more" to continue the last topic.

- **Task Management**
- Click "Add Task" to enter a task title and description (e.g., "Enable two-factor authentication").
- After adding a task, you'll be asked if you want a reminder. Use the "Set Reminder" button or type "remind me to [task]" followed by a date (e.g., "2025-06-27" or "in 3 days").

- **Quiz**
- Click "Start Quiz" to begin a 10-question cybersecurity quiz.
- Answer with "A", "B", "C", "D", "TRUE", or "FALSE" and click "Send".
- Use "next question" to proceed or "end quiz" to finish early. The score and feedback will be displayed.

- **Activity Log**
- Click "Show Activity Log" or type "show activity log" to view the last 10 actions with timestamps.
- Actions include task additions, quiz responses, and topic discussions.

### Buttons
- **Send**: Submits the text input for processing.
- **Add Task**: Opens a dialog to add a new task.
- **Set Reminder**: Opens a dialog to set a reminder for an existing task.
- **Start Quiz**: Begins the cybersecurity quiz.
- **Show Activity Log**: Displays the recent activity history.

## Troubleshooting

- **Application Does Not Start**
- Ensure Visual Studio and .NET SDK are correctly installed. Check the Output window for build errors.
- Verify the `welcome.wav` file is in the project directory.

- **Quiz Not Displaying**
- Ensure the "Start Quiz" button is clicked, and the first question should appear automatically.
- If not, check the ChatDisplay TextBox for any error messages and ensure `QuizQuestions` in `Chatbot.cs` is populated.

- **Invalid Date Format**
- When setting reminders, use formats like "2025-06-27" or "in 3 days". An error message will appear for invalid inputs.

- **Audio Not Playing**
- Confirm `welcome.wav` exists and is a valid WAV file. The console will log an error if the file is missing.

## Contributing

If you wish to contribute:
1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Commit your changes and push to your fork.
4. Submit a pull request with a description of your changes.

## License

This project is licensed under the [MIT License](LICENSE) - see the `LICENSE` file for details.

## Last Updated
- **Date and Time**: 09:14 AM SAST, Thursday, June 26, 2025

