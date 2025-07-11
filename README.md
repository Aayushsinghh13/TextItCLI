# 🚀 TextIt - Social Media Reimagined!

<div align="center">
  <img src="https://img.shields.io/badge/Status-In%20Development-yellow" alt="Status: In Development">
  <img src="https://img.shields.io/badge/Security-Basic-orange" alt="Security: Basic">
  <img src="https://img.shields.io/badge/Version-1.1-blue" alt="Version: 1.1">
  <img src="https://img.shields.io/badge/Language-Java-orange" alt="Language: Java">
</div>

## ✨ Welcome to TextIt!

**TextIt** is an evolving Java-based open-source console application that aims to create a secure social media platform. Currently in early development, TextIt focuses on building a solid foundation with user authentication and basic security features. Made for Indians by Indians, TextIt is designed with security in mind, implementing validation checks for user registration and OTP-based verification. As development progresses, we plan to add comprehensive social features like posting, following, and content engagement.

## 🔥 Why Choose TextIt?

- **🔒 Focus on Security**: Building a foundation with input validation and OTP verification
- **👤 User Authentication**: Comprehensive validation for usernames, passwords, emails, and phone numbers
- **📱 Early-Stage Development**: Join us on the ground floor as we build a secure social platform
- **⚡ Java-Based Architecture**: Clean, modular code structure for maintainability and extensibility
- **🛠️ Constantly Evolving**: Regular updates and new features based on user feedback

## 🌟 Current Features

| Feature | Description |
|---------|-------------|
| 🔐 Input Validation | Our robust validation system checks for: |
| | • Non-empty unique usernames |
| | • Valid 10-15 digit numeric phone numbers |
| | • Email uniqueness |
| | • Strong 8-16 character passwords with uppercase, lowercase, numbers, and special characters |
| 🔑 Basic Security | SHA-256 hashing for passwords and simple AES encryption capabilities |
| 📧 OTP Verification | Email-based OTP generation and verification for account security |
| 💾 Database Integration | PostgreSQL database connection for storing and validating user data |
| 🧩 Modular Design | Clean separation of concerns with interfaces and implementation classes |

## 🚧 Features Under Development

| Feature | Status |
|---------|--------|
| 👤 Profile Management | Early stages |
| 📱 Content Creation | Planned |
| 🔔 Notification System | Basic framework in place |
| 👥 Follow System | Framework in place |
| 👍 Like System | Basic framework in place |

## 💻 Technologies Used

TextIt is currently built with the following technologies:

- **Backend**: Java
- **Database**: PostgreSQL
- **Build Tools**: Maven
- **Security**: 
  - Basic SHA-256 hashing for passwords
  - Simple AES encryption (currently using default ECB mode)
  - Email-based OTP verification
- **Email**: JavaMail API for OTP delivery
- **Version Control**: Git
- **Documentation**: Markdown, JavaDoc

## 🏗️ Current Project Architecture

TextIt is organized into a modular structure that separates concerns and promotes maintainability:

```
📁 src/
├── 📁 model/auth/ - Authentication interfaces
│   └── 📄 Authentication.java - Interface defining validation methods
├── 📁 model/exceptions/ - Custom exceptions for validation
│   ├── 📄 EmptyInputException.java - For empty input fields
│   ├── 📄 DataAlreadyUsedException.java - For duplicate usernames/emails
│   ├── 📄 IllegalLengthException.java - For invalid input lengths
│   ├── 📄 UpperCaseNotFoundException.java - For password validation
│   ├── 📄 LowerCaseNotFoundException.java - For password validation
│   ├── 📄 NumericNotFoundException.java - For password validation
│   └── 📄 SpecialCharacterNotFoundException.java - For password validation
├── 📁 service/pages/ - User interface components
│   └── 📄 SignUp.java - Implements registration validation
├── 📁 security/ - Security implementations
│   ├── 📄 Hashing.java - Basic SHA-256 password hashing
│   ├── 📄 Encryption.java - Simple AES encryption
│   └── 📄 OTPHandler.java - Email-based OTP generation and delivery
├── 📁 database/ - Database access
│   └── 📄 DataBase.java - Contains Profile and OTP management classes
├── 📁 inbox/ - Early social feature implementations
│   ├── 📄 FollowTracker.java - Framework for follow functionality
│   ├── 📄 LikeTracker.java - Basic implementation for like tracking
│   └── 📄 InboxHandler.java - Manages notifications
└── 📁 UI/ - User interface
    └── 📄 Main.java - Application entry point
```

This structure provides a foundation that can be extended as more features are implemented.

## 🚦 Getting Started

### Prerequisites
- Java JDK 8 or higher
- PostgreSQL for database
- Git for version control
- Maven for dependency management
- Gmail account for OTP functionality (with app password)

### Installation Steps

1. **Clone the repository** - Bring TextIt to your local machine
   ```bash
   git clone https://github.com/yourusername/textit.git
   cd textit
   ```

2. **Set up your database** - Create a PostgreSQL database
   ```bash
   # Create a database named "Local TextIT"
   # Create tables for user profiles and OTP storage
   ```

3. **Configure database credentials** - Update the DataBase.java file
   ```java
   // Update these values in DataBase.java
   private static final String url = "jdbc:postgresql://localhost:5432/Local TextIT";
   private static final String username = "your_username";
   private static final String password = "your_password";
   ```

4. **Configure email credentials** - Update the OTPHandler.java file
   ```java
   // Update these values in OTPHandler.java with your Gmail app password
   private static final String SENDER_EMAIL = "your.email@gmail.com";
   private static final String SENDER_PASSWORD = "your_app_password";
   ```

5. **Build the project** - Compile and package the application
   ```bash
   mvn clean package
   ```

6. **Run the application** - Start exploring TextIt
   ```bash
   java -jar target/textit-1.1.jar
   ```

> **Note**: The application is in early development, so many features described in the documentation are still being implemented.

## 🛡️ Security: Current Implementation

TextIt is being built with security in mind. Our current security features include:

- **Password Validation** with requirements for:
  - 🔠 Upper and lowercase letters
  - 🔢 Numbers
  - #️⃣ Special characters (!, @, $, &, *)
  - 📏 Length between 8-16 characters

- **Basic Hashing** using SHA-256 for password storage

- **Simple Encryption** capabilities using AES (currently in default ECB mode)

- **OTP Verification** via email for account verification

> **Note**: We plan to enhance security in future versions with salted password hashing, more secure encryption modes, and additional authentication factors.

## 🔮 Development Roadmap

TextIt is in active development. Here's what we're working on:

### 🔒 Security Enhancements
- **Improved Password Hashing**: Implement bcrypt or PBKDF2 with salt
- **Enhanced Encryption**: Replace default ECB mode with more secure GCM mode
- **Secure Key Management**: Proper handling of encryption keys
- **Multi-factor Authentication**: Additional security layers

### 📱 Core Social Media Features
- **User Profiles**: Complete profile management system
- **Post Creation & Sharing**: Text-based content sharing
- **Like System**: Fully functional like tracking and notifications
- **Follow Functionality**: Complete follow system with notifications
- **Comments**: Interactive conversations on posts

### 🛠️ Technical Improvements
- **Database Optimization**: Proper schema design and indexing
- **Connection Pooling**: Efficient database connection management
- **Error Handling**: Comprehensive exception handling
- **Logging**: Proper logging instead of System.out.println
- **Testing**: Unit and integration tests

See our detailed [task list](docs/tasks.md) for more information on planned improvements.

## 🤝 Join Our Community

TextIt is in its early stages, making this the perfect time to get involved and help shape its future. We welcome contributions of all kinds:

### How to Contribute

- **Code Improvements**: Help implement features from our [task list](docs/tasks.md)
- **Security Enhancements**: Improve our authentication and encryption systems
- **Bug Fixes**: Address issues in the current implementation
- **Documentation**: Improve or expand our documentation
- **Testing**: Add unit and integration tests
- **Ideas**: Share your suggestions for features or improvements

### Current Development Priorities

1. **Complete the Authentication System**: Finish the login functionality
2. **Enhance Security**: Implement proper password hashing with salt
3. **Develop Social Features**: Complete the follow and like systems
4. **Improve Database Design**: Optimize schema and queries
5. **Add Content Management**: Implement post creation and storage

### Reporting Issues & Requesting Features

We use GitHub Issues to track bugs and feature requests:

1. **Check existing issues** first to avoid duplicates
2. **Use our templates** for [bug reports](.github/ISSUE_TEMPLATE/bug_report.md) or [feature requests](.github/ISSUE_TEMPLATE/feature_request.md)
3. **Provide detailed information** to help us understand and address your submission

For security vulnerabilities, please follow our [Security Policy](docs/SECURITY.md) instead of creating a public issue.

## 📣 Connect With Us

Have questions or suggestions? We'd love to hear from you!

- **GitHub Issues**: [Report bugs or request features](https://github.com/yourusername/textit/issues)
- **Email**: [contact@textit.example.com](mailto:contact@textit.example.com)
- **Twitter**: [@TextItApp](https://twitter.com/TextItApp)
- **Discord**: [Join our community](https://discord.gg/textit)
- **Reddit**: [r/TextIt](https://reddit.com/r/TextIt)

## 📄 Project Documentation

TextIt maintains comprehensive documentation to ensure a professional and organized project:

### Legal Documents
- [License](LICENSE) - MIT License detailing how the code can be used
- [Terms of Service](TERMS_OF_SERVICE.md) - Rules and conditions for using TextIt
- [Privacy Policy](PRIVACY_POLICY.md) - How we collect, use, and protect your data
- [Patent Grant](PATENTS.md) - Patent usage rights for the project
- [Trademark Policy](TRADEMARK.md) - Guidelines for using the TextIt name and logo

### Community Guidelines
- [Code of Conduct](CODE_OF_CONDUCT.md) - Guidelines for community participation
- [Contributing Guide](CONTRIBUTING.md) - How to contribute to the project
- [Governance](GOVERNANCE.md) - Project leadership and decision-making structure
- [Security Policy](SECURITY.md) - Reporting and handling security vulnerabilities
- [Changelog](CHANGELOG.md) - Record of all notable changes to the project

### For Contributors
- [Bug Report Template](.github/ISSUE_TEMPLATE/bug_report.md) - For reporting issues
- [Feature Request Template](.github/ISSUE_TEMPLATE/feature_request.md) - For suggesting enhancements
- [Pull Request Template](.github/PULL_REQUEST_TEMPLATE.md) - For submitting code changes
- [Code Owners](.github/CODEOWNERS) - Designated maintainers for different parts of the codebase

If you'd like to support TextIt financially, check out our [funding options](.github/FUNDING.yml).

---

<div align="center">
  <b>TextIt - Your Secure Social Media Experience</b>
</div>
