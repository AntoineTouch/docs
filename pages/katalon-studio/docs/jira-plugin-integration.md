---
title: "Jira Integration"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/jira-plugin-integration.html

description:
---

Prerequisites:
* Install [Jira Integration plugin](https://store.katalon.com/product/3/Jira-Integration) for Katalon Studio from Katalon Store.
* Install [Katalon BDD app](https://marketplace.atlassian.com/apps/1217501/katalon-bdd-test-automation-for-jira) for Jira from Atlassian Marketplace.

## Configuration (Jira Cloud)

You need to enable JIRA Integration in order to submit issues to JIRA. This setting is available at **Project > Settings > Integration > JIRA**.

![](../../images/katalon-studio/docs/jira-plugin-integration/config.png)
1.  Select **Enable integration** option. The settings will be available for configuration.

**Jira Cloud**
* *Server URL* must be in the form *https://<site_name>.atlassian.net*.
* Use a Atlassian Cloud's API token for *Password*. See instructions [here](https://confluence.atlassian.com/cloud/api-tokens-938839638.html).

**Jira Server**
* *Server URL* must be in the form *http(s)://domain* without any trailing parts e.g. */secure*.
* Use username instead of email for *Username*.

2.  Specify information regarding your JIRA Server and login credential then click **Connect** button.


3.  After successfully authenticating with JIRA, all relevant **JIRA Projects** and **Issue Types** will be retrieved and displayed under **Submit Options**. You can specify the default project and issue type for submission here. These settings will be used when you submit a new issue manually from Katalon Studio test report.

![](../../images/katalon-studio/docs/jira-plugin-integration/image2016-11-3-133A533A20.png)


4.  Click **OK** button to complete the JIRA Integration setup.

## Integrate Test Case

1. Prepare [ Jira JQL Script]( https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-764478330.html )
![](../../images/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A393A33.png)

2. Open **Jira Integration** > click Import Test Case from JIRA JQL
![](../../images/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A233A49.png)

3. Enter the Jira JQL. Click **OK**.
![](../../images/katalon-studio/docs/jira-plugin-integration/image2017-8-2-113A413A34.png)

4. The **Test Case Folder Selection** window will appear. Choose the destination to store the issues. Click **OK**.
![](../../images/katalon-studio/docs/jira-plugin-integration/save_test_cases.png)

5. The **Jira Issues** window will appear. Click **OK**.
![](../../images/katalon-studio/docs/jira-plugin-integration/image2016-11-3-143A413A132.png)

If your test cases have already been linked to a JIRA ticket, Katalon Studio will not sync them again.

## Import BDD Feature Files

**Jira Integration** also allows you to import Jira BDD Feature Files to Katalon Studio.

When importing test cases from Jira, please check **Link to BDD Feature File** &gt; **OK** &gt; Choose the destination to store the issues.

![](../../images/katalon-studio/docs/jira-plugin-integration/sample.png)

A new Feature File (with the same name as the test case) will be created with the content from Jira BDD. Moreover, a RunFeature step will be created in the linked test case to Jira.

![](../../images/katalon-studio/docs/jira-plugin-integration/bdd2.png)

## View Test Results on Jira

After you have successfully integrated test cases, test execution results will be automatically created in the associated Jira ticket. Review the status and attachments of Katalon Studio test cases right inside Jira.

![](../../images/katalon-studio/docs/jira-plugin-integration/image2017-8-2-173A563A40.png)

## Submit an Issue to Jira

_Note_: this feature supports Test Suite and Test Suite Collection execution level
Submit options will be available in your test reports after **Jira Integration** has been set up.

1. In your reports, open a test execution
![](../../images/katalon-studio/docs/jira-plugin-integration/image2017-2-22-103A03A4.png)

2. Select the test case results to be reported
![](../../images/katalon-studio/docs/jira-plugin-integration/image2016-11-3-143A153A20.png)

3. Click on the bug icon to manage Jira issues
![](../../images/katalon-studio/docs/jira-plugin-integration/image2016-11-3-143A163A50.png)

4. (Optional) In Jira's Login screen, select *Remember my login on this computer* to let the browser remember the session so that logging in will not be required next time.

5. Create a new issue and submit
![](../../images/katalon-studio/docs/jira-plugin-integration/image2016-11-3-143A323A53.png)

