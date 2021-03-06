---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 0
info:
  title: Google Compute Engine API Create Instance Group Manager
  description: Creates a managed instance group using the information that you specify
    in the request. After the group is created, it schedules an action to create instances
    in the group using the specified instance template. This operation is marked as
    DONE when the group is created even if the instances in the group have not yet
    been created. You must separately verify the status of the individual instances
    with the listmanagedinstances method.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/aggregated/instanceGroupManagers:
    get:
      summary: Get Instance Group Managers
      description: Retrieves the list of managed instance groups and groups them by
        zone.
      operationId: compute.instanceGroupManagers.aggregatedList
      x-api-path-slug: projectaggregatedinstancegroupmanagers-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Instance Group
  /{project}/aggregated/instanceGroups:
    get:
      summary: Get Instance Groups
      description: Retrieves the list of instance groups and sorts them by zone.
      operationId: compute.instanceGroups.aggregatedList
      x-api-path-slug: projectaggregatedinstancegroups-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Instance Group
      - Aggregation
  /{project}/regions/{region}/instanceGroupManagers:
    get:
      summary: Get Instance Group Managers
      description: Retrieves the list of managed instance groups that are contained
        within the specified region.
      operationId: compute.regionInstanceGroupManagers.list
      x-api-path-slug: projectregionsregioninstancegroupmanagers-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region scoping this request
      responses:
        200:
          description: OK
      tags:
      - Instance Group
    post:
      summary: Create Instance Group Manager
      description: Creates a managed instance group using the information that you
        specify in the request. After the group is created, it schedules an action
        to create instances in the group using the specified instance template. This
        operation is marked as DONE when the group is created even if the instances
        in the group have not yet been created. You must separately verify the status
        of the individual instances with the listmanagedinstances method.
      operationId: compute.regionInstanceGroupManagers.insert
      x-api-path-slug: projectregionsregioninstancegroupmanagers-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region scoping this request
      responses:
        200:
          description: OK
      tags:
      - Instance Group
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---