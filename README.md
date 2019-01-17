## Microsoft Open Source Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# dynamics365smb-docs
Welcome to the repository for user assistance content for Microsoft Dynamics 365 Business Central! This repo enables you to take the Business Central Help and customize it to suit your application. It also provides a way for you to actively contribute to the current Business Central content.  

The content is available as markdown files (.md), where each file represents an article in the help. You can edit these markdown files, and then convert them to HTML files for application.

There are different repos in GitHub for the source content and each of the languages that Microsoft translates to. The *dynamics365smb-docs* repo contains the content in English (US). If you want access to the content in other languages, navigate to the relevant repo - the names follow this pattern: `dynamics365smb-docs-pr.<language>-<country>`, such as [dynamics365smb-docs-pr.da-DK](https://github.com/MicrosoftDocs/dynamics365smb-docs-pr.da-DK) for the Danish version.

**NOTE**: Microsoft accepts pull requests to the *dynamics365smb-docs* repo only, not the language-specific repos. If you have feedback about translations, you can report a GitHub issue in the relevant repo.

For guidance about extending and customizing the Microsoft-provided content for Business Central, see [Configuring the Help Experience for Dynamics 365 Business Central](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/deployment/configure-help) and [Dynamics 365 Business Central User Assistance Model](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/user-assistance). If you have any questions, you can contact the Dynamics SMB Content Experience (UA) team at nav-olh@microsoft.com.

## Getting Started

1. Fork this repo

    You cannot work directly in the dynamics365smb-docs repo, so the first thing you need to do is create a fork of the repo under your GitHub account. A fork basically is copy of this repo that lets you work freely on the content without affecting the dynamics365smb-docs repo. For more information, see [Fork a Repo](https://help.github.com/articles/fork-a-repo/).

2.  Install GitHub Desktop (optional) and clone your forked repo.

    GitHub Desktop makes is easy to work and collaborate with repos locally from your own desktop. For more information, see [GitHub Desktop](https://desktop.github.com/).   

2. Get hold of your favorite MarkDown editor, and start making changes.

    The help content is stored in the articles folder of the repo. Articles use a syntax for formatting text called GitHub Flavored Markdown. To learn more about working with markdown, see [Getting started with writing and formatting on GitHub](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/).

You can also find guidance for how to get started with MarkDown in the [Docs Contributor Guide](https://docs.microsoft.com/en-us/contribute/), which is published by the team that built the Docs.microsoft.com site where the Business Central team publishes their docs.

### Contributing

A benefit of GitHub is the ability for you to contribute to the core content that the Microsoft team provides in the dynamics365smb-docs repo. For example, you might have a new article that you think would be beneficial or you might have a correction to an existing article. If you would like to contribute to the dynamics365smb-docs repo, you create what is called a *pull request* from your repo to the dynamics365smb-docs repo. The Microsoft team will then review the request and include the changes as appropriate.

For example, to create a pull request to the dynamics365smb-docs repo by using GitHub Desktop, do the following:

1.  Commit the changes to your repo that you want to include in the pull request.
2.  Choose **Sync** to push the changes up to your repo on GitHub.
3.  When the sync is completed, choose **Pull Request**, make sure that the pull request points at the *live* branch, and then choose send **Pull Request**.

**NOTE**: Microsoft accepts pull requests to the dynamics365smb-docs repo only, not the language-specific repos. If you have feedback about translations, you can report a GitHub issue in the relevant repo.

You can also find tips and tricks in the general contribution guide for the Docs site at [https://docs.microsoft.com/en-us/contribute/](https://docs.microsoft.com/en-us/contribute/).


## Authoring in Markdown

The content is styled using a Markdown syntax as described below..

### General info:
[Getting started with writing and formatting on GitHub](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/)

### Authoring tools:
If you want to work locally, you can edit using any text editor. Just save the file as a .md type. Here are a couple good tools that provide you with some nice features, such as Preview.  
- [Visual Studio Code](https://code.visualstudio.com/)
- [Atom](https://atom.io/) (this has spell check and is good for managing many files)

### Properties and tags
All topics must start with a YAML header with the following set of attributes.

```
---
title: 'Short title with a couple of buzzwords for the feature. Not the same as your heading for the topic. | Microsoft Docs'
description: 'A longer description that identifies the topic in search results.'
author: MyGitHubAccount
ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords:keyword1, keyword2
ms.date: MM/DD/YYYY

---
```

The ms.date tag must be updated to the date when you make the change. The ms.date property must follow the US date format of MM/DD/YYYY.

Some articles will have a different value for the ms.topic tag. For more information, see https://opsdocs.azurewebsites.net/en-us/opsdocs/partnerdocs/metadata?branch=master.

### Headings
Use ```#``` for headings.

Examples:
```#``` Heading 1, looks like:
# Heading 1

```##``` Heading 2, looks like:
## Heading 2

```###``` Heading 3, looks like:
### Heading 3


### Bulleted lists
Use - to create bullets, for example:

The following options are available:
```
- first option
- second option
- third option
```

### Ordered lists
Use numbers for ordered lists. No space between the lines, we'll let the template take care of that.

```
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.
2. In the **Payment Journal** window, on the first journal line, enter the relevant information about the payment entry.
3. To apply a single vendor ledger entry:
4. In the **Applies-to Doc. No.** field, choose the field to open the **Apply Vendor Entries** window.
```

### Bold and italics syntax
Use ```**bold**``` and ```*italics*```

### Tables
- For tables in the body, use the markdown syntax.

```
| To   | See                       |
|------|---------------------------|
|<text>|<link>|
| | |
| | |
```

- For nested tables in ordered and unordered lists use HTML-syntax. Markdown does not support tables very well. If you use the markdown syntax the list will be broken, the table will align left and list will be renumbered.

### Comment syntax
Useful for sections that are not ready and will not pass the build check.
```
<!-- Comments -->
```
Examples
```
<!-- [Managing Payables](payables-manage-payables.md)-->
<!-- This is a paragraph that spans more lines and I can just put the comment tag
at the beginning and end of it -->
```
### Links
Ordinary link to a different topic in the same folder

These links have the format ```[link text](filename.md)```.

Example:
```[Managing Payables](payables-manage-payables.md)```


### Link to a topic in a subfolder of the source topic

These links have the format ```[link text](subfolder/filename.md)```.

For example, you want to link to payables-manage-payables.md from ui-work-general-journals.md, where the folder structure is as follows:

- articles
    - ui-work-general-journals.md
- ManagePayables
    - payables-manage-payables.md

Here is the link:
```[Manage Payables](ManagePayables/payables-manage-payables.md)```

### Link to a topic in a different folder than source topic

These links have the format ```[link text](../folder/filename.md)```.

For example, you want to link to payables-manage-payables.md from receivables-manage-receivables.md, where the folder structure is as follows:

- articles
    - ManageReceivables
        - receivables-manage-receivables.md
    - ui-work-general-journals.md
    - ManagePayables
        - payables-manage-payables.md

Here is the link:
```[Manage Payables](../ManagePayables/payables-manage-payables.md)```

### Link to a place in the same article
From within an article, you can create a link to a specific heading in the same article. You can create the link like other links except with the following format:

```[link text](#target-heading)```

target-heading is the text of the heading that you want to link to, except it is all lowercase and spaces between words are replaced with hyphens. For example, here is the link:
```[How Autoscaling Works](#how-autoscaling-works)```

To the heading:
```## How Autoscaling Works```

### Link to a place in a different article
From an article, you can create a link to a specific heading in another article. You can create the link like other links except with the following format:

```[link text](targetarticlename#target-heading)```

targetarticlename is the file name of the article, including the .md file type.
target-heading is the text of the heading that you want to link to, except it is all lowercase and spaces between words are replaced with hyphens.

For example, to link to the heading "How Autoscaling Works" in the article Autoscaling.md", add the following code:
```[link text](Autoscaling.md#how-autoscaling-works)```

### Line breaks (soft return)
In the editor, add two blank spaces at the end of the sentence and hit return. This is used in the See Also list. (See Also must be heading 2.)

### Continue steps after a non-step para
Enter four spaces in front of the non-step para. Otherwise, the non-step para will restart the step sequence.

### TOC
The TOC structure of the TOC file is as follows:

```
#[Overview](overview.md)
 ##[Topic 1](topic-1.md)
 ##[Topic 2](topic-2.md)
 ##[Topic 3](topic-3.md)
 ##[Topic 4](topic-4.md)
```

### Standard Phrases
All fields in Business Central have tooltips. Therefore, do not document fields in Help. To refer readers to the tooltips, use this standard phrase where relevant:    
"Choose a field to read a short description of the field or link to more information."
For more information, see [Dynamics 365 Business Central User Assistance Model](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/user-assistance).

### Topic Titles
- Use imperative verb form for step-based topics ("Pay vendors").
- Use gerund verb form for conceptual, non-step topics. ("Paying Vendors")
- Use nouns for highest-level topics. ("Sales")

### File Naming

#### Rules
- No spaces or punctuation characters. Use hyphens to separate the words in the file name.
- Use all lowercase letters
- No more than 80 characters - this is a publishing system limit
- Use action verbs that are specific such as develop, buy, build, troubleshoot. No -ing words.
- No small words - don't include a, and, the, in, or, etc.
- All files must be in markdown and use the .md file extension.

#### Examples

|Topic title |Naming  |
|------------|--------|
|Select a Company|ui-how-select-company.md|
|Enter Criteria in Filters|ui-enter-criteria-filters.md|
|Troubleshooting: Record Locked by Another User|ui-troubleshoot-record-locked-another-user.md|
|Changing Basic Settings|ui-change-basic-settings.md|
|Sales|sales-manage-sales.md|
|Set Up Currencies|finance-setup-currencies.md|
|Set Up Purchasers|purchases-how-setup-purchasers.md|
|Understanding Session Timeouts|admin-understand-session-timeouts.md|
|Manage Data Encryption|admin-manage-data-encryption.md|

### Country-specific content
To simplify content localization and translation, country-specific articles live in country-specific folders. The TOC entries live under the "Local Functionality" parent node.
