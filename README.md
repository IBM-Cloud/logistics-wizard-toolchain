# Logistics Wizard Toolchain

This toolchain allows to deploy the [Logistics Wizard](https://github.com/IBM-Bluemix/logistics-wizard) sample application, which is a supply chain management web application composed of several micro-services. Refer to the [parent project](https://github.com/IBM-Bluemix/logistics-wizard) for details.

It includes four modules:  
- [Controller][github_controller_url] - The API that sits on the edge of the architecture and interfaces with all other services.  
- [ERP][github_erp_url] - An API that handles user login and interaction with the ERP system objects.  
- [WEBUI][github_webui_url] - The Web UI that is the web front end of the entire application, built using React.
- [Weather Recommandation][github_recommendation_url] - Makes shipment recommendations based on weather conditions

The toolchain is preconfigured for:
- issue tracking
- source control
- continuous delivery and integration (CI/CD)
- unit and code coverage testing
- blue-green deployment

## Deploy the toolchain in IBM Bluemix

1. Ensure you have a [GitHub](https://github.com/) account.

1. Ensure you have a [Bluemix](https://ibm.com/bluemix) account.

1. Ensure you have 2GB of free memory and space for 4 additional services in your Bluemix organization.

1. It is recommended to create a new space named `logistics-wizard` in your Bluemix organization. This helps grouping the apps and services together in the console.

1. **To get started, click this button:**

  [![Deploy To Bluemix](./.bluemix/create_toolchain_button.png)](https://new-console.ng.bluemix.net/devops/setup/deploy/?repository=https%3A//github.com//IBM-Bluemix/logistics-wizard-toolchain.git)

1. Give a name to your toolchain. This name is used as the prefix for the deployed applications. The name must be unique within your organization.

  > A simple trick is to use your name or initials or to leave the default generated name.

1. Select the GitHub box.

1. Optionally change the name of the GitHub repositories that will be created in your GitHub account.

  > You can choose to fork the main repositories so that you can import changes as they become available or to clone the repositories.

1. Select the Delivery Pipeline box.

1. Ensure the app names are unique.

1. Select the region, organization and space where you want to deploy the application.

1. Set your OpenWhisk Authorization Key. You can find your OpenWhisk key in the [Bluemix console here](https://console.ng.bluemix.net/openwhisk/cli). When doing so, make sure you are in the same region/organization/space where you are deploying the apps. The authorization key is specific to a given space. In the CLI configuration page, the authorization key is after the `--auth` parameter. As example in the following, the authorization key is `1234-4567-8901-2345:tonywinBtm00001112221`:

  ```
  wsk property set --apihost openwhisk.ng.bluemix.net --auth 1234-4567-8901-2345:tonywinBtm00001112221
  ```

1. You can leave the [coveralls][coveralls_url] tokens empty - this is really needed only for the main deployment we do in our team.

1. Click Create

1. Once the toolchain is created, you will end up with several delivery pipelines for all applications in the sample. Wait for the pipelines to deploy all the apps. You can open all pipelines in new browser tabs to follow the deployments or you can wait for all apps to be ready in the Bluemix dashboard.

1. Your apps are deployed. Head over the [walkthrough](https://github.com/IBM-Bluemix/logistics-wizard/blob/master/WALKTHROUGH.md) for a tour of the app.

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
