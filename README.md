# Introduction 
This SharePoint extension or webpart enables a user to enter a keyword, e.g. "How do you feel today?". By using keywords,
users can re-use terms entered previously by anyone. The keyword is stored in a minimalistic list with keywords enabled.

## Description
The label is the displayname of the "Enterprise Keyword" colummn. The hint text is the description. To chnage those:
- open the list settings
- Click on the column "Enterprise Keywords"
- Change the column name, e.g. "Feedback", this is the display value shown to the user, the internal name will remain intakt
- Change the description, e.g. "How do you feel?" or "On your mind?"

# Table of contents
1. [Getting Started](#getting-started)
    1. [Requirements](#requirements)
    2. [Minimal path to awesomeness](#minimal-path-to-awesomeness)
3. [Build and install](#build-and-install)
4. [Contribute](#contribute)
    1. [To do list](#to-do-list)
5. [Create new project](#create-new-project)

# Getting Started
You can use the "Minimal path to awesomeness" to have look around. Please branch before contributing.
You can follow the "Create a new project" to start with a copy of this a starting point for a new project (usually app)

## Requirements
You should have the following installed:
- Visual Studio Code (or similar)
- Node 14
- yarn
- git
- GitExtension (the program, if your contributing or forking a new project of this)

## Minimal path to awesomeness
```
yarn global add lerna
git clone --recurse-submodules https://github.com/mauriora/Keyword-Feedback-Solution.git
cd webpart-keyword-feedback
lerna bootstrap
yarn build-shared
```
### either serve the webpart
```
yarn serve-webpart
```
and:
- [browse to the workbench on *YOUR-SITE*](https://YOUR-DOMAIN.sharepoint.com/sites/YOUR-SITE/_layouts/15/workbench.aspx)
- add the webpart to the page

### or serve the extension
- edit app/Keyword-Feedback-Extension/config/serve.json
- run:
```
yarn serve-extension
```


# Build and install
1. In a solution terminal execute `yarn workspace @mauriora/webpart-example serve`
2. [browse to the sharepoint app store on *YOUR-TENANT*](https://YOUR-TENANT.sharepoint.com/sites/apps/AppCatalog/Forms/AllItems.aspx)
3. Click **Upload**
4. Click **Choose files**
5. Navigate to *YOUR-SOLUTION*/apps/*YOUR-PROJECT*/sharepoint/solution
6. Select *YOUR-PROJECT*.sppkg and click **Open**
7. Add a comment and click **OK**
8. Wait for the upload to finish and a dialog to open
9. If you want the webpart to be available on all sites without installing, tick **Make this solution available to all sites in the organization**, otherwise it needs to be installed on each site using
10. Click **Deploy**
11. grant API permissions in [Sharepoint Admin Center: Advanced / API access](https://YOUR-DOMAIN-admin.sharepoint.com/_layouts/15/online/AdminHome.aspx#/webApiPermissionManagement)
12. If not installed tenant wide, go to each site you wnat the webpart on
    1. Go to *Site Content*
    2. Click **+ New** -> **App**
    3. Find *YOUR-APP* and click on it
    4. Wait until it's installed
13. Create a page and add **YOUR-WEBPART**

# Contribute
Use the minmal path to awesomeness and please create a branch for your contribution.
Then do a pull request to merge your branch into the main branch.
