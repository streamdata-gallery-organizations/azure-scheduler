---
swagger: "2.0"
x-collection-name: Azure Scheduler
x-complete: 1
info:
  title: SchedulerManagementClient
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.Scheduler/jobCollections:
    get:
      summary: Job Collections List By Subscription
      description: Gets all job collections under specified subscription.
      operationId: JobCollections_ListBySubscription
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoftschedulerjobcollections-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Job Collections Subscription
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections:
    get:
      summary: Job Collections List By Resource Group
      description: Gets all job collections under specified resource group.
      operationId: JobCollections_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollections-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections Resource Group
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}
  : get:
      summary: Job Collections Get
      description: Gets a job collection.
      operationId: JobCollections_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionname-get
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections
    put:
      summary: Job Collections Create Or Update
      description: Provisions a new job collection or updates an existing job collection.
      operationId: JobCollections_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionname-put
      parameters:
      - in: body
        name: jobCollection
        description: The job collection definition
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections
    patch:
      summary: Job Collections Patch
      description: Patches an existing job collection.
      operationId: JobCollections_Patch
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionname-patch
      parameters:
      - in: body
        name: jobCollection
        description: The job collection definition
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections
    delete:
      summary: Job Collections Delete
      description: Deletes a job collection.
      operationId: JobCollections_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionname-delete
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}/enable
  : post:
      summary: Job Collections Enable
      description: Enables all of the jobs in the job collection.
      operationId: JobCollections_Enable
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnameenable-post
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}/disable
  : post:
      summary: Job Collections Disable
      description: Disables all of the jobs in the job collection.
      operationId: JobCollections_Disable
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamedisable-post
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Job Collections
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}/jobs/{jobName}
  : get:
      summary: Jobs Get
      description: Gets a job.
      operationId: Jobs_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobsjobname-get
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: path
        name: jobName
        description: The job name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
    put:
      summary: Jobs Create Or Update
      description: Provisions a new job or updates an existing job.
      operationId: Jobs_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobsjobname-put
      parameters:
      - in: body
        name: job
        description: The job definition
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: path
        name: jobName
        description: The job name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
    patch:
      summary: Jobs Patch
      description: Patches an existing job.
      operationId: Jobs_Patch
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobsjobname-patch
      parameters:
      - in: body
        name: job
        description: The job definition
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: path
        name: jobName
        description: The job name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
    delete:
      summary: Jobs Delete
      description: Deletes a job.
      operationId: Jobs_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobsjobname-delete
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: path
        name: jobName
        description: The job name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}/jobs/{jobName}/run
  : post:
      summary: Jobs Run
      description: Runs a job.
      operationId: Jobs_Run
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobsjobnamerun-post
      parameters:
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: path
        name: jobName
        description: The job name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}/jobs
  : get:
      summary: Jobs List
      description: Lists all jobs under the specified job collection.
      operationId: Jobs_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobs-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the job state
      - in: query
        name: $skip
        description: The (0-based) index of the job history list from which to begin
          requesting entries
      - in: query
        name: $top
        description: The number of jobs to request, in the of range of [1
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Scheduler/jobCollections/{jobCollectionName}/jobs/{jobName}/history
  : get:
      summary: Jobs List Job History
      description: Lists job history.
      operationId: Jobs_ListJobHistory
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftschedulerjobcollectionsjobcollectionnamejobsjobnamehistory-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the job state
      - in: query
        name: $skip
        description: The (0-based) index of the job history list from which to begin
          requesting entries
      - in: query
        name: $top
        description: the number of job history to request, in the of range of [1
      - in: path
        name: jobCollectionName
        description: The job collection name
      - in: path
        name: jobName
        description: The job name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Jobs
---