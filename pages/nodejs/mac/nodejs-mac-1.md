---
layout: page-steps
language: Node.js
title: macOS
permalink: /node/mac/
redirect_from:
  - /node/
  - /node/mac/step/
  - /node/mac/step/1
---

> In this section, you will get SQL Server 2017 running on Docker. After that you will install the necessary dependencies to create Node.js apps with SQL Server

## Step 1.1 Install SQL Server

{% include partials/install_sql_server_mac.md %}

## Step 1.2 Install Homebrew and Node.js

1. Install Homebrew.

    {% include partials/install_homebrew.md %}

2. Restart the terminal session.

3. Install Node.js

    ```terminal
      brew install node
    ```
    
    ```results
      ==> Downloading https://homebrew.bintray.com/bottles/node-6.7.0.el_captian.bottle.tar.gz
      ################################################################## 100.0%
      ==> Pouring node-6.7.0.el_captian.bottle.tar.gz
      ...
      ==> Using the sandbox
      ==> Caveats
      Please note by the default...
      ...
      ==> Summary
      /usr/local/Cellar/node/6.7.0: 3,669 files, 40.8M
    ```
> You now have Node.js installed! The next section will walk you through getting the tools to interact with your database.

## Step 1.3 Install the ODBC Driver and SQL Command Line Utility for SQL Server

{% include partials/install_sqlcmd_mac.md %}
    
> You have successfully installed SQL Server Command Line Utilities on macOS. You now have everything you need to start writing Node.js apps with SQL Server!
