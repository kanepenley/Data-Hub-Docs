---
uid: remove-agent-portal
---

# Remove an agent

You remove a PI to Data Hub Agent by first uninstalling it from the host machine and then the portal. There are two parts to removing an agent:

* Step 1: Uninstall the agent from the host machine

* Step 2: Remove the agent listing in AVEVA Data Hub  

## Step 1: Uninstall the PI to Data Hub Agent on the host machine

To remove the PI to Data Hub Agent application from a host machine, uninstall it from the `Apps & features` window and then follow the prompts in the `PI to Data Hub Agent` window.

To remove the PI to Data Hub agent from the host machine:

1. Select Windows **Start**, then select **Settings** > **Apps** > **Apps & features**.

1. In the `Apps & features` window, select **PI to Data Hub Agent** in the list of installed apps.
 
1. Select **Uninstall** twice, then select **Yes** in the `User Account Control` window.

1. In the `PI to Data Hub Agent (Administrator)` window, select the **Uninstall** option, then select **Next**.

1. Select the **Unregister agent from Data Hub** option, then select **Next**.

   The agent's associated client and connection information is also removed from AVEVA Data Hub during the uninstall process.

   **Note:** After uninstalling the agent from the host machine, you still need to remove the agent from the portal. 

1. Select the user account to use to log on, then close the browser window.<!--AF 11/16/21 When did a browser window open?-->

1. On the `PI to Data Hub Agent` window, select **Uninstall**, then select **Close**.

   The PI to Data Hub Agent application is uninstalled on the host machine.

## Step 2: Remove the PI to Data Hub Agent on the portal

After uninstalling an agent from a host machine, you also need to remove it from the portal.

To remove an agent from the portal:

1. In the left pane, select **Data Collection** > **PI to Data Hub Agents**.

1. In the `PI to Data Hub Agents` window, select an agent in the list.

1. Select **Remove Agent**.

1. On the `Remove Agent` window, select **Remove**.

   The agent is removed in the portal.
