# splunk-cloud-version-control
Version Control for your SplunkCloud Instance

Endpoints
| No. | Active    | Category             | Title                                | Description                                         | Command                                                                   |
|-----|-----------|----------------------|--------------------------------------|-----------------------------------------------------|---------------------------------------------------------------------------|
| 1   | X         | Access Control       | User Roles                           | All user roles and permissions                      | `\| rest splunk_server=local /servicesNS/-/-/authorization/roles`           |
| 2   | X         | Access Control       | User Accounts                        | Information about user accounts                     | `\| rest splunk_server=local /servicesNS/-/-/authentication/users`          |
| 3   | X         | Applications         | Apps Installed                       | List of all installed apps                          | `\| rest splunk_server=local /servicesNS/-/-/apps/local`                    |
| 4   |           | Clusters             | Search Head Clusters                 | Information about search head clusters              | `\| rest splunk_server=local /services/shcluster/captain/members`           |
| 5   |           | Clusters             | Indexer Clusters                     | Information about indexer clusters                  | `\| rest splunk_server=local /services/cluster/master/peers`                |
| 6   |           | Configuration        | Server Settings                      | Retrieves general server settings                   | `\| rest splunk_server=local /services/server/settings`                     |
| 7   |           | Configuration        | Configuration Files                  | Retrieves settings from configuration (.conf) files | `\| rest splunk_server=local /services/configs/conf-{filename}`            |
| 34  |           | Configuration        | limits.conf Settings                 | Retrieve settings from limits.conf                  | `\| rest splunk_server=local /services/configs/conf-limits`                 |
| 8   |           | Deployment           | Deployment Server                    | Information about the deployment server             | `\| rest splunk_server=local /services/deployment/server`                   |
| 9   |           | Inputs               | Data Inputs                          | All data input configurations                       | `\| rest splunk_server=local /servicesNS/-/-/data/inputs/all`               |
| 10  |           | Inputs               | Modular Inputs                       | Retrieves a list of modular inputs and configurations | `\| rest splunk_server=local /servicesNS/-/-/data/modular-inputs`          |
| 11  |           | Inputs               | HTTP Event Collector (HEC) Tokens    | Retrieves HEC token configurations                  | `\| rest splunk_server=local /servicesNS/-/-/data/inputs/http`             |
| 12  |           | Inputs               | Scripted Inputs                      | Retrieves configurations for scripted inputs        | `\| rest splunk_server=local /servicesNS/-/-/data/inputs/script`           |
| 13  | X         | Knowledge            | Index Definitions                    | All index definitions and properties                | `\| rest splunk_server=local /servicesNS/-/-/data/indexes`                  |
| 14  | X         | Knowledge            | Lookup Tables                        | List of lookup table files                          | `\| rest splunk_server=local /servicesNS/-/-/data/transforms/lookups`       |
| 15  | X         | Knowledge            | Lookup Definitions                   | Definitions of lookups                              | `\| rest splunk_server=local /servicesNS/-/-/data/transforms/lookups`       |
| 16  | X         | Knowledge            | Automatic Lookups                    | Configurations for automatic lookups                | `\| rest splunk_server=local /servicesNS/-/-/props/lookups`                 |
| 17  | X         | Knowledge            | Field Extractions                    | All field extraction rules and configurations      | `\| rest splunk_server=local /servicesNS/-/-/data/props/extractions`        |
| 18  | X         | Knowledge            | Field Aliases                        | All field alias configurations                      | `\| rest splunk_server=local /servicesNS/-/-/data/props/aliases`            |
| 19  | X         | Knowledge            | Source Types                         | All source type configurations                      | `\| rest splunk_server=local /servicesNS/-/-/data/props/sourcetypes`        |
| 20  | X         | Knowledge            | Macro Definitions                    | Definitions of all macros                           | `\| rest splunk_server=local /servicesNS/-/-/admin/macros`                  |
| 21  |           | Licensing            | License Information                  | Details about the Splunk license                    | `\| rest splunk_server=local /services/licenser/licenses`                   |
| 22  |           | Licensing            | License Usage                        | Retrieves license usage data                        | `\| rest splunk_server=local /services/licenser/usage`                      |
| 23  |           | Outputs              | System Messages                      | Retrieves system messages                           | `\| rest splunk_server=local /services/messages`                            |
| 24  | X         | Search               | Saved Searches                       | Every saved search including query and settings     | `\| rest splunk_server=local /servicesNS/-/-/saved/searches`                |
| 25  | X         | Search               | Event Types                          | All event type definitions                          | `\| rest splunk_server=local /servicesNS/-/-/saved/eventtypes`              |
| 26  |           | Search               | Scheduled Reports                    | All scheduled reports and configurations            | `\| rest splunk_server=local /servicesNS/-/-/scheduled/views`               |
| 27  |           | Search               | Alerts                               | All alerts and configurations                       | `\| rest splunk_server=local /servicesNS/-/-/alerts`                        |
| 28  |           | System               | Firewall Traffic                     | Retrieves information about firewall traffic        | `\| rest splunk_server=local /services/firewall/traffic`                    |
| 29  | X         | User Interface       | Dashboards                           | All dashboards and XML configurations               | `\| rest splunk_server=local /servicesNS/-/-/data/ui/views`                 |
| 30  |           | User Interface       | Data Models                          | List of data models                                 | `\| rest splunk_server=local /servicesNS/-/-/datamodel/model`               |
| 31  | X         | User Interface       | Navigation Menus                     | Configuration of navigation menus                   | `\| rest splunk_server=local /servicesNS/-/-/data/ui/nav`                   |
| 32  |           | User Preferences     | User Preferences                     | User-specific preferences and settings              | `\| rest splunk_server=local /servicesNS/-/-/admin/user-prefs`              |
| 33  |           | Workload Management  | Search Head Clusters                 | Information about search head clusters              | `\| rest splunk_server=local /services/shcluster/captain/members`           |

* Splunk REST API Endpoints reference list: [https://docs.splunk.com/Documentation/Splunk/9.1.2/RESTREF/RESTlist](https://docs.splunk.com/Documentation/Splunk/9.1.2/RESTREF/RESTlist)
