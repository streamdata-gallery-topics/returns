---
swagger: "2.0"
x-collection-name: AWS ElastiCache
x-complete: 0
info:
  title: Amazon ElastiCache API Describe Engine Default Parameters
  version: 1.0.0
  description: |-
    Returns the default engine and
                system parameter information for the specified cache engine.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeCacheClusters:
    get:
      summary: Describe Cache Clusters
      description: |-
        Returns information about all provisioned
                    cache clusters if no cache cluster identifier is specified, or about a specific cache
                    cluster if a cache cluster identifier is supplied.
      operationId: describeCacheClusters
      x-api-path-slug: actiondescribecacheclusters-get
      parameters:
      - in: query
        name: CacheClusterId
        description: The user-supplied cluster identifier
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      - in: query
        name: ShowCacheNodeInfo
        description: An optional flag that can be included in the DescribeCacheCluster
          request             to retrieve information about the individual cache nodes
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Clusters
  /?Action=DescribeCacheEngineVersions:
    get:
      summary: Describe Cache Engine Versions
      description: |-
        Returns a list of the available cache
                    engines and their versions.
      operationId: describeCacheEngineVersions
      x-api-path-slug: actiondescribecacheengineversions-get
      parameters:
      - in: query
        name: CacheParameterGroupFamily
        description: The name of a specific cache parameter group family to return
          details for
        type: string
      - in: query
        name: DefaultOnly
        description: If true, specifies that only the default version of the specified
          engine or engine            and major version combination is to be returned
        type: string
      - in: query
        name: Engine
        description: The cache engine to return
        type: string
      - in: query
        name: EngineVersion
        description: The cache engine version to return
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Engine Versions
  /?Action=DescribeCacheParameterGroups:
    get:
      summary: Describe Cache Parameter Groups
      description: |-
        Returns a list of cache parameter group
                    descriptions.
      operationId: describeCacheParameterGroups
      x-api-path-slug: actiondescribecacheparametergroups-get
      parameters:
      - in: query
        name: CacheParameterGroupName
        description: The name of a specific cache parameter group to return details
          for
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Parameter Groups
  /?Action=DescribeCacheParameters:
    get:
      summary: Describe Cache Parameters
      description: |-
        Returns the detailed parameter list for a
                    particular cache parameter group.
      operationId: describeCacheParameters
      x-api-path-slug: actiondescribecacheparameters-get
      parameters:
      - in: query
        name: CacheParameterGroupName
        description: The name of a specific cache parameter group to return details
          for
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      - in: query
        name: Source
        description: The parameter types to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Parameters
  /?Action=DescribeCacheSecurityGroups:
    get:
      summary: Describe Cache Security Groups
      description: |-
        Returns a list of cache security group
                    descriptions.
      operationId: describeCacheSecurityGroups
      x-api-path-slug: actiondescribecachesecuritygroups-get
      parameters:
      - in: query
        name: CacheSecurityGroupName
        description: The name of the cache security group to return details for
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Security Groups
  /?Action=DescribeCacheSubnetGroups:
    get:
      summary: Describe Cache Subnet Groups
      description: |-
        Returns a list of cache subnet group
                    descriptions.
      operationId: describeCacheSubnetGroups
      x-api-path-slug: actiondescribecachesubnetgroups-get
      parameters:
      - in: query
        name: CacheSubnetGroupName
        description: The name of the cache subnet group to return details for
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Subnet Groups
  /?Action=DescribeEngineDefaultParameters:
    get:
      summary: Describe Engine Default Parameters
      description: |-
        Returns the default engine and
                    system parameter information for the specified cache engine.
      operationId: describeEngineDefaultParameters
      x-api-path-slug: actiondescribeenginedefaultparameters-get
      parameters:
      - in: query
        name: CacheParameterGroupFamily
        description: The name of the cache parameter group family
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Engine Default Parameters
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