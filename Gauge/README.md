<tr>
  <td>
    <a href="https://hub.docker.com/r/sinanerdinc/gauge-testmo-lambdatest" target="_blank">
      <img src="https://img.shields.io/docker/pulls/sinanerdinc/gauge-testmo-lambdatest?style=for-the-badge" />
    </a>
  </td>
</tr>

## Docker image for QA Developers
This Docker image is based on Ubuntu 23.10 and includes the necessary dependencies and tools for building and running applications. It is specifically designed for software development and testing purposes.

### Key features:

- Ubuntu 23.10 as the base image, providing a stable and reliable foundation.
- Essential packages are pre-installed, including curl, wget, zip, unzip, openjdk-11-jdk, apt-transport-https, gnupg2, ca-certificates, maven, nodejs, and npm.
- The globally installed "@testmo/testmo-cli" package for convenient testing and monitoring of applications.
- The Gauge test framework is installed, along with Java and various Gauge plugins such as html-report, xml-report, and screenshot.
- The Lambdatest tunnel is included, enabling secure testing of applications in a LambdaTest environment.

This Docker image provides a streamlined environment for building and testing applications, making it ideal for QA engineers. It offers the necessary tools and dependencies to support a wide range of development and testing workflows. By leveraging this image, you can quickly set up and deploy your applications in a containerized environment, ensuring consistency and reproducibility across different deployment environments.
