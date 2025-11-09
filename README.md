# GitManager

A Windows Forms application built with C++/CLI that provides a graphical user interface for managing Git repositories. This tool simplifies common Git operations and makes version control more accessible for developers working on Windows.

## 🚀 Features

- **Repository Initialization**: Initialize new Git repositories with a single click
- **Git Configuration**: Easy setup of user name and email for Git commits
- **Status Monitoring**: View the current status of your repository
- **File Management**: 
  - Add and commit files with automated workflows
  - Delete files and folders (including submodules)
  - Browse and select repository folders
- **Remote Operations**:
  - Add remote repositories
  - Push changes to GitHub
  - Clone existing repositories
- **Commit History**: 
  - View detailed commit history
  - Filter commits by author and date
  - Display commit hash, message, author, and timestamp
- **User-Friendly Interface**: Intuitive Windows Forms GUI with real-time command output

## 📋 Prerequisites

- Windows Operating System
- Visual Studio 2022 (or later) with C++/CLI support
- .NET Framework 4.7.2 or higher
- Git installed and accessible from command line
- LibGit2Sharp.NativeBinaries (included via NuGet)

## 🛠️ Installation

1. Clone this repository or download the source code
2. Open `GitManager.sln` in Visual Studio
3. Restore NuGet packages (should happen automatically)
4. Build the solution in Debug or Release mode
5. Run the executable from `x64/Debug/GitManager.exe` or `x64/Release/GitManager.exe`

## 💻 Usage

### Getting Started

1. **Launch the Application**: Run `GitManager.exe`
2. **Start Screen**: Click "Start" to proceed to the main interface
3. **Configure Git**: 
   - Enter your GitHub email and username
   - Click "Configure Git" to set up your credentials

### Basic Operations

#### Initialize a Repository
1. Browse or enter the path to your project folder
2. Click "Initialize Git" to create a new Git repository

#### Add and Commit Changes
1. Ensure Git is configured
2. Click "Git Add & Commit" to stage and commit all changes

#### Push to GitHub
1. Enter your GitHub username and repository name
2. Click "Git Push" to upload changes to remote repository

#### Clone a Repository
1. Click "Clone Repository"
2. Enter the repository URL and destination folder name
3. Click "Clone" to download the repository

#### View Commit History
1. Click "View Commit History"
2. Filter by author or date as needed
3. Review detailed commit information in the list

## 📁 Project Structure

```
GitManager/
├── CloneRepoForm.h/cpp     # Clone repository dialog
├── MainForm.h/cpp          # Main application interface
├── StartScreen.h/cpp       # Initial startup screen
├── WinMain.cpp             # Application entry point
├── GitManager.sln          # Visual Studio solution file
├── GitManager.vcxproj      # Project configuration
└── packages/               # NuGet packages (LibGit2Sharp)
```

## 🔧 Technologies Used

- **C++/CLI**: Bridging native C++ with .NET Framework
- **Windows Forms**: GUI framework
- **.NET Framework 4.7.2**: Application runtime
- **LibGit2Sharp**: Native Git binaries for enhanced functionality
- **Git**: Version control system integration

## 📝 Key Features Explained

### Delegates and Event Handling
The application uses custom delegates for handling button clicks and Git operations, providing a clean separation between UI and business logic.

### Process Management
Git commands are executed using `System::Diagnostics::Process` class, allowing real-time output capture and error handling.

### File Operations
Supports complex file operations including:
- Regular file deletion
- Recursive folder deletion
- Submodule management and removal

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## 📄 License

This project is available for educational purposes.

## 👥 Authors

Project developed as part of the "Programación Genérica y Eventos" course.

## 🐛 Known Issues

- Requires Git to be installed and available in system PATH
- Currently supports only master/main branch for push operations
- Windows-only application

## 📞 Support

For issues or questions, please create an issue in the GitHub repository.

---

**Note**: Ensure Git is properly installed on your system and accessible from the command line before using this application.
