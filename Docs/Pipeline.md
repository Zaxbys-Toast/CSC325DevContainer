# CI/CD Pipeline Section

## CI/CD Pipeline Environment:

Our CI/CD pipeline operates within a cloud-based infrastructure provided by GitHub Actions. The pipeline runs on Ubuntu latest runners hosted by GitHub's infrastructure. This ensures consistency and reliability in our build and deployment processes. Additionally, our project utilizes Flutter for cross-platform development, which is supported by GitHub Actions.

## CI/CD Pipeline Tools:

### GitHub Actions:
We have chosen GitHub Actions as our CI/CD tool for its seamless integration with our GitHub repositories and its native support for building, testing, and deploying software applications. GitHub Actions allows us to define custom workflows using YAML files within our repository, providing flexibility and ease of configuration.

#### Features:
- **Native Integration**: GitHub Actions is tightly integrated with GitHub repositories, allowing us to trigger workflows based on various events such as pushes, pull requests, and issue comments.
- **Workflow Customization**: We can define complex workflows using YAML syntax, specifying different jobs and steps to automate our CI/CD processes.
- **Extensive Marketplace**: GitHub Actions provides a marketplace with a wide range of pre-built actions for common tasks, enabling us to easily incorporate third-party tools and services into our workflows.
- **Scalability**: GitHub Actions scales effortlessly to accommodate our project's growing needs, with generous resource allocation for concurrent workflows.

#### Limitations:
- **Learning Curve**: While YAML-based configuration is straightforward, mastering advanced features and best practices may require some initial learning.

### Flutter Action:
We utilize the `subosito/flutter-action` action to set up the Flutter environment within our GitHub Actions workflow. This action installs the Flutter SDK and configures it based on the specified channel (beta), ensuring consistency in our build environment.

#### Features:
- **Automatic Setup**: The Flutter Action automates the setup process for the Flutter SDK, eliminating the need for manual installation and configuration.
- **Channel Selection**: It allows us to specify the Flutter channel (beta) to use for building our project, giving us access to the latest features and updates while maintaining stability.

#### Limitations:
- **Dependency Management**: While the Flutter Action handles the installation of the Flutter SDK, managing project dependencies still requires additional steps, such as running `flutter pub get`.

### peaceiris/actions-gh-pages:
For deployment of our Flutter web application to GitHub Pages, we utilize the `peaceiris/actions-gh-pages` action. This action simplifies the process of deploying static web content to GitHub Pages, providing configuration options for specifying the publish directory and authentication.

#### Features:
- **GitHub Pages Deployment**: The actions-gh-pages action automates the deployment of static files to GitHub Pages, eliminating the need for manual uploads or configuration.
- **Token Authentication**: It utilizes GitHub tokens for authentication, ensuring secure deployment without exposing sensitive credentials.

#### Limitations:
- **Static Content Only**: This action is specifically designed for deploying static content to GitHub Pages and may not be suitable for more complex deployment scenarios.

## Automation Process:

Our CI/CD pipeline automates the build and deployment phases of our software development lifecycle, ensuring efficient and reliable delivery of our Flutter web application. The automation process is outlined below: