# splunk-cloud-version-control
Version Control for your SplunkCloud Instance

## Endpoint Overview


| No. | Active    | Category             | Title                                | Description                                         | Command                                                                   |
|-----|-----------|----------------------|--------------------------------------|-----------------------------------------------------|---------------------------------------------------------------------------|
| 1   | X         | Access Control       | User Roles                           | All user roles and permissions                      | `\| rest splunk_server=local /servicesNS/-/-/authorization/roles`           |
| 2   | X         | Access Control       | User Accounts                        | Information about user accounts                     | `\| rest splunk_server=local /servicesNS/-/-/authentication/users`          |
| 3   | X         | Applications         | Apps Installed                       | List of all installed apps                          | `\| rest splunk_server=local /servicesNS/-/-/apps/local`                    |
| 4   |           | Clusters             | Search Head Clusters                 | Information about search head clusters              | `\| rest splunk_server=local /services/shcluster/captain/members`           |
| 5   |           | Clusters             | Indexer Clusters                     | Information about indexer clusters                  | `\| rest splunk_server=local /services/cluster/master/peers`                |
| 6   |           | Configuration        | Server Settings                      | Retrieves general server settings                   | `\| rest splunk_server=local /services/server/settings`                     |
| 7   |           | Configuration        | Configuration Files                  | Retrieves settings from configuration (.conf) files | `\| rest splunk_server=local /services/configs/conf-{filename}`            |
| 8   |           | Configuration        | limits.conf Settings                 | Retrieve settings from limits.conf                  | `\| rest splunk_server=local /services/configs/conf-limits`                 |
| 9   |           | Deployment           | Deployment Server                    | Information about the deployment server             | `\| rest splunk_server=local /services/deployment/server`                   |
| 10  |           | Inputs               | Data Inputs                          | All data input configurations                       | `\| rest splunk_server=local /servicesNS/-/-/data/inputs/all`               |
| 11  |           | Inputs               | Modular Inputs                       | Retrieves a list of modular inputs and configurations | `\| rest splunk_server=local /servicesNS/-/-/data/modular-inputs`          |
| 12  |           | Inputs               | HTTP Event Collector (HEC) Tokens    | Retrieves HEC token configurations                  | `\| rest splunk_server=local /servicesNS/-/-/data/inputs/http`             |
| 13  |           | Inputs               | Scripted Inputs                      | Retrieves configurations for scripted inputs        | `\| rest splunk_server=local /servicesNS/-/-/data/inputs/script`           |
| 14  | X         | Knowledge            | Index Definitions                    | All index definitions and properties                | `\| rest splunk_server=local /servicesNS/-/-/data/indexes`                  |
| 16  | X         | Knowledge            | Lookup Definitions                   | Definitions of lookups                              | `\| rest splunk_server=local /servicesNS/-/-/data/transforms/lookups`       |
| 17  | X         | Knowledge            | Automatic Lookups                    | Configurations for automatic lookups                | `\| rest splunk_server=local /servicesNS/-/-/props/lookups`                 |
| 18  | X         | Knowledge            | Field Extractions                    | All field extraction rules and configurations       | `\| rest splunk_server=local /servicesNS/-/-/data/props/extractions`        |
| 19  | X         | Knowledge            | Field Aliases                        | All field alias configurations                      | `\| rest splunk_server=local /servicesNS/-/-/data/props/aliases`            |
| 20  | X         | Knowledge            | Source Types                         | All source type configurations                      | `\| rest splunk_server=local /servicesNS/-/-/data/props/sourcetypes`        |
| 21  | X         | Knowledge            | Macro Definitions                    | Definitions of all macros                           | `\| rest splunk_server=local /servicesNS/-/-/admin/macros`                  |
| 22  | X         | Knowledge            | Tags                                 | Tag configurations                                  | `\| rest splunk_server=local /servicesNS/-/-/configs/conf-tags`             |
| 23  | X         | Knowledge            | Calculated Fields                    | Field calculations based on other fields            | `\| rest splunk_server=local /servicesNS/-/-/data/props/calcfields`         |
| 24  |           | Knowledge            | Alert Actions                        | Configurations for alert actions                    | `\| rest splunk_server=local /servicesNS/-/-/saved/alert_actions`           |
| 25  | X         | Knowledge            | Field Transformations                | Field transformation configurations                 | `\| rest splunk_server=local /servicesNS/-/-/data/transforms/extractions`   |
| 26  |           | Knowledge            | Workflow Actions                     | Workflow action configurations                      | `\| rest splunk_server=local /servicesNS/-/-/data/ui/workflow-actions`      |
| 27  |           | Knowledge            | Panels                               | Panel configurations                                | `\| rest splunk_server=local /servicesNS/-/-/data/ui/panels`                |
| 28  |           | Knowledge            | Source Type Renaming                 | Source type renaming configurations                 | `\| rest splunk_server=local /servicesNS/-/-/data/props/sourcetype-rename`  |
| 29  | X         | Knowledge            | Collections                          | KV Store collection configurations                  | `\| rest splunk_server=local /servicesNS/-/-/storage/collections/config`    |
| 30  |           | Knowledge            | ViewState                            | View state configurations                           | `\| rest splunk_server=local /servicesNS/-/-/configs/conf-viewstates`       |
| 31  |           | Knowledge            | Times                                | Time-related configurations                         | `\| rest splunk_server=local /servicesNS/-/-/configs/conf-times`            |
| 32  |           | Licensing            | License Information                  | Details about the Splunk license                    | `\| rest splunk_server=local /services/licenser/licenses`                   |
| 33  |           | Licensing            | License Usage                        | Retrieves license usage data                        | `\| rest splunk_server=local /services/licenser/usage`                      |
| 34  |           | Outputs              | System Messages                      | Retrieves system messages                           | `\| rest splunk_server=local /services/messages`                            |
| 35  | X         | Search               | Saved Searches                       | Every saved search including query and settings     | `\| rest splunk_server=local /servicesNS/-/-/saved/searches`                |
| 36  | X         | Search               | Event Types                          | All event type definitions                          | `\| rest splunk_server=local /servicesNS/-/-/saved/eventtypes`              |
| 37  |           | Search               | Scheduled Reports                    | All scheduled reports and configurations            | `\| rest splunk_server=local /servicesNS/-/-/scheduled/views`               |
| 38  |           | Search               | Alerts                               | All alerts and configurations                       | `\| rest splunk_server=local /servicesNS/-/-/alerts`                        |
| 39  |           | System               | Firewall Traffic                     | Retrieves information about firewall traffic        | `\| rest splunk_server=local /services/firewall/traffic`                    |
| 40  | X         | User Interface       | Dashboards                           | All dashboards and XML configurations               | `\| rest splunk_server=local /servicesNS/-/-/data/ui/views`                 |
| 41  |           | User Interface       | Data Models                          | List of data models                                 | `\| rest splunk_server=local /servicesNS/-/-/datamodel/model`               |
| 42  | X         | User Interface       | Navigation Menus                     | Configuration of navigation menus                   | `\| rest splunk_server=local /servicesNS/-/-/data/ui/nav`                   |
| 43  |           | User Preferences     | User Preferences                     | User-specific preferences and settings              | `\| rest splunk_server=local /servicesNS/-/-/admin/user-prefs`              |
| 44  |           | Workload Management  | Search Head Clusters                 | Information about search head clusters              | `\| rest splunk_server=local /services/shcluster/captain/members`           |

* Splunk REST API Endpoints reference list: [https://docs.splunk.com/Documentation/Splunk/9.1.2/RESTREF/RESTlist](https://docs.splunk.com/Documentation/Splunk/9.1.2/RESTREF/RESTlist)

