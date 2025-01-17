---
uid: AddConfigurationTemplate
---

# Add and edit configuration templates

You can create and edit configuration templates for systems in AVEVA Data Hub. Once the configuration is complete, export the configuration in a text file to manually apply it to the system in the field or to deploy it to the edge module using AVEVA Edge Management. You can also use an exported configuration text file as a template for configuring other systems by importing it. Default configurations are available for supported system types. The maximum size for a configuration file is 16 MB.

You can create configuration templates for the following system types:

 - AVEVA Adapter for Azure Event Hubs
 
 - AVEVA Adapter for BACnet 

 - AVEVA Adapter for DNP3

 - AVEVA Adapter for Azure Event Hubs
 
 - AVEVA Adapter for BACnet 

 - AVEVA Adapter for DNP3

 - Edge Data Store

 - AVEVA Adapter for Modbus TCP
 
 - AVEVA Adapter for MQTT

 - AVEVA Adapter for OPC UA

 - AVEVA Adapter for RDBMS

 - AVEVA Adapter for Structured Data Files

**Note:** You can only deploy edge modules using AVEVA Edge Management. 

The `namespaceId` in the data and health endpoint URLs defaults to the namespace where the configuration template is created. For example, if the namespace of the configuration template is MyData, the endpoint URL would be `https://website.com/api/v1/Tenants/{tenantId}/Namespaces/MyData/Omf`.

## Edge module configuration

For edge modules, use variables to denote secrets in configuration files. Variables must be used within the configuration file in place of actual secret and password values. Use the following variables as required for your specific configuration:

  - `{{EgressEndpointSecret}}` - Use this variable for the secret or password value to connect to the egress endpoint. When sending data to AVEVA Data Hub, use this variable in place of the client secret. When sending data to PI Web API, use this variable in place of the password.
  
  - `{{AdditionalEgressEndpointSecret}}` - Use this variable when egressing data to more than one endpoint, when the other endpoint requires a different secret or password. 
  
  - `{{DataSourceSecret}}` - Use this variable in place of a data source password when the data source you are connecting to requires a password in order to connect.
  
  - `{{AdditionalDataSourceSecret}}` - Use this variable when connecting to more than one data source, when the other data source requires a different password in order to connect.

When you deploy the configuration in AVEVA Edge Management, you define values for the variables and securely transfer those values to the device. For more information, see [Deploy an edge module](xref:DeployModule).


## Add a new configuration template

To create a system configuration template and export it for use:

1. In the left pane, select **Data Collection** > **Edge Data Store & Adapters**.

1. Verify that the **Systems/Configuration Templates** selector is set to **Configuration Templates**.

1. Select **New Configuration Template**.

1. In the **Configuration Template Name** field, enter a name to identify the configuration.

1. In the **Type** and **Version** fields, select the system type and version for which to create the configuration.

   The default configuration for the selected system type displays.

1. To import a configuration, select **Import Configuration**, then browse to the JSON file that contains the configuration, and select **Import**.

1. (Optional) In the **Section Select** dropdown list, select the section of the configuration to modify. The default option of `JSON Configuration` shows the entire configuration.

1. Modify the JSON as needed. For configuration guidelines, refer to the specific system documentation.

   **WARNING:** For security reasons, do not include secrets in the configuration. Secrets cannot be stored or exported in a configuration. For edge modules, variables must be used within the configuration file in place of actual secret and password values. For more details, see the [Configure a Module](https://edgemanagement.connect.aveva.com/help/#/home/665922/10/11) topic in the AVEVA Edge Management documentation.

   Errors in the JSON syntax are underlined. To see an explanation of the issue, hold the mouse over the underlined text. The overall status of the JSON syntax is displayed over the right pane.  

1. To export the completed configuration, do one of the following:

   - To export just the selected section, select **Export Section** in the right pane. 

   - To export the entire configuration in one file, select **Export Configuration**.

   The JSON file is downloaded to your browser.

1. When you have finished, select **Save & Close**.

1. Select **Save & Close** to confirm the changes. 

## Edit an existing configuration template

To modify a configuration template and export it for use:

1. In the left pane, select **Data Collection** > **Edge Data Store & Adapters**.

1. Verify that the **Systems/Configuration Templates** selector is set to **Configuration Templates**.

1. Find and select the configuration template to modify.

1. (Optional) To search for specific configuration templates, select the **Search for Configuration Templates** search bar. The search function provides examples for filtering by criteria such as device name and version. For more information, read [Search in AVEVA Data Hub](xref:Search).

1. In the right pane, select the edit icon ![Edit](../../../_icons/default/pencil.svg).

1. Modify the configuration template name, **Type**, and **Version** as needed.

1. (Optional)  In the **Section Select** dropdown list, select the section of the configuration to modify. The default option of `JSON Configuration` shows the entire configuration.

1. Modify the JSON as needed. For configuration guidelines, refer to the specific system documentation.

  **WARNING:** For security reasons, do not include secrets or passwords in the configuration. Secrets and passwords cannot be stored or exported in a configuration. Client secrets and passwords must be applied directly on the device. For edge modules, variables must be used within the configuration file in place of actual secret and password values. For more details, see the [Configure a Module](https://edgemanagement.connect.aveva.com/help/#/home/665922/10/11) topic in the AVEVA Edge Management documentation

  Errors in the JSON syntax are underlined. To see an explanation of the issue, hold the mouse over the underlined text. The overall status of the JSON syntax is displayed over the right pane.  

1. To export the completed configuration, do one of the following:

   - To export just the selected section, select **Export Section** in the right pane. 

   - To export the entire configuration in one file, select **Export Configuration**. 

   The JSON file is downloaded to your browser.

1. When you have finished, select **Save & Close**.

1. To confirm the changes, select **Save & Close**. 
