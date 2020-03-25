# ADF.procfwk

![alt text](https://mrpaulandrew.files.wordpress.com/2020/03/adfprocfwk-icon.png "ADF.procfwk Icon")

## Code Project Overview

This open source code project delivers a simple metadata driven processing framework for Azure Data Factory (ADF). The framework is delivered by coupling ADF with an Azure SQL Database that houses execution stage and pipeline information that is later called using an Azure Functions App. The parent/child metadata structure firstly allows stages of dependencies to be executed in sequence. Then secondly, all pipelines within a stage to be executed in parallel offering scaled out control flows where no inter-dependencies exist for a given stage.

The framework is designed to integrate with any existing Data Factory solution by making the lowest level executor a stand alone processing pipeline that is wrapped in a higher level of controlled (sequential) dependencies. This level of abstraction means operationally nothing about the monitoring of orchestration processes is hidden in multiple levels of dynamic activity calls. Instead, everything from the processing pipeline doing the work can be inspected using out-of-the-box ADF features.

This framework can also be used in any Azure Tenant and allow the creation of complex control flows across multiple Data Factory resources by connecting Service Principal details to targeted Subscriptions > Resource Groups > Data Factory's and Pipelines, this offers very granular administration over data processing components in a given environment.

 ## Authors

 | Who | Details |
|------------|-------------|
|Paul Andrew |[@mrpaulandrew](https://twitter.com/mrpaulandrew)<br/>[paul@mrpaulandrew.com](mailto:paul@mrpaulandrew.com)<br/>[https://mrpaulandrew.tech](https://mrpaulandrew.tech)|
| | |

## Development Backlog
[Go to GitHub Kanban board...](https://github.com/mrpaulandrew/ADF.procfwk/projects/1)

## Resources and Content

<table>
<tbody>
<tr>
<td><img class="aligncenter wp-image-1972" src="https://mrpaulandrew.files.wordpress.com/2020/03/azure-square-logo.png?w=150" alt="" width="61" height="61" /></td>
<td><strong>Blogs</strong></td>
<td><a href="https://mrpaulandrew.com/category/azure/data-factory/adf-procfwk/" target="_blank" rel="noopener">mrpaulandrew.com/ADF.procfwk</a></td>
</tr>
<tr>
<td><img class="aligncenter wp-image-819" src="https://mrpaulandrew.files.wordpress.com/2018/11/github-icon.png?w=150" alt="" width="61" height="61" /></td>
<td><strong>GitHub</strong></td>
<td><a href="https://github.com/mrpaulandrew/ADF.procfwk" target="_blank" rel="noopener">github.com/mrpaulandrew/ADF.procfwk</a></td>
</tr>
<tr>
<td><img class="aligncenter wp-image-1971" src="https://mrpaulandrew.files.wordpress.com/2020/03/twitterlogo.png?w=150" alt="" width="61" height="61" /></td>
<td><strong>Twitter</strong></td>
<td><a href="https://twitter.com/search?q=%23ADFprocfwk&amp;src=hashtag_click" target="_blank" rel="noopener">#ADFprocfwk</a></td>
</tr>
</tbody>
</table>

## Release Details

| Version | Overview | Related Blog(s) |
|:----:|--------------|--------|
| 1.2 |<u>Execution Restartability</u>, plus: <ul><li>Data Factory annotations and descriptions.</li><li>Database covering indexes.</li><li>Pipeline log status changed from 'Started' to 'Preparing'.</li><li>Pipeline log start date/time now set in child pipeline.</li></ul> |[ADF.procfwk v1.2 - Execution Restartability](https://mrpaulandrew.com/2020/03/24/adf-procfwk-v1-2-execution-restartability/)  |
| 1.1 |<u>Service Principal Handling</u> via Metadata, plus: <ul><li>Data Factory table.</li><li>Properties table and view.</li><li>Function body bug fix.</li><li>New sample data.</li></ul> |[ADF.procfwk v1.1 - Service Principal Handling via Metadata](https://mrpaulandrew.com/2020/03/17/adf-procfwk-v1-1-service-principal-handling-via-metadata/) |
| 1.0 |Simple <u>framework designed and base compontents built</u>.<br/><br/><ul><li>Part 1 - Design, concepts, service coupling, caveats, problems.</li><li>Part 2 - Database build and metadata.</li><li>Part 3 - Data Factory build.</li><li>Part 4 - Execution, conclusions, enhancements.</li></ul>|[Creating a Simple Staged Metadata Driven Processing Framework for Azure Data Factory Pipelines](https://mrpaulandrew.com/2020/02/25/creating-a-simple-staged-metadata-driven-processing-framework-for-azure-data-factory-pipelines-part-1-of-4/) |