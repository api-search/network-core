---
name: Compute
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/compute.png
url: https://example.com/apis/compute.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Compute
apis:
  - name: batch
    description: >-
      <fullname>Batch</fullname> <p>Using Batch, you can run batch computing
      workloads on the Amazon Web Services Cloud. Batch computing is a common
      means for developers, scientists, and engineers to access large amounts of
      compute resources. Batch uses the advantages of the batch computing to
      remove the undifferentiated heavy lifting of configuring and managing
      required infrastructure. At the same time, it also adopts a familiar batch
      computing software approach. You can use Batch to efficiently provision
      resources d, and work toward eliminating capacity constraints, reducing
      your overall compute costs, and delivering results more quickly.</p> <p>As
      a fully managed service, Batch can run batch computing workloads of any
      scale. Batch automatically provisions compute resources and optimizes
      workload distribution based on the quantity and scale of your specific
      workloads. With Batch, there's no need to install or manage batch
      computing software. This means that you can focus on analyzing results and
      solving your specific problems instead.</p>
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: batch
          paths:
            /v1/canceljob:
              POST:
                summary: CancelJob
                description: >-
                  <p>Cancels a job in an Batch job queue. Jobs that are in the
                  <code>SUBMITTED</code> or <code>PENDING</code> are canceled. A
                  job in<code>RUNNABLE</code> remains in <code>RUNNABLE</code>
                  until it reaches the head of the job queue. Then the job
                  status is updated to <code>FAILED</code>.</p> <note> <p>A
                  <code>PENDING</code> job is canceled after all dependency jobs
                  are completed. Therefore, it may take longer than expected to
                  cancel a job in <code>PENDING</code> status.</p> <p>When you
                  try to cancel an array parent job in <code>PENDING</code>,
                  Batch attempts to cancel all child jobs. The array parent job
                  is canceled when all child jobs are completed.</p> </note>
                  <p>Jobs that progressed to the <code>STARTING</code> or
                  <code>RUNNING</code> state aren't canceled. However, the API
                  operation still succeeds, even if no job is canceled. These
                  jobs must be terminated with the <a>TerminateJob</a>
                  operation.</p>
                tags:
                  - Cancel
                  - Jobs
                  - null
                  - Cancel Jobs
            /v1/createcomputeenvironment:
              POST:
                summary: CreateComputeEnvironment
                description: >-
                  <p>Creates an Batch compute environment. You can create
                  <code>MANAGED</code> or <code>UNMANAGED</code> compute
                  environments. <code>MANAGED</code> compute environments can
                  use Amazon EC2 or Fargate resources. <code>UNMANAGED</code>
                  compute environments can only use EC2 resources.</p> <p>In a
                  managed compute environment, Batch manages the capacity and
                  instance types of the compute resources within the
                  environment. This is based on the compute resource
                  specification that you define or the <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html">launch
                  template</a> that you specify when you create the compute
                  environment. Either, you can choose to use EC2 On-Demand
                  Instances and EC2 Spot Instances. Or, you can use Fargate and
                  Fargate Spot capacity in your managed compute environment. You
                  can optionally set a maximum price so that Spot Instances only
                  launch when the Spot Instance price is less than a specified
                  percentage of the On-Demand price.</p> <note> <p>Multi-node
                  parallel jobs aren't supported on Spot Instances.</p> </note>
                  <p>In an unmanaged compute environment, you can manage your
                  own EC2 compute resources and have flexibility with how you
                  configure your compute resources. For example, you can use
                  custom AMIs. However, you must verify that each of your AMIs
                  meet the Amazon ECS container instance AMI specification. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonECS/latest/developerguide/container_instance_AMIs.html">container
                  instance AMIs</a> in the <i>Amazon Elastic Container Service
                  Developer Guide</i>. After you created your unmanaged compute
                  environment, you can use the
                  <a>DescribeComputeEnvironments</a> operation to find the
                  Amazon ECS cluster that's associated with it. Then, launch
                  your container instances into that Amazon ECS cluster. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonECS/latest/developerguide/launch_container_instance.html">Launching
                  an Amazon ECS container instance</a> in the <i>Amazon Elastic
                  Container Service Developer Guide</i>.</p> <note> <p>To create
                  a compute environment that uses EKS resources, the caller must
                  have permissions to call <code>eks:DescribeCluster</code>.</p>
                  </note> <note> <p>Batch doesn't automatically upgrade the AMIs
                  in a compute environment after it's created. For example, it
                  also doesn't update the AMIs in your compute environment when
                  a newer version of the Amazon ECS optimized AMI is available.
                  You're responsible for the management of the guest operating
                  system. This includes any updates and security patches. You're
                  also responsible for any additional application software or
                  utilities that you install on the compute resources. There are
                  two ways to use a new AMI for your Batch jobs. The original
                  method is to complete these steps:</p> <ol> <li> <p>Create a
                  new compute environment with the new AMI.</p> </li> <li>
                  <p>Add the compute environment to an existing job queue.</p>
                  </li> <li> <p>Remove the earlier compute environment from your
                  job queue.</p> </li> <li> <p>Delete the earlier compute
                  environment.</p> </li> </ol> <p>In April 2022, Batch added
                  enhanced support for updating compute environments. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/batch/latest/userguide/updating-compute-environments.html">Updating
                  compute environments</a>. To use the enhanced updating of
                  compute environments to update AMIs, follow these rules:</p>
                  <ul> <li> <p>Either don't set the service role
                  (<code>serviceRole</code>) parameter or set it to the
                  <b>AWSBatchServiceRole</b> service-linked role.</p> </li> <li>
                  <p>Set the allocation strategy
                  (<code>allocationStrategy</code>) parameter to
                  <code>BEST_FIT_PROGRESSIVE</code>,
                  <code>SPOT_CAPACITY_OPTIMIZED</code>, or
                  <code>SPOT_PRICE_CAPACITY_OPTIMIZED</code>.</p> </li> <li>
                  <p>Set the update to latest image version
                  (<code>updateToLatestImageVersion</code>) parameter to
                  <code>true</code>. The <code>updateToLatestImageVersion</code>
                  parameter is used when you update a compute environment. This
                  parameter is ignored when you create a compute
                  environment.</p> </li> <li> <p>Don't specify an AMI ID in
                  <code>imageId</code>, <code>imageIdOverride</code> (in <a
                  href="https://docs.aws.amazon.com/batch/latest/APIReference/API_Ec2Configuration.html">
                  <code>ec2Configuration</code> </a>), or in the launch template
                  (<code>launchTemplate</code>). In that case, Batch selects the
                  latest Amazon ECS optimized AMI that's supported by Batch at
                  the time the infrastructure update is initiated.
                  Alternatively, you can specify the AMI ID in the
                  <code>imageId</code> or <code>imageIdOverride</code>
                  parameters, or the launch template identified by the
                  <code>LaunchTemplate</code> properties. Changing any of these
                  properties starts an infrastructure update. If the AMI ID is
                  specified in the launch template, it can't be replaced by
                  specifying an AMI ID in either the <code>imageId</code> or
                  <code>imageIdOverride</code> parameters. It can only be
                  replaced by specifying a different launch template, or if the
                  launch template version is set to <code>$Default</code> or
                  <code>$Latest</code>, by setting either a new default version
                  for the launch template (if <code>$Default</code>) or by
                  adding a new version to the launch template (if
                  <code>$Latest</code>).</p> </li> </ul> <p>If these rules are
                  followed, any update that starts an infrastructure update
                  causes the AMI ID to be re-selected. If the
                  <code>version</code> setting in the launch template
                  (<code>launchTemplate</code>) is set to <code>$Latest</code>
                  or <code>$Default</code>, the latest or default version of the
                  launch template is evaluated up at the time of the
                  infrastructure update, even if the <code>launchTemplate</code>
                  wasn't updated.</p> </note>
                tags:
                  - Create
                  - Compute
                  - Environments
                  - null
                  - Cancel Jobs
                  - Computer Environments
            /v1/createjobqueue:
              POST:
                summary: CreateJobQueue
                description: >-
                  <p>Creates an Batch job queue. When you create a job queue,
                  you associate one or more compute environments to the queue
                  and assign an order of preference for the compute
                  environments.</p> <p>You also set a priority to the job queue
                  that determines the order that the Batch scheduler places jobs
                  onto its associated compute environments. For example, if a
                  compute environment is associated with more than one job
                  queue, the job queue with a higher priority is given
                  preference for scheduling jobs to that compute
                  environment.</p>
                tags:
                  - Create
                  - Jobs
                  - Queues
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
            /v1/createschedulingpolicy:
              POST:
                summary: CreateSchedulingPolicy
                description: <p>Creates an Batch scheduling policy.</p>
                tags:
                  - Create
                  - Scheduling
                  - Policies
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
            /v1/deletecomputeenvironment:
              POST:
                summary: DeleteComputeEnvironment
                description: >-
                  <p>Deletes an Batch compute environment.</p> <p>Before you can
                  delete a compute environment, you must set its state to
                  <code>DISABLED</code> with the <a>UpdateComputeEnvironment</a>
                  API operation and disassociate it from any job queues with the
                  <a>UpdateJobQueue</a> API operation. Compute environments that
                  use Fargate resources must terminate all active jobs on that
                  compute environment before deleting the compute environment.
                  If this isn't done, the compute environment enters an invalid
                  state.</p>
                tags:
                  - Delete
                  - Compute
                  - Environments
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
            /v1/deletejobqueue:
              POST:
                summary: DeleteJobQueue
                description: >-
                  <p>Deletes the specified job queue. You must first disable
                  submissions for a queue with the <a>UpdateJobQueue</a>
                  operation. All jobs in the queue are eventually terminated
                  when you delete a job queue. The jobs are terminated at a rate
                  of about 16 jobs each second.</p> <p>It's not necessary to
                  disassociate compute environments from a queue before
                  submitting a <code>DeleteJobQueue</code> request.</p>
                tags:
                  - Delete
                  - Jobs
                  - Queues
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
            /v1/deleteschedulingpolicy:
              POST:
                summary: DeleteSchedulingPolicy
                description: >-
                  <p>Deletes the specified scheduling policy.</p> <p>You can't
                  delete a scheduling policy that's used in any job queues.</p>
                tags:
                  - Delete
                  - Scheduling
                  - Policies
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
            /v1/deregisterjobdefinition:
              POST:
                summary: DeregisterJobDefinition
                description: >-
                  <p>Deregisters an Batch job definition. Job definitions are
                  permanently deleted after 180 days.</p>
                tags:
                  - Deregister
                  - Jobs
                  - Definitions
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
            /v1/describecomputeenvironments:
              POST:
                summary: DescribeComputeEnvironments
                description: >-
                  <p>Describes one or more of your compute environments.</p>
                  <p>If you're using an unmanaged compute environment, you can
                  use the <code>DescribeComputeEnvironment</code> operation to
                  determine the <code>ecsClusterArn</code> that you launch your
                  Amazon ECS container instances into.</p>
                tags:
                  - Describe
                  - Compute
                  - Environments
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
            /v1/describejobdefinitions:
              POST:
                summary: DescribeJobDefinitions
                description: >-
                  <p>Describes a list of job definitions. You can specify a
                  <code>status</code> (such as <code>ACTIVE</code>) to only
                  return job definitions that match that status.</p>
                tags:
                  - Describe
                  - Jobs
                  - Definitions
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
            /v1/describejobqueues:
              POST:
                summary: DescribeJobQueues
                description: <p>Describes one or more of your job queues.</p>
                tags:
                  - Describe
                  - Jobs
                  - Queues
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
            /v1/describejobs:
              POST:
                summary: DescribeJobs
                description: <p>Describes a list of Batch jobs.</p>
                tags:
                  - Describe
                  - Jobs
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
            /v1/describeschedulingpolicies:
              POST:
                summary: DescribeSchedulingPolicies
                description: <p>Describes one or more of your scheduling policies.</p>
                tags:
                  - Describe
                  - Scheduling
                  - Policies
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
            /v1/listjobs:
              POST:
                summary: ListJobs
                description: >-
                  <p>Returns a list of Batch jobs.</p> <p>You must specify only
                  one of the following items:</p> <ul> <li> <p>A job queue ID to
                  return a list of jobs in that job queue</p> </li> <li> <p>A
                  multi-node parallel job ID to return a list of nodes for that
                  job</p> </li> <li> <p>An array job ID to return a list of the
                  children for that job</p> </li> </ul> <p>You can filter the
                  results by job status with the <code>jobStatus</code>
                  parameter. If you don't specify a status, only
                  <code>RUNNING</code> jobs are returned.</p>
                tags:
                  - Lists
                  - Jobs
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
            /v1/listschedulingpolicies:
              POST:
                summary: ListSchedulingPolicies
                description: <p>Returns a list of Batch scheduling policies.</p>
                tags:
                  - Lists
                  - Scheduling
                  - Policies
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
            /v1/tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deletes specified tags from an Batch resource.</p>
                tags:
                  - Untag
                  - Resources
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
            /v1/registerjobdefinition:
              POST:
                summary: RegisterJobDefinition
                description: <p>Registers an Batch job definition.</p>
                tags:
                  - Register
                  - Jobs
                  - Definitions
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
                  - Register Job Definitions
            /v1/submitjob:
              POST:
                summary: SubmitJob
                description: >-
                  <p>Submits an Batch job from a job definition. Parameters that
                  are specified during <a>SubmitJob</a> override parameters
                  defined in the job definition. vCPU and memory requirements
                  that are specified in the <code>resourceRequirements</code>
                  objects in the job definition are the exception. They can't be
                  overridden this way using the <code>memory</code> and
                  <code>vcpus</code> parameters. Rather, you must specify
                  updates to job definition parameters in a
                  <code>resourceRequirements</code> object that's included in
                  the <code>containerOverrides</code> parameter.</p> <note>
                  <p>Job queues with a scheduling policy are limited to 500
                  active fair share identifiers at a time. </p> </note>
                  <important> <p>Jobs that run on Fargate resources can't be
                  guaranteed to run for more than 14 days. This is because,
                  after 14 days, Fargate resources might become unavailable and
                  job might be terminated.</p> </important>
                tags:
                  - Submit
                  - Jobs
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
                  - Register Job Definitions
                  - Submit Jobs
            /v1/terminatejob:
              POST:
                summary: TerminateJob
                description: >-
                  <p>Terminates a job in a job queue. Jobs that are in the
                  <code>STARTING</code> or <code>RUNNING</code> state are
                  terminated, which causes them to transition to
                  <code>FAILED</code>. Jobs that have not progressed to the
                  <code>STARTING</code> state are cancelled.</p>
                tags:
                  - Terminate
                  - Jobs
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
                  - Register Job Definitions
                  - Submit Jobs
                  - Terminate Jobs
            /v1/updatecomputeenvironment:
              POST:
                summary: UpdateComputeEnvironment
                description: <p>Updates an Batch compute environment.</p>
                tags:
                  - Update
                  - Compute
                  - Environments
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
                  - Register Job Definitions
                  - Submit Jobs
                  - Terminate Jobs
                  - Computer Environments
            /v1/updatejobqueue:
              POST:
                summary: UpdateJobQueue
                description: <p>Updates a job queue.</p>
                tags:
                  - Update
                  - Jobs
                  - Queues
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
                  - Register Job Definitions
                  - Submit Jobs
                  - Terminate Jobs
                  - Computer Environments
                  - Job Queues
            /v1/updateschedulingpolicy:
              POST:
                summary: UpdateSchedulingPolicy
                description: <p>Updates a scheduling p
                tags:
                  - Update
                  - Scheduling
                  - Policies
                  - null
                  - Cancel Jobs
                  - Computer Environments
                  - Job Queues
                  - Scheduling Policy
                  - null
                  - Job Queues
                  - Scheduling Policies
                  - Deregister Job Definitions
                  - Computer Environments
                  - Job Definitions
                  - Job Queues
                  - Jobs
                  - Scheduling Policies
                  - Jobs
                  - Scheduling Policies
                  - ARN
                  - Register Job Definitions
                  - Submit Jobs
                  - Terminate Jobs
                  - Computer Environments
                  - Job Queues
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/batch-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/batch-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:batch
  - name: Digital Ocean API
    description: >
      The DigitalOcean API lets you programmatically manage your Droplets and
      other resources using conventional HTTP requests. Any action that you can
      perform through the DigitalOcean Control Panel (except for creating
      personal access tokens) can also be performed with the API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.digitalocean.com/
    baseURL: https://api.example.com
    tags:
      - Servers
      - Cloud
      - Compute
    properties:
      - type: Documentation
        url: https://docs.digitalocean.com/
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: DigitalOcean API
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          tags:
            - name: 1-Click Applications
              description: >-
                1-Click applications are pre-built Droplet images or Kubernetes
                apps with software,

                features, and configuration details already set up for you. They
                can be found in the

                [DigitalOcean
                Marketplace](https://www.digitalocean.com/docs/marketplace).
            - name: Account
              description: Provides information about your current account.
            - name: Actions
              description: >-
                Actions are records of events that have occurred on the
                resources in your account.

                These can be things like rebooting a Droplet, or transferring an
                image to a new region.


                An action object is created every time one of these actions is
                initiated. The action

                object contains information about the current status of the
                action, start and complete

                timestamps, and the associated resource type and ID.


                Every action that creates an action object is available through
                this endpoint. Completed

                actions are not removed from this list and are always available
                for querying.


                **Note:** You can pass the following HTTP header with the
                request to have the API return

                the `reserved_ips` stanza instead of the `floating_ips` stanza:


                - `Accept: application/vnd.digitalocean.reserveip+json`
            - name: Apps
              description: >-
                App Platform is a Platform-as-a-Service (PaaS) offering from
                DigitalOcean that allows

                developers to publish code directly to DigitalOcean servers
                without worrying about the

                underlying infrastructure.


                Most API operations are centered around a few core object types.
                Following are the

                definitions of these types. These definitions will be omitted
                from the operation-specific

                documentation.


                For documentation on app specifications (`AppSpec` objects),
                please refer to the

                [product
                documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/)).
            - name: Billing
              description: >-
                The billing endpoints allow you to retrieve your account
                balance, invoices

                and billing history.


                **Balance:** By sending requests to the
                `/v2/customers/my/balance` endpoint, you can

                retrieve the balance information for the requested customer
                account.


                **Invoices:**
                [Invoices](https://www.digitalocean.com/docs/accounts/billing/invoices/)

                are generated on the first of each month for every DigitalOcean

                customer. An invoice preview is generated daily, which can be
                accessed

                with the `preview` keyword in place of `$INVOICE_UUID`. To
                interact with

                invoices, you will generally send requests to the invoices
                endpoint at

                `/v2/customers/my/invoices`.


                **Billing History:** Billing history is a record of billing
                events for your account.

                For example, entries may include events like payments made,
                invoices

                issued, or credits granted. To interact with invoices, you

                will generally send requests to the invoices endpoint at

                `/v2/customers/my/billing_history`.
            - name: Block Storage
              description: >-
                [DigitalOcean Block Storage
                Volumes](https://www.digitalocean.com/docs/volumes/)

                provide expanded storage capacity for your Droplets and can be
                moved

                between Droplets within a specific region.


                Volumes function as raw block devices, meaning they appear to
                the

                operating system as locally attached storage which can be
                formatted using

                any file system supported by the OS. They may be created in
                sizes from

                1GiB to 16TiB.


                By sending requests to the `/v2/volumes` endpoint, you can list,
                create, or

                delete volumes as well as attach and detach them from Droplets
            - name: Block Storage Actions
              description: >-
                Block storage actions are commands that can be given to a
                DigitalOcean

                Block Storage Volume. An example would be detaching or attaching
                a volume

                from a Droplet. These requests are made on the

                `/v2/volumes/$VOLUME_ID/actions` endpoint.


                An action object is returned. These objects hold the current
                status of the

                requested action.
            - name: CDN Endpoints
              description: >-
                Content hosted in DigitalOcean's object storage solution,

                [Spaces](https://www.digitalocean.com/docs/spaces/overview/),

                can optionally be served by our globally distributed Content
                Delivery

                Network (CDN). By sending requests to `/v2/cdn/endpoints`, you
                can list,

                create, or delete CDN Endpoints as well as purge cached content.
                To use a

                custom subdomain to access the CDN Endpoint, provide the ID of a

                DigitalOcean managed TLS certificate and the fully qualified
                domain name

                for the custom subdomain.
            - name: Certificates
              description: >-
                In order to perform SSL termination on load balancers,
                DigitalOcean offers

                two types of [SSL certificate
                management](https://www.digitalocean.com/docs/accounts/security/#certificates):


                * **Custom**: User-generated certificates may be uploaded to
                DigitalOcean

                where they will be placed in a fully encrypted and isolated
                storage system.


                * **Let's Encrypt**: Certificates may be automatically generated
                by

                DigitalOcean utilizing an integration with Let's Encrypt, the
                free and

                open certificate authority. These certificates will also be
                automatically

                renewed as required.
            - name: Container Registry
              description: >-
                DigitalOcean offers the ability for you to create a

                [private container
                registry](https://www.digitalocean.com/docs/images/container-registry/quickstart/)

                to store your Docker images for use with your Kubernetes
                clusters. This

                container registry runs inside the same datacenters as your
                cluster,

                ensuring reliable and performant rollout of image deployments.


                You can only create one registry per DigitalOcean account, but
                you can use

                that registry to create as many repositories as you wish.
            - name: Databases
              description: >-
                DigitalOcean's [managed database
                service](https://www.digitalocean.com/docs/databases)

                simplifies the creation and management of highly available
                database clusters. Currently, it

                offers support for
                [PostgreSQL](http://www.digitalocean.com/docs/databases/postgresql/),

                [Redis](https://www.digitalocean.com/docs/databases/redis/),

                [MySQL](https://www.digitalocean.com/docs/databases/mysql/), and

                [MongoDB](https://www.digitalocean.com/docs/databases/mongodb/).


                By sending requests to the `/v2/databases` endpoint, you can
                list, create, or delete

                database clusters as well as scale the size of a cluster, add or
                remove read-only replicas,

                and manage other configuration details.


                Database clusters may be deployed in a multi-node,
                high-availability configuration.

                If your machine type is above the basic nodes, your node plan is
                above the smallest option,

                or you are running MongoDB, you may additionally include up to
                two standby nodes in your cluster.


                The size of individual nodes in a database cluster is
                represented by a human-readable slug,

                which is used in some of the following requests. Each slug
                denotes the node's identifier,

                CPU count, and amount of RAM, in that order.


                For a list of currently available database slugs and options,
                use the `/v2/databases/options` endpoint or use the 

                `doctl databases options`
                [command](https://docs.digitalocean.com/reference/doctl/reference/databases/options).
            - name: Domain Records
              description: >-
                Domain record resources are used to set or retrieve information
                about the

                individual DNS records configured for a domain. This allows you
                to build

                and manage DNS zone files by adding and modifying individual
                records for a

                domain.


                The [DigitalOcean DNS management
                interface](https://www.digitalocean.com/docs/networking/dns/)

                allows you to configure the following DNS records:


                Name  |
                Description                                                                                                                                       
                |

                |-------------------------------------------------------------------------------------------------------------------------------------------------|

                A     | This record type is used to map an IPv4 address to a
                hostname.                                                                                    
                |

                AAAA  | This record type is used to map an IPv6 address to a
                hostname.                                                                                    
                |

                CAA   | As specified in RFC-6844, this record type can be used
                to restrict which certificate authorities are permitted to issue
                certificates for a domain. |

                CNAME | This record type defines an alias for your canonical
                hostname (the one defined by an A or AAAA
                record).                                            |

                MX    | This record type is used to define the mail exchanges
                used for the
                domain.                                                                        
                |

                NS    | This record type defines the name servers that are used
                for this
                zone.                                                                            
                |

                TXT   | This record type is used to associate a string of text
                with a hostname, primarily used for
                verification.                                           |

                SRV   | This record type specifies the location (hostname and
                port number) of servers for specific
                services.                                               |

                SOA   | This record type defines administrative information
                about the zone. Can only have ttl changed, cannot be
                deleted                                   |
            - name: Domains
              description: >-
                Domain resources are domain names that you have purchased from a
                domain

                name registrar that you are managing through the

                [DigitalOcean DNS
                interface](https://www.digitalocean.com/docs/networking/dns/).


                This resource establishes top-level control over each domain.
                Actions that

                affect individual domain records should be taken on the

                [Domain Records](#tag/Domain-Records) resource.
            - name: Droplet Actions
              description: >-
                Droplet actions are tasks that can be executed on a Droplet.
                These can be

                things like rebooting, resizing, snapshotting, etc.


                Droplet action requests are generally targeted at one of the
                "actions"

                endpoints for a specific Droplet. The specific actions are
                usually

                initiated by sending a POST request with the action and
                arguments as

                parameters.


                Droplet action requests create a Droplet actions object, which
                can be used

                to get information about the status of an action. Creating a
                Droplet

                action is asynchronous: the HTTP call will return the action
                object before

                the action has finished processing on the Droplet. The current
                status of

                an action can be retrieved from either the Droplet actions
                endpoint or the

                global actions endpoint. If a Droplet action is uncompleted it
                may block

                the creation of a subsequent action for that Droplet, the locked
                attribute

                of the Droplet will be true and attempts to create a Droplet
                action will

                fail with a status of 422.
            - name: Droplets
              description: >-
                A [Droplet](https://www.digitalocean.com/docs/droplets/) is a
                DigitalOcean

                virtual machine. By sending requests to the Droplet endpoint,
                you can

                list, create, or delete Droplets.


                Some of the attributes will have an object value. The `region`
                and `image`

                objects will all contain the standard attributes of their
                associated

                types. Find more information about each of these objects in
                their

                respective sections.
            - name: Firewalls
              description: >-
                [DigitalOcean Cloud
                Firewalls](https://www.digitalocean.com/docs/networking/firewalls/)

                provide the ability to restrict network access to and from a
                Droplet

                allowing you to define which ports will accept inbound or
                outbound

                connections. By sending requests to the `/v2/firewalls`
                endpoint, you can

                list, create, or delete firewalls as well as modify access
                rules.
            - name: Floating IP Actions
              description: >-
                As of 16 June 2022, we have renamed the Floating IP product to
                [Reserved
                IPs](https://docs.digitalocean.com/reference/api/api-reference/#tag/Reserved-IPs).

                The Reserved IP product's endpoints function the exact same way
                as Floating IPs.

                The only difference is the name change throughout the URLs and
                fields.

                For example, the `floating_ips` field is now the `reserved_ips`
                field.

                The Floating IP endpoints will remain active until fall 2023
                before being

                permanently deprecated.


                With the exception of the [Projects
                API](https://docs.digitalocean.com/reference/api/api-reference/#tag/Projects),

                we will reflect this change as an additional field in the
                responses across the API

                where the `floating_ip` field is used. For example, the Droplet
                metadata response

                will contain the field `reserved_ips` in addition to the
                `floating_ips` field.

                Floating IPs retrieved using the Projects API will retain the
                original name.


                Floating IP actions are commands that can be given to a
                DigitalOcean

                floating IP. These requests are made on the actions endpoint of
                a specific

                floating IP.


                An action object is returned. These objects hold the current
                status of the

                requested action.
            - name: Floating IPs
              description: >-
                As of 16 June 2022, we have renamed the Floating IP product to
                [Reserved
                IPs](https://docs.digitalocean.com/reference/api/api-reference/#tag/Reserved-IPs).

                The Reserved IP product's endpoints function the exact same way
                as Floating IPs.

                The only difference is the name change throughout the URLs and
                fields.

                For example, the `floating_ips` field is now the `reserved_ips`
                field.

                The Floating IP endpoints will remain active until fall 2023
                before being

                permanently deprecated.


                With the exception of the [Projects
                API](https://docs.digitalocean.com/reference/api/api-reference/#tag/Projects),

                we will reflect this change as an additional field in the
                responses across the API

                where the `floating_ip` field is used. For example, the Droplet
                metadata response

                will contain the field `reserved_ips` in addition to the
                `floating_ips` field.

                Floating IPs retrieved using the Projects API will retain the
                original name.


                [DigitalOcean Floating
                IPs](https://www.digitalocean.com/docs/networking/floating-ips/)

                are publicly-accessible static IP addresses that can be mapped
                to one of

                your Droplets. They can be used to create highly available
                setups or other

                configurations requiring movable addresses.


                Floating IPs are bound to a specific region.
            - name: Functions
              description: >-
                [Serverless
                functions](https://docs.digitalocean.com/products/functions) are
                blocks of code that run on demand without the need to manage any
                infrastructure.

                You can develop functions on your local machine and then deploy
                them to a namespace using `doctl`, the [official DigitalOcean
                CLI tool](https://docs.digitalocean.com/reference/doctl).


                The Serverless Functions API currently only supports creating
                and managing namespaces.
            - name: Image Actions
              description: >-
                Image actions are commands that can be given to a DigitalOcean
                image. In

                general, these requests are made on the actions endpoint of a
                specific

                image.


                An image action object is returned. These objects hold the
                current status

                of the requested action.
            - name: Images
              description: >-
                A DigitalOcean
                [image](https://www.digitalocean.com/docs/images/) can be

                used to create a Droplet and may come in a number of flavors.
                Currently,

                there are five types of images: snapshots, backups,
                applications,

                distributions, and custom images.


                *
                [Snapshots](https://www.digitalocean.com/docs/images/snapshots/)
                provide

                a full copy of an existing Droplet instance taken on demand.


                * [Backups](https://www.digitalocean.com/docs/images/backups/)
                are similar

                to snapshots but are created automatically at regular intervals
                when

                enabled for a Droplet.


                * [Custom
                images](https://www.digitalocean.com/docs/images/custom-images/)

                are Linux-based virtual machine images (raw, qcow2, vhdx, vdi,
                and vmdk

                formats are supported) that you may upload for use on
                DigitalOcean.


                * Distributions are the public Linux distributions that are
                available to

                be used as a base to create Droplets.


                * Applications, or [1-Click
                Apps](https://www.digitalocean.com/docs/one-clicks/),

                are distributions pre-configured with additional software.


                To interact with images, you will generally send requests to the
                images

                endpoint at /v2/images.
            - name: Kubernetes
              description: >-
                [DigitalOcean
                Kubernetes](https://www.digitalocean.com/docs/kubernetes/)

                allows you to quickly deploy scalable and secure Kubernetes
                clusters. By

                sending requests to the `/v2/kubernetes/clusters` endpoint, you
                can list,

                create, or delete clusters as well as scale node pools up and
                down,

                recycle individual nodes, and retrieve the kubeconfig file for
                use with

                a cluster.
            - name: Load Balancers
              description: >-
                [DigitalOcean Load
                Balancers](https://www.digitalocean.com/docs/networking/load-balancers/)

                provide a way to distribute traffic across multiple Droplets. By
                sending

                requests to the `/v2/load_balancers` endpoint, you can list,
                create, or

                delete load balancers as well as add or remove Droplets,
                forwarding rules,

                and other configuration details.
            - name: Monitoring
              description: >-
                The DigitalOcean Monitoring API makes it possible to
                programmatically retrieve metrics as well as configure alert

                policies based on these metrics. The Monitoring API can help you
                gain insight into how your apps are performing

                and consuming resources.
            - name: Project Resources
              description: >-
                Project Resources are resources that can be grouped into your
                projects.

                You can group resources (like Droplets, Spaces, load balancers,
                domains,

                and floating IPs) in ways that align with the applications you
                host on

                DigitalOcean.


                ### Supported Resource Types Examples


                Projects resources are identified by uniform resource names or
                URNs. A

                valid URN has the following format:
                `do:resource_type:resource_id`. The

                following resource types are supported:


                Resource Type      | Example URN

                -------------------|------------

                App Platform App   |
                `do:app:be5aab85-851b-4cab-b2ed-98d5a63ba4e8`

                Database           |
                `do:dbaas:83c7a55f-0d84-4760-9245-aba076ec2fb2`

                Domain             | `do:domain:example.com`

                Droplet            | `do:droplet:4126873`

                Floating IP        | `do:floatingip:192.168.99.100`

                Kubernetes Cluster |
                `do:kubernetes:bd5f5959-5e1e-4205-a714-a914373942af`

                Load Balancer      |
                `do:loadbalancer:39052d89-8dd4-4d49-8d5a-3c3b6b365b5b`

                Space              | `do:space:my-website-assets`

                Volume             |
                `do:volume:6fc4c277-ea5c-448a-93cd-dd496cfef71f`


                ### Resource Status Codes


                When assigning and retrieving resources in projects, a `status`
                attribute

                is returned that indicates if a resource was successfully
                retrieved or

                assigned. The status codes can be one of the following:


                Status Code        | Explanation

                -------------------|------------

                `ok`               | There was no problem retrieving or
                assigning a resource.

                `not_found`        | The resource was not found.

                `assigned`         | The resource was successfully assigned.

                `already_assigned` | The resource was already assigned.

                `service_down`     | There was a problem retrieving or assigning
                a resource. Please try again.
            - name: Projects
              description: >-
                Projects allow you to organize your resources into groups that
                fit the way

                you work. You can group resources (like Droplets, Spaces, load
                balancers,

                domains, and floating IPs) in ways that align with the
                applications

                you host on DigitalOcean.
            - name: Regions
              description: Provides information about DigitalOcean data center regions.
            - name: Reserved IP Actions
              description: >-
                As of 16 June 2022, we have renamed the [Floating
                IP](https://docs.digitalocean.com/reference/api/api-reference/#tag/Floating-IPs)

                product to Reserved IPs. The Reserved IP product's endpoints
                function the exact

                same way as Floating IPs. The only difference is the name change
                throughout the

                URLs and fields. For example, the `floating_ips` field is now
                the `reserved_ips` field.

                The Floating IP endpoints will remain active until fall 2023
                before being

                permanently deprecated.


                With the exception of the [Projects
                API](https://docs.digitalocean.com/reference/api/api-reference/#tag/Projects),

                we will reflect this change as an additional field in the
                responses across the API

                where the `floating_ip` field is used. For example, the Droplet
                metadata response

                will contain the field `reserved_ips` in addition to the
                `floating_ips` field.

                Floating IPs retrieved using the Projects API will retain the
                original name.


                Reserved IP actions are commands that can be given to a
                DigitalOcean

                reserved IP. These requests are made on the actions endpoint of
                a specific

                reserved IP.


                An action object is returned. These objects hold the current
                status of the

                requested action.
            - name: Reserved IPs
              description: >-
                As of 16 June 2022, we have renamed the [Floating
                IP](https://docs.digitalocean.com/reference/api/api-reference/#tag/Floating-IPs)

                product to Reserved IPs. The Reserved IP product's endpoints
                function the exact

                same way as Floating IPs. The only difference is the name change
                throughout the

                URLs and fields. For example, the `floating_ips` field is now
                the `reserved_ips` field.

                The Floating IP endpoints will remain active until fall 2023
                before being

                permanently deprecated.


                With the exception of the [Projects
                API](https://docs.digitalocean.com/reference/api/api-reference/#tag/Projects),

                we will reflect this change as an additional field in the
                responses across the API

                where the `floating_ip` field is used. For example, the Droplet
                metadata response

                will contain the field `reserved_ips` in addition to the
                `floating_ips` field.

                Floating IPs retrieved using the Projects API will retain the
                original name.


                DigitalOcean Reserved IPs are publicly-accessible static IP
                addresses that can be

                mapped to one of your Droplets. They can be used to create
                highly available

                setups or other configurations requiring movable addresses.


                Reserved IPs are bound to a specific region.
            - name: Sizes
              description: >-
                The sizes objects represent different packages of hardware
                resources that

                can be used for Droplets. When a Droplet is created, a size must
                be

                selected so that the correct resources can be allocated.


                Each size represents a plan that bundles together specific sets
                of

                resources. This includes the amount of RAM, the number of
                virtual CPUs,

                disk space, and transfer. The size object also includes the
                pricing

                details and the regions that the size is available in.
            - name: Snapshots
              description: >-
                [Snapshots](https://www.digitalocean.com/docs/images/snapshots/)
                are saved

                instances of a Droplet or a block storage volume, which is
                reflected in

                the `resource_type` attribute. In order to avoid problems with
                compressing

                filesystems, each defines a `min_disk_size` attribute which is
                the minimum

                size of the Droplet or volume disk when creating a new resource
                from the

                saved snapshot.


                To interact with snapshots, you will generally send requests to
                the

                snapshots endpoint at `/v2/snapshots`.
            - name: SSH Keys
              description: Manage SSH keys available on your account.
            - name: Tags
              description: >-
                A tag is a label that can be applied to a resource (currently
                Droplets,

                Images, Volumes, Volume Snapshots, and Database clusters) in
                order to

                better organize or facilitate the lookups and actions on it.


                Tags have two attributes: a user defined `name` attribute and an
                embedded

                `resources` attribute with information about resources that have
                been tagged.
            - name: Uptime
              description: >-
                [DigitalOcean Uptime
                Checks](https://docs.digitalocean.com/products/uptime/) provide
                the ability to monitor your endpoints from around the world, and
                alert you when they're slow, unavailable, or SSL certificates
                are expiring.

                To interact with Uptime, you will generally send requests to the
                Uptime endpoint at `/v2/uptime/`.
            - name: VPCs
              description: >-
                [VPCs (virtual private
                clouds)](https://www.digitalocean.com/docs/networking/vpc/)

                allow you to create virtual networks containing resources that
                can

                communicate with each other in full isolation using private IP
                addresses.


                By sending requests to the `/v2/vpcs` endpoint, you can create,
                configure,

                list, and delete custom VPCs as well as retrieve information
                about the

                resources assigned to them.
          paths:
            /v2/1-clicks:
              get: {}
            /v2/1-clicks/kubernetes:
              post: {}
            /v2/account:
              get: {}
            /v2/account/keys:
              get: {}
              post: {}
            /v2/account/keys/{ssh_key_identifier}:
              get: {}
              put: {}
              delete: {}
            /v2/actions:
              get: {}
            /v2/actions/{action_id}:
              get: {}
            /v2/apps:
              get: {}
              post: {}
            /v2/apps/{id}:
              delete: {}
              get: {}
              put: {}
            /v2/apps/{app_id}/components/{component_name}/logs:
              get: {}
            /v2/apps/{app_id}/deployments:
              get: {}
              post: {}
            /v2/apps/{app_id}/deployments/{deployment_id}:
              get: {}
            /v2/apps/{app_id}/deployments/{deployment_id}/cancel:
              post: {}
            /v2/apps/{app_id}/deployments/{deployment_id}/components/{component_name}/logs:
              get: {}
            /v2/apps/{app_id}/deployments/{deployment_id}/logs:
              get: {}
            /v2/apps/{app_id}/logs:
              get: {}
            /v2/apps/tiers:
              get: {}
            /v2/apps/tiers/{slug}:
              get: {}
            /v2/apps/tiers/instance_sizes:
              get: {}
            /v2/apps/tiers/instance_sizes/{slug}:
              get: {}
            /v2/apps/regions:
              get: {}
            /v2/apps/propose:
              post: {}
            /v2/apps/{app_id}/alerts:
              get: {}
            /v2/apps/{app_id}/alerts/{alert_id}/destinations:
              post: {}
            /v2/apps/{app_id}/rollback:
              post: {}
            /v2/apps/{app_id}/rollback/validate:
              post: {}
            /v2/apps/{app_id}/rollback/commit:
              post: {}
            /v2/apps/{app_id}/rollback/revert:
              post: {}
            /v2/apps/{app_id}/metrics/bandwidth_daily:
              get: {}
            /v2/apps/metrics/bandwidth_daily:
              post: {}
            /v2/cdn/endpoints:
              get: {}
              post: {}
            /v2/cdn/endpoints/{cdn_id}:
              get: {}
              put: {}
              delete: {}
            /v2/cdn/endpoints/{cdn_id}/cache:
              delete: {}
            /v2/certificates:
              get: {}
              post: {}
            /v2/certificates/{certificate_id}:
              get: {}
              delete: {}
            /v2/customers/my/balance:
              get: {}
            /v2/customers/my/billing_history:
              get: {}
            /v2/customers/my/invoices:
              get: {}
            /v2/customers/my/invoices/{invoice_uuid}:
              get: {}
            /v2/customers/my/invoices/{invoice_uuid}/csv:
              get: {}
            /v2/customers/my/invoices/{invoice_uuid}/pdf:
              get: {}
            /v2/customers/my/invoices/{invoice_uuid}/summary:
              get: {}
            /v2/databases/options:
              get: {}
            /v2/databases:
              get: {}
              post: {}
            /v2/databases/{database_cluster_uuid}:
              get: {}
              delete: {}
            /v2/databases/{database_cluster_uuid}/config:
              get: {}
              patch: {}
            /v2/databases/{database_cluster_uuid}/ca:
              get: {}
            /v2/databases/{database_cluster_uuid}/online-migration:
              get: {}
              put: {}
            /v2/databases/{database_cluster_uuid}/online-migration/{migration_id}:
              delete: {}
            /v2/databases/{database_cluster_uuid}/migrate:
              put: {}
            /v2/databases/{database_cluster_uuid}/resize:
              put: {}
            /v2/databases/{database_cluster_uuid}/firewall:
              get: {}
              put: {}
            /v2/databases/{database_cluster_uuid}/maintenance:
              put: {}
            /v2/databases/{database_cluster_uuid}/backups:
              get: {}
            /v2/databases/{database_cluster_uuid}/replicas:
              get: {}
              post: {}
            /v2/databases/{database_cluster_uuid}/events:
              get: {}
            /v2/databases/{database_cluster_uuid}/replicas/{replica_name}:
              get: {}
              delete: {}
            /v2/databases/{database_cluster_uuid}/replicas/{replica_name}/promote:
              put: {}
            /v2/databases/{database_cluster_uuid}/users:
              get: {}
              post: {}
            /v2/databases/{database_cluster_uuid}/users/{username}:
              get: {}
              delete: {}
              put: {}
            /v2/databases/{database_cluster_uuid}/users/{username}/reset_auth:
              post: {}
            /v2/databases/{database_cluster_uuid}/dbs:
              get: {}
              post: {}
            /v2/databases/{database_cluster_uuid}/dbs/{database_name}:
              get: {}
              delete: {}
            /v2/databases/{database_cluster_uuid}/pools:
              get: {}
              post: {}
            /v2/databases/{database_cluster_uuid}/pools/{pool_name}:
              get: {}
              put: {}
              delete: {}
            /v2/databases/{database_cluster_uuid}/eviction_policy:
              get: {}
              put: {}
            /v2/databases/{database_cluster_uuid}/sql_mode:
              get: {}
              put: {}
            /v2/databases/{database_cluster_uuid}/upgrade:
              put: {}
            /v2/databases/{database_cluster_uuid}/topics:
              get: {}
              post: {}
            /v2/databases/{database_cluster_uuid}/topics/{topic_name}:
              get: {}
              put: {}
              delete: {}
            /v2/databases/metrics/credentials:
              get: {}
              put: {}
            /v2/domains:
              get: {}
              post: {}
            /v2/domains/{domain_name}:
              get: {}
              delete: {}
            /v2/domains/{domain_name}/records:
              get: {}
              post: {}
            /v2/domains/{domain_name}/records/{domain_record_id}:
              get: {}
              patch: {}
              put: {}
              delete: {}
            /v2/droplets:
              get: {}
              post: {}
              delete: {}
            /v2/droplets/{droplet_id}:
              get: {}
              delete: {}
            /v2/droplets/{droplet_id}/backups:
              get: {}
            /v2/droplets/{droplet_id}/snapshots:
              get: {}
            /v2/droplets/{droplet_id}/actions:
              get: {}
              post: {}
            /v2/droplets/actions:
              post: {}
            /v2/droplets/{droplet_id}/actions/{action_id}:
              get: {}
            /v2/droplets/{droplet_id}/kernels:
              get: {}
            /v2/droplets/{droplet_id}/firewalls:
              get: {}
            /v2/droplets/{droplet_id}/neighbors:
              get: {}
            /v2/droplets/{droplet_id}/destroy_with_associated_resources:
              get: {}
            /v2/droplets/{droplet_id}/destroy_with_associated_resources/selective:
              delete: {}
            /v2/droplets/{droplet_id}/destroy_with_associated_resources/dangerous:
              delete: {}
            /v2/droplets/{droplet_id}/destroy_with_associated_resources/status:
              get: {}
            /v2/droplets/{droplet_id}/destroy_with_associated_resources/retry:
              post: {}
            /v2/firewalls:
              get: {}
              post: {}
            /v2/firewalls/{firewall_id}:
              get: {}
              put: {}
              delete: {}
            /v2/firewalls/{firewall_id}/droplets:
              post: {}
              delete: {}
            /v2/firewalls/{firewall_id}/tags:
              post: {}
              delete: {}
            /v2/firewalls/{firewall_id}/rules:
              post: {}
              delete: {}
            /v2/floating_ips:
              get: {}
              post: {}
            /v2/floating_ips/{floating_ip}:
              get: {}
              delete: {}
            /v2/floating_ips/{floating_ip}/actions:
              get: {}
              post: {}
            /v2/floating_ips/{floating_ip}/actions/{action_id}:
              get: {}
            /v2/functions/namespaces:
              get: {}
              post: {}
            /v2/functions/namespaces/{namespace_id}:
              get: {}
              delete: {}
            /v2/functions/namespaces/{namespace_id}/triggers:
              get: {}
              post: {}
            /v2/functions/namespaces/{namespace_id}/triggers/{trigger_name}:
              get: {}
              put: {}
              delete: {}
            /v2/images:
              get: {}
              post: {}
            /v2/images/{image_id}:
              get: {}
              put: {}
              delete: {}
            /v2/images/{image_id}/actions:
              get: {}
              post: {}
            /v2/images/{image_id}/actions/{action_id}:
              get: {}
            /v2/kubernetes/clusters:
              get: {}
              post: {}
            /v2/kubernetes/clusters/{cluster_id}:
              get: {}
              put: {}
              delete: {}
            /v2/kubernetes/clusters/{cluster_id}/destroy_with_associated_resources:
              get: {}
            /v2/kubernetes/clusters/{cluster_id}/destroy_with_associated_resources/selective:
              delete: {}
            /v2/kubernetes/clusters/{cluster_id}/destroy_with_associated_resources/dangerous:
              delete: {}
            /v2/kubernetes/clusters/{cluster_id}/kubeconfig:
              get: {}
            /v2/kubernetes/clusters/{cluster_id}/credentials:
              get: {}
            /v2/kubernetes/clusters/{cluster_id}/upgrades:
              get: {}
            /v2/kubernetes/clusters/{cluster_id}/upgrade:
              post: {}
            /v2/kubernetes/clusters/{cluster_id}/node_pools:
              get: {}
              post: {}
            /v2/kubernetes/clusters/{cluster_id}/node_pools/{node_pool_id}:
              get: {}
              put: {}
              delete: {}
            /v2/kubernetes/clusters/{cluster_id}/node_pools/{node_pool_id}/nodes/{node_id}:
              delete: {}
            /v2/kubernetes/clusters/{cluster_id}/node_pools/{node_pool_id}/recycle:
              post: {}
            /v2/kubernetes/clusters/{cluster_id}/user:
              get: {}
            /v2/kubernetes/options:
              get: {}
            /v2/kubernetes/clusters/{cluster_id}/clusterlint:
              post: {}
              get: {}
            /v2/kubernetes/registry:
              post: {}
              delete: {}
            /v2/load_balancers:
              post: {}
              get: {}
            /v2/load_balancers/{lb_id}:
              get: {}
              put: {}
              delete: {}
            /v2/load_balancers/{lb_id}/droplets:
              post: {}
              delete: {}
            /v2/load_balancers/{lb_id}/forwarding_rules:
              post: {}
              delete: {}
            /v2/monitoring/alerts:
              get: {}
              post: {}
            /v2/monitoring/alerts/{alert_uuid}:
              get: {}
              put: {}
              delete: {}
            /v2/monitoring/metrics/droplet/bandwidth:
              get: {}
            /v2/monitoring/metrics/droplet/cpu:
              get: {}
            /v2/monitoring/metrics/droplet/filesystem_free:
              get: {}
            /v2/monitoring/metrics/droplet/filesystem_size:
              get: {}
            /v2/monitoring/metrics/droplet/load_1:
              get: {}
            /v2/monitoring/metrics/droplet/load_5:
              get: {}
            /v2/monitoring/metrics/droplet/load_15:
              get: {}
            /v2/monitoring/metrics/droplet/memory_cached:
              get: {}
            /v2/monitoring/metrics/droplet/memory_free:
              get: {}
            /v2/monitoring/metrics/droplet/memory_total:
              get: {}
            /v2/monitoring/metrics/droplet/memory_available:
              get: {}
            /v2/monitoring/metrics/apps/memory_percentage:
              get: {}
            /v2/monitoring/metrics/apps/cpu_percentage:
              get: {}
            /v2/monitoring/metrics/apps/restart_count:
              get: {}
            /v2/projects:
              get: {}
              post: {}
            /v2/projects/default:
              get: {}
              put: {}
              patch: {}
            /v2/projects/{project_id}:
              get: {}
              put: {}
              patch: {}
              delete: {}
            /v2/projects/{project_id}/resources:
              get: {}
              post: {}
            /v2/projects/default/resources:
              get: {}
              post: {}
            /v2/regions:
              get: {}
            /v2/registry:
              get: {}
              post: {}
              delete: {}
            /v2/registry/subscription:
              get: {}
              post: {}
            /v2/registry/docker-credentials:
              get: {}
            /v2/registry/validate-name:
              post: {}
            /v2/registry/{registry_name}/repositories:
              get: {}
            /v2/registry/{registry_name}/repositoriesV2:
              get: {}
            /v2/registry/{registry_name}/repositories/{repository_name}/tags:
              get: {}
            /v2/registry/{registry_name}/repositories/{repository_name}/tags/{repository_tag}:
              delete: {}
            /v2/registry/{registry_name}/repositories/{repository_name}/digests:
              get: {}
            /v2/registry/{registry_name}/repositories/{repository_name}/digests/{manifest_digest}:
              delete: {}
            /v2/registry/{registry_name}/garbage-collection:
              post: {}
              get: {}
            /v2/registry/{registry_name}/garbage-collections:
              get: {}
            /v2/registry/{registry_name}/garbage-collection/{garbage_collection_uuid}:
              put: {}
            /v2/registry/options:
              get: {}
            /v2/reports/droplet_neighbors_ids:
              get: {}
            /v2/reserved_ips:
              get: {}
              post: {}
            /v2/reserved_ips/{reserved_ip}:
              get: {}
              delete: {}
            /v2/reserved_ips/{reserved_ip}/actions:
              get: {}
              post: {}
            /v2/reserved_ips/{reserved_ip}/actions/{action_id}:
              get: {}
            /v2/sizes:
              get: {}
            /v2/snapshots:
              get: {}
            /v2/snapshots/{snapshot_id}:
              get: {}
              delete: {}
            /v2/tags:
              get: {}
              post: {}
            /v2/tags/{tag_id}:
              get: {}
              delete: {}
            /v2/tags/{tag_id}/resources:
              post: {}
              delete: {}
            /v2/volumes:
              get: {}
              post: {}
              delete: {}
            /v2/volumes/actions:
              post: {}
            /v2/volumes/snapshots/{snapshot_id}:
              get: {}
              delete: {}
            /v2/volumes/{volume_id}:
              get: {}
              delete: {}
            /v2/volumes/{volume_id}/actions:
              get: {}
              post: {}
            /v2/volumes/{volume_id}/actions/{action_id}:
              get: {}
            /v2/volumes/{volume_id}/snapshots:
              get: {}
              post: {}
            /v2/vpcs:
              get: {}
              post: {}
            /v2/vpcs/{vpc_id}:
              get: {}
              put: {}
              patch: {}
              delete: {}
            /v2/vpcs/{vpc_id}/members:
              get: {}
            /v2/uptime/checks:
              get: {}
              post: {}
            /v2/uptime/checks/{check_id}:
              get: {}
              put: {}
              delete: {}
            /v2/uptime/checks/{check_id}/state:
              get: {}
            /v2/uptime/checks/{check_id}/alerts:
              get: {}
              post: {}
            /v2/uptime/checks/{check_id}/alerts/{alert_id}:
              get: {}
              put: {}
              delete: {}
    aid: digital-ocean:digital-ocean-api
    overlays:
      - type: APIs.io Search
        url: overlays/digital-ocean-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---