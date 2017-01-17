# Logistics Wizard Toolchain

This toolchain will allow you to deploy the entire [Logistics Wizard](https://github.com/IBM-Bluemix/logistics-wizard) demo system, which is a supply chain management web application composed of several microservices:  
- [Controller][github_controller_url] - The API that sits on the edge of the architecture and interfaces with all other services.  
- [ERP][github_erp_url] - An API that handles user login and interaction with the ERP system objects.  
- [WEBUI][github_webui_url] - The Web UI that is the web front end of the entire application, built using React.
- [Weather Recommandation][github_recommendation_url] - Makes shipment recommendations based on weather conditions

## Create the toolchain

1. If you don't already have one, [sign up for a Bluemix account](https://bluemix.net/).

1. Ensure you have 2GB of free memory and space for 4 additional services in your organization.

1. It is recommended to [create a new space](./assets/manage-organizations.png) in your organization. This helps grouping the apps and services together in the console.

1. **To get started, click this button:**

  [![Deploy To Bluemix](./.bluemix/create_toolchain_button.png)](https://new-console.ng.bluemix.net/devops/setup/deploy/?repository=https%3A//github.com//IBM-Bluemix/logistics-wizard-toolchain.git)

  > :warning: Make sure to pick unique application names in the Delivery Pipeline step.

The toolchain is preconfigured for:

- issue tracking
- source control
- continuous delivery and integration (CI/CD)
- unit and code coverage testing
- blue-green deployment

### Setting up code coverage tests

In order to utilize the code coverage tests in the pipelines, you need add your repos to [coveralls][coveralls_url] and get the generated repo token. Once you get these tokens, use these values in the GitHub section during the toolchain configuration. Coverage tests will not be reported if you leave these values blank.

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
[github_recommendation_url]: https://github.com/IBM-Bluemix/logistics-wizard-recommendation
[coveralls_url]: https://coveralls.io/
[toolchains_overview_url]: https://new-console.ng.bluemix.net/docs/toolchains/toolchains_overview.html
[toolchains_interconnect_video_url]: https://vimeo.com/156126035/8b04b8878a
