---
sidebar_position: 1
sidebar_label: 'Create Project / Application'
---

# Azure DevOps

Hands-on Lab Script - Part 1

## Create Project / Application sample

Use Azure DevOps Starter <https://portal.azure.com/#blade/HubsExtension/BrowseResource/resourceType/microsoft.visualstudio%2Faccount%2Fproject>

- Select `Create DevOps Starter`

![](Images/TPDevOpsStarter1.png)

- If you see the message on screen "Setting up DevOps starter with GitHub, change settings here" - click on link and change to use Azure DevOps

![](Images/TPDevOpsStarter2.png)

- Create a .NET project ... suggest use Windows AppService F1 free tier
  - Choose `.NET` | [Next]
  - Choose `ASP.NET Core` | [Next]
  - Choose `Windows Wep App` | [Next]
  - Enter details - webapp name must be unique, use local regions
  - Use the [Additional Settings] - select F1 free tier
  - [Done]

![](Images/TPCreate1.png)

![](Images/TPCreate1a.png)

![](Images/TPCreate1b.png)

![](Images/TPCreate1c.png)

When the project has been provisioned, the following has happenend:

- a sample application is stored in a Azure DevOps repo
- infrastructure as code ARM template is stored in the same Azure DevOps repo (different top level folder)
- build and release pipelines are generated, and invoked
- an Azure DevOps Project dashboard is generated.

![](Images/TPCreate2.png)

Note on the Azure DevOps Project dashboard links to the AzureDevs homepage, repos, pipelines and boards.

![](Images/TPCreate3.png)

![](Images/TPCreate3a.png)

The website has been deployed on Azure App Service

![](Images/TPCreate4.png)

## Build Pipelines - Automated Testing

Also note on the Azure DevOps Project dashboard that the pipelines did some automated testing.

In the Build pipeline there was one unit test executed and this passed successfully.

![](Images/TPBuild1.png)

![](Images/TPBuild2.png)

![](Images/TPBuild3.png)

![](Images/TPBuild4.png)

![](Images/TPBuild5.png)

## Release Pipelines - Automated Testing

Also in the Release pipeline, there was one functional test executed and this passed successfully.

![](Images/TPRelease1.png)

![](Images/TPRelease2.png)

![](Images/TPRelease3.png)

## Amend Pipelines

Make the following change to the Release pipeline ... this will be useful later.

- Select [Edit]

![](Images/TPEditRelease1.png)

- Select [Options]

![](Images/TPEditRelease2.png)

- Enable the Integrations :

  - Report deployment status to the repository host
  - Report deployment status to Work
  - Report deployment status to Boards
  - Enable the deployment status badge

- [Save]

![](Images/TPEditRelease3.png)

## Create WorkItems

Next we will create a User Story with two Tasks and two Test Cases.

- Go to WorkItems
- Create Story

![](Images/TPCreateStory1.png)

![](Images/TPCreateStory2.png)

- Go to Boards

![](Images/TPCreateStory3.png)

- Create two tasks:

![](Images/TPCreateTask1.png)

![](Images/TPCreateTask2.png)

- Create two test cases:

![](Images/TPCreateTestCase1.png)

![](Images/TPCreateTestCase2.png)

- Move story to Active

![](Images/TPStoryActive.png)

- Goto Backlogs
- Move story to iteraction 1

![](Images/TPStorySprint1.png)

![](Images/TPStorySprint2.png)

- On the iteration, click `Set Dates` and allocate a three week period

![](Images/TPStorySprint3.png)

## Add .NET SDK

It is possible to amend the version of .NET used.   This is not currently required for the lab - but may be needed if things change.

![](Images/TPAddSDK.png)

## Summary

In this section we created our DevOps project and set up some work items.

In the next section we shall take on the persona of a developer, and make some code changes that relate to the work items.

