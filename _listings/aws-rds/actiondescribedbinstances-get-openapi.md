---
swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 0
info:
  title: Amazon RDS API Describe D B Instances
  version: 1.0.0
  description: Returns information about provisioned RDS instances.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeDBClusterParameterGroups:
    get:
      summary: Describe D B Cluster Parameter Groups
      description: Returns a list of DBClusterParameterGroup descriptions.
      operationId: describedbclusterparametergroups
      x-api-path-slug: actiondescribedbclusterparametergroups-get
      parameters:
      - in: query
        name: DBClusterParameterGroupName
        description: The name of a specific DB cluster parameter group to return details
          for
        type: string
      - in: query
        name: Filters.Filter.N
        description: This parameter is not currently supported
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous        DescribeDBClusterParameterGroups
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cluster Parameter Groups
  /?Action=DescribeDBClusterParameters:
    get:
      summary: Describe D B Cluster Parameters
      description: Returns the detailed parameter list for a particular DB cluster
        parameter group.
      operationId: describedbclusterparameters
      x-api-path-slug: actiondescribedbclusterparameters-get
      parameters:
      - in: query
        name: DBClusterParameterGroupName
        description: The name of a specific DB cluster parameter group to return parameter
          details for
        type: string
      - in: query
        name: Filters.Filter.N
        description: This parameter is not currently supported
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous      DescribeDBClusterParameters
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      - in: query
        name: Source
        description: A value that indicates to return only parameters for a specific
          source
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cluster Parameters
  /?Action=DescribeDBClusters:
    get:
      summary: Describe D B Clusters
      description: Returns information about provisioned Aurora DB clusters.
      operationId: describedbclusters
      x-api-path-slug: actiondescribedbclusters-get
      parameters:
      - in: query
        name: DBClusterIdentifier
        description: The user-supplied DB cluster identifier
        type: string
      - in: query
        name: Filters.Filter.N
        description: A filter that specifies one or more DB clusters to describe
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous            DescribeDBClusters
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Clusters
  /?Action=DescribeDBClusterSnapshotAttributes:
    get:
      summary: Describe D B Cluster Snapshot Attributes
      description: Returns a list of DB cluster snapshot attribute names and values
        for a manual DB cluster snapshot.
      operationId: describedbclustersnapshotattributes
      x-api-path-slug: actiondescribedbclustersnapshotattributes-get
      parameters:
      - in: query
        name: DBClusterSnapshotIdentifier
        description: The identifier for the DB cluster snapshot to describe the attributes
          for
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cluster Snapshots
  /?Action=DescribeDBClusterSnapshots:
    get:
      summary: Describe D B Cluster Snapshots
      description: Returns information about DB cluster snapshots.
      operationId: describedbclustersnapshots
      x-api-path-slug: actiondescribedbclustersnapshots-get
      parameters:
      - in: query
        name: DBClusterIdentifier
        description: The ID of the DB cluster to retrieve the list of DB cluster snapshots
          for
        type: string
      - in: query
        name: DBClusterSnapshotIdentifier
        description: A specific DB cluster snapshot identifier to describe
        type: string
      - in: query
        name: Filters.Filter.N
        description: This parameter is not currently supported
        type: string
      - in: query
        name: IncludePublic
        description: Set this value to true to include manual DB cluster snapshots
          that are public and can be copied             or restored by any AWS account,
          otherwise set this value to false
        type: string
      - in: query
        name: IncludeShared
        description: Set this value to true to include shared manual DB cluster snapshots             from
          other AWS accounts that this AWS account has been given             permission
          to copy or restore, otherwise set this value to false
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous            DescribeDBClusterSnapshots
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      - in: query
        name: SnapshotType
        description: The type of DB cluster snapshots to be returned
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cluster Snapshots
  /?Action=DescribeDBEngineVersions:
    get:
      summary: Describe D B Engine Versions
      description: Returns a list of the available DB engines.
      operationId: describedbengineversions
      x-api-path-slug: actiondescribedbengineversions-get
      parameters:
      - in: query
        name: DBParameterGroupFamily
        description: The name of a specific DB parameter group family to return details
          for
        type: string
      - in: query
        name: DefaultOnly
        description: Indicates that only the default version of the specified engine
          or engine and major version combination is returned
        type: string
      - in: query
        name: Engine
        description: The database engine to return
        type: string
      - in: query
        name: EngineVersion
        description: The database engine version to return
        type: string
      - in: query
        name: Filters.Filter.N
        description: Not currently supported
        type: string
      - in: query
        name: ListSupportedCharacterSets
        description: If this parameter is specified           and the requested engine
          supports the CharacterSetName parameter for CreateDBInstance,           the
          response includes a list of supported character sets for each engine version
        type: string
      - in: query
        name: ListSupportedTimezones
        description: If this parameter is specified             and the requested
          engine supports the TimeZone parameter for CreateDBInstance,             the
          response includes a list of supported time zones for each engine version
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Engines
  /?Action=DescribeDBInstances:
    get:
      summary: Describe D B Instances
      description: Returns information about provisioned RDS instances.
      operationId: describedbinstances
      x-api-path-slug: actiondescribedbinstances-get
      parameters:
      - in: query
        name: DBInstanceIdentifier
        description: The user-supplied instance identifier
        type: string
      - in: query
        name: Filters.Filter.N
        description: A filter that specifies one or more DB instances to describe
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous        DescribeDBInstances
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Instances
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