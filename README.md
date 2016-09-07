# Logistics Wizard Toolchain

This toolchain will allow you to deploy the entire Logistics Wizard demo system, which is a supply chain management web application composed of several microservices:  
- [Controller][github_controller_url] - The API that sits on the edge of the architecture and interfaces with all other services.  
- [ERP][github_erp_url] - An API that handles user login and interaction with the ERP system objects.  
- [WEBUI][github_webui_url] - The Web UI that is the web front end of the entire application, built using React.

The toolchain is preconfigured for:

- issue tracking
- source control
- continuous delivery and integration (CI/CD)
- unit and code coverage testing
- blue-green deployment

![Toolchain template steps](./.bluemix/toolchain.png)

## Create the toolchain

**To get started, click this button:**  
[![Deploy To Bluemix](./.bluemix/create_toolchain_button.png)](https://new-console.ng.bluemix.net/devops/setup/deploy/?repository=https%3A//github.com//IBM-Bluemix/logistics-wizard-toolchain.git)

### Setting up code coverage tests

In order to utilize the code coverage tests in the pipelines, you need add your repos to [coveralls][coveralls_url] and get the generated repo token. Once you get these tokens, use these values in the GitHub section during the toolchain configuration. Coverage tests will not be reported if you leave these values blank.

### Setting up email environment variables

The TEST stage will make sure your app is capable of sending welcome emails. You need to set the corresponding environment variables by following the [Setting up email][email_instructions_url] section in the Logistics Wizard Controller README. Once you have your Gmail username and password, use these values in the Delivery Pipeline section during the toolchain configuration. Your controller app will be unable to send emails and corresponding tests will not be run if you leave these values blank.

---
### Learn more

* [Bluemix DevOps Services][bluemix_devops_url]
* [Bluemix Toolchains Documentation][toolchains_overview_url]
* [InterConnect 2016 video recording][toolchains_interconnect_video_url]

<!--Links-->
[bluemix_devops_url]: https://new-console.ng.bluemix.net/devops
[github_controller_url]: https://github.com/IBM-Bluemix/logistics-wizard-controller
[github_erp_url]: https://github.com/IBM-Bluemix/logistics-wizard-erp
[github_webui_url]: https://github.com/IBM-Bluemix/logistics-wizard-webui
[coveralls_url]: https://coveralls.io/
[email_instructions_url]: https://github.com/IBM-Bluemix/logistics-wizard-controller#setting-up-email
[toolchains_overview_url]: https://new-console.ng.bluemix.net/docs/toolchains/toolchains_overview.html
[toolchains_interconnect_video_url]: https://vimeo.com/156126035/8b04b8878a
