---
name: Aggregations
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/aggregations.png
url: https://example.com/apis/aggregations.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Aggregations
apis:
  - name: imagebuilder
    description: >-
      <p>EC2 Image Builder is a fully managed Amazon Web Services service that
      makes it easier to automate the creation, management, and deployment of
      customized, secure, and up-to-date "golden" server images that are
      pre-installed and pre-configured with software and settings to meet
      specific IT standards.</p>
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
            title: imagebuilder
          paths:
            /CancelImageCreation:
              PUT:
                summary: CancelImageCreation
                description: >-
                  <p>CancelImageCreation cancels the creation of Image. This
                  operation can only be used on images in a non-terminal
                  state.</p>
                tags:
                  - Cancel
                  - Images
                  - Creation
                  - Cancel
                  - Images
                  - Creation
            /CancelLifecycleExecution:
              PUT:
                summary: CancelLifecycleExecution
                description: >-
                  <p>Cancel a specific image lifecycle policy runtime
                  instance.</p>
                tags:
                  - Cancel
                  - Lifecycle
                  - Execution
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
            /CreateComponent:
              PUT:
                summary: CreateComponent
                description: >-
                  <p>Creates a new component that can be used to build,
                  validate, test, and assess your image. The component is based
                  on a YAML document that you specify using exactly one of the
                  following methods:</p> <ul> <li> <p>Inline, using the
                  <code>data</code> property in the request body.</p> </li> <li>
                  <p>A URL that points to a YAML document file stored in Amazon
                  S3, using the <code>uri</code> property in the request
                  body.</p> </li> </ul>
                tags:
                  - Create
                  - Components
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
            /CreateContainerRecipe:
              PUT:
                summary: CreateContainerRecipe
                description: >-
                  <p>Creates a new container recipe. Container recipes define
                  how images are configured, tested, and assessed.</p>
                tags:
                  - Create
                  - Container
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
            /CreateDistributionConfiguration:
              PUT:
                summary: CreateDistributionConfiguration
                description: >-
                  <p>Creates a new distribution configuration. Distribution
                  configurations define and configure the outputs of your
                  pipeline.</p>
                tags:
                  - Create
                  - Distributions
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
            /CreateImage:
              PUT:
                summary: CreateImage
                description: >-
                  <p>Creates a new image. This request will create a new image
                  along with all of the configured output resources defined in
                  the distribution configuration. You must specify exactly one
                  recipe for your image, using either a ContainerRecipeArn or an
                  ImageRecipeArn.</p>
                tags:
                  - Create
                  - Images
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
            /CreateImagePipeline:
              PUT:
                summary: CreateImagePipeline
                description: >-
                  <p>Creates a new image pipeline. Image pipelines enable you to
                  automate the creation and distribution of images.</p>
                tags:
                  - Create
                  - Images
                  - Pipelines
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
            /CreateImageRecipe:
              PUT:
                summary: CreateImageRecipe
                description: >-
                  <p>Creates a new image recipe. Image recipes define how images
                  are configured, tested, and assessed.</p>
                tags:
                  - Create
                  - Images
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
            /CreateInfrastructureConfiguration:
              PUT:
                summary: CreateInfrastructureConfiguration
                description: >-
                  <p>Creates a new infrastructure configuration. An
                  infrastructure configuration defines the environment in which
                  your image will be built and tested.</p>
                tags:
                  - Create
                  - Infrastructure
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
            /CreateLifecyclePolicy:
              PUT:
                summary: CreateLifecyclePolicy
                description: <p>Create a lifecycle policy resource.</p>
                tags:
                  - Create
                  - Lifecycle
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
            /CreateWorkflow:
              PUT:
                summary: CreateWorkflow
                description: >-
                  <p>Create a new workflow or a new version of an existing
                  workflow.</p>
                tags:
                  - Create
                  - Workflows
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
            /DeleteComponent:
              DELETE:
                summary: DeleteComponent
                description: <p>Deletes a component build version.</p>
                tags:
                  - Delete
                  - Components
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteContainerRecipe:
              DELETE:
                summary: DeleteContainerRecipe
                description: <p>Deletes a container recipe.</p>
                tags:
                  - Delete
                  - Container
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteDistributionConfiguration:
              DELETE:
                summary: DeleteDistributionConfiguration
                description: <p>Deletes a distribution configuration.</p>
                tags:
                  - Delete
                  - Distributions
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteImage:
              DELETE:
                summary: DeleteImage
                description: >-
                  <p>Deletes an Image Builder image resource. This does not
                  delete any EC2 AMIs or ECR container images that are created
                  during the image build process. You must clean those up
                  separately, using the appropriate Amazon EC2 or Amazon ECR
                  console actions, or API or CLI commands.</p> <ul> <li> <p>To
                  deregister an EC2 Linux AMI, see <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/deregister-ami.html">Deregister
                  your Linux AMI</a> in the <i> <i>Amazon EC2 User Guide</i>
                  </i>.</p> </li> <li> <p>To deregister an EC2 Windows AMI, see
                  <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/deregister-ami.html">Deregister
                  your Windows AMI</a> in the <i> <i>Amazon EC2 Windows
                  Guide</i> </i>.</p> </li> <li> <p>To delete a container image
                  from Amazon ECR, see <a
                  href="https://docs.aws.amazon.com/AmazonECR/latest/userguide/delete_image.html">Deleting
                  an image</a> in the <i>Amazon ECR User Guide</i>.</p> </li>
                  </ul>
                tags:
                  - Delete
                  - Images
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteImagePipeline:
              DELETE:
                summary: DeleteImagePipeline
                description: <p>Deletes an image pipeline.</p>
                tags:
                  - Delete
                  - Images
                  - Pipelines
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteImageRecipe:
              DELETE:
                summary: DeleteImageRecipe
                description: <p>Deletes an image recipe.</p>
                tags:
                  - Delete
                  - Images
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteInfrastructureConfiguration:
              DELETE:
                summary: DeleteInfrastructureConfiguration
                description: <p>Deletes an infrastructure configuration.</p>
                tags:
                  - Delete
                  - Infrastructure
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteLifecyclePolicy:
              DELETE:
                summary: DeleteLifecyclePolicy
                description: <p>Delete the specified lifecycle policy resource.</p>
                tags:
                  - Delete
                  - Lifecycle
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /DeleteWorkflow:
              DELETE:
                summary: DeleteWorkflow
                description: <p>Deletes a specific workflow resource.</p>
                tags:
                  - Delete
                  - Workflows
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
            /GetComponent:
              GET:
                summary: GetComponent
                description: <p>Gets a component object.</p>
                tags:
                  - Get
                  - Components
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetComponentPolicy:
              GET:
                summary: GetComponentPolicy
                description: <p>Gets a component policy.</p>
                tags:
                  - Get
                  - Components
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetContainerRecipe:
              GET:
                summary: GetContainerRecipe
                description: <p>Retrieves a container recipe.</p>
                tags:
                  - Get
                  - Container
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetContainerRecipePolicy:
              GET:
                summary: GetContainerRecipePolicy
                description: <p>Retrieves the policy for a container recipe.</p>
                tags:
                  - Get
                  - Container
                  - Recipes
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetDistributionConfiguration:
              GET:
                summary: GetDistributionConfiguration
                description: <p>Gets a distribution configuration.</p>
                tags:
                  - Get
                  - Distributions
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetImage:
              GET:
                summary: GetImage
                description: <p>Gets an image.</p>
                tags:
                  - Get
                  - Images
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetImagePipeline:
              GET:
                summary: GetImagePipeline
                description: <p>Gets an image pipeline.</p>
                tags:
                  - Get
                  - Images
                  - Pipelines
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetImagePolicy:
              GET:
                summary: GetImagePolicy
                description: <p>Gets an image policy.</p>
                tags:
                  - Get
                  - Images
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetImageRecipe:
              GET:
                summary: GetImageRecipe
                description: <p>Gets an image recipe.</p>
                tags:
                  - Get
                  - Images
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetImageRecipePolicy:
              GET:
                summary: GetImageRecipePolicy
                description: <p>Gets an image recipe policy.</p>
                tags:
                  - Get
                  - Images
                  - Recipes
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetInfrastructureConfiguration:
              GET:
                summary: GetInfrastructureConfiguration
                description: <p>Gets an infrastructure configuration.</p>
                tags:
                  - Get
                  - Infrastructure
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetLifecycleExecution:
              GET:
                summary: GetLifecycleExecution
                description: >-
                  <p>Get the runtime information that was logged for a specific
                  runtime instance of the lifecycle policy.</p>
                tags:
                  - Get
                  - Lifecycle
                  - Execution
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetLifecyclePolicy:
              GET:
                summary: GetLifecyclePolicy
                description: <p>Get details for the specified image lifecycle policy.</p>
                tags:
                  - Get
                  - Lifecycle
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetWorkflow:
              GET:
                summary: GetWorkflow
                description: <p>Get a workflow resource object.</p>
                tags:
                  - Get
                  - Workflows
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetWorkflowExecution:
              GET:
                summary: GetWorkflowExecution
                description: >-
                  <p>Get the runtime information that was logged for a specific
                  runtime instance of the workflow.</p>
                tags:
                  - Get
                  - Workflows
                  - Execution
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
            /GetWorkflowStepExecution:
              GET:
                summary: GetWorkflowStepExecution
                description: >-
                  <p>Get the runtime information that was logged for a specific
                  runtime instance of the workflow step.</p>
                tags:
                  - Get
                  - Workflows
                  - Steps
                  - Execution
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
            /ImportComponent:
              PUT:
                summary: ImportComponent
                description: >-
                  <p>Imports a component and transforms its data into a
                  component document.</p>
                tags:
                  - Import
                  - Components
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
            /ImportVmImage:
              PUT:
                summary: ImportVmImage
                description: >-
                  <p>When you export your virtual machine (VM) from its
                  virtualization environment, that process creates a set of one
                  or more disk container files that act as snapshots of your
                  VM’s environment, settings, and data. The Amazon EC2 API <a
                  href="https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportImage.html">ImportImage</a>
                  action uses those files to import your VM and create an AMI.
                  To import using the CLI command, see <a
                  href="https://docs.aws.amazon.com/cli/latest/reference/ec2/import-image.html">import-image</a>
                  </p> <p>You can reference the task ID from the VM import to
                  pull in the AMI that the import created as the base image for
                  your Image Builder recipe.</p>
                tags:
                  - Import
                  - Vm
                  - Images
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
            /ListComponentBuildVersions:
              POST:
                summary: ListComponentBuildVersions
                description: >-
                  <p>Returns the list of component build versions for the
                  specified semantic version.</p> <note> <p>The semantic version
                  has four nodes:
                  &lt;major&gt;.&lt;minor&gt;.&lt;patch&gt;/&lt;build&gt;. You
                  can assign values for the first three, and can filter on all
                  of them.</p> <p> <b>Filtering:</b> With semantic versioning,
                  you have the flexibility to use wildcards (x) to specify the
                  most recent versions or nodes when selecting the base image or
                  components for your recipe. When you use a wildcard in any
                  node, all nodes to the right of the first wildcard must also
                  be wildcards.</p> </note>
                tags:
                  - Lists
                  - Components
                  - Build
                  - Versions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
            /ListComponents:
              POST:
                summary: ListComponents
                description: >-
                  <p>Returns the list of components that can be filtered by
                  name, or by using the listed <code>filters</code> to
                  streamline results. Newly created components can take up to
                  two minutes to appear in the ListComponents API Results.</p>
                  <note> <p>The semantic version has four nodes:
                  &lt;major&gt;.&lt;minor&gt;.&lt;patch&gt;/&lt;build&gt;. You
                  can assign values for the first three, and can filter on all
                  of them.</p> <p> <b>Filtering:</b> With semantic versioning,
                  you have the flexibility to use wildcards (x) to specify the
                  most recent versions or nodes when selecting the base image or
                  components for your recipe. When you use a wildcard in any
                  node, all nodes to the right of the first wildcard must also
                  be wildcards.</p> </note>
                tags:
                  - Lists
                  - Components
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
            /ListContainerRecipes:
              POST:
                summary: ListContainerRecipes
                description: <p>Returns a list of container recipes.</p>
                tags:
                  - Lists
                  - Container
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
            /ListDistributionConfigurations:
              POST:
                summary: ListDistributionConfigurations
                description: <p>Returns a list of distribution configurations.</p>
                tags:
                  - Lists
                  - Distributions
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
            /ListImageBuildVersions:
              POST:
                summary: ListImageBuildVersions
                description: <p>Returns a list of image build versions.</p>
                tags:
                  - Lists
                  - Images
                  - Build
                  - Versions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
            /ListImagePackages:
              POST:
                summary: ListImagePackages
                description: >-
                  <p>List the Packages that are associated with an Image Build
                  Version, as determined by Amazon Web Services Systems Manager
                  Inventory at build time.</p>
                tags:
                  - Lists
                  - Images
                  - Packages
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
            /ListImagePipelineImages:
              POST:
                summary: ListImagePipelineImages
                description: >-
                  <p>Returns a list of images created by the specified
                  pipeline.</p>
                tags:
                  - Lists
                  - Images
                  - Pipelines
                  - Images
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
            /ListImagePipelines:
              POST:
                summary: ListImagePipelines
                description: <p>Returns a list of image pipelines.</p>
                tags:
                  - Lists
                  - Images
                  - Pipelines
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
            /ListImageRecipes:
              POST:
                summary: ListImageRecipes
                description: <p>Returns a list of image recipes.</p>
                tags:
                  - Lists
                  - Images
                  - Recipes
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
            /ListImageScanFindingAggregations:
              POST:
                summary: ListImageScanFindingAggregations
                description: >-
                  <p>Returns a list of image scan aggregations for your account.
                  You can filter by the type of key that Image Builder uses to
                  group results. For example, if you want to get a list of
                  findings by severity level for one of your pipelines, you
                  might specify your pipeline with the
                  <code>imagePipelineArn</code> filter. If you don't specify a
                  filter, Image Builder returns an aggregation for your
                  account.</p> <p>To streamline results, you can use the
                  following filters in your request:</p> <ul> <li> <p>
                  <code>accountId</code> </p> </li> <li> <p>
                  <code>imageBuildVersionArn</code> </p> </li> <li> <p>
                  <code>imagePipelineArn</code> </p> </li> <li> <p>
                  <code>vulnerabilityId</code> </p> </li> </ul>
                tags:
                  - Lists
                  - Images
                  - Scans
                  - Findings
                  - Aggregations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
            /ListImageScanFindings:
              POST:
                summary: ListImageScanFindings
                description: <p>Returns a list of image scan findings for your account.</p>
                tags:
                  - Lists
                  - Images
                  - Scans
                  - Findings
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
            /ListImages:
              POST:
                summary: ListImages
                description: >-
                  <p>Returns the list of images that you have access to. Newly
                  created images can take up to two minutes to appear in the
                  ListImages API Results.</p>
                tags:
                  - Lists
                  - Images
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
            /ListInfrastructureConfigurations:
              POST:
                summary: ListInfrastructureConfigurations
                description: <p>Returns a list of infrastructure configurations.</p>
                tags:
                  - Lists
                  - Infrastructure
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
            /ListLifecycleExecutionResources:
              POST:
                summary: ListLifecycleExecutionResources
                description: >-
                  <p>List resources that the runtime instance of the image
                  lifecycle identified for lifecycle actions.</p>
                tags:
                  - Lists
                  - Lifecycle
                  - Execution
                  - Resources
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
            /ListLifecycleExecutions:
              POST:
                summary: ListLifecycleExecutions
                description: >-
                  <p>Get the lifecycle runtime history for the specified
                  resource.</p>
                tags:
                  - Lists
                  - Lifecycle
                  - Executions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
            /ListLifecyclePolicies:
              POST:
                summary: ListLifecyclePolicies
                description: >-
                  <p>Get a list of lifecycle policies in your Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Lifecycle
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
            /ListWaitingWorkflowSteps:
              POST:
                summary: ListWaitingWorkflowSteps
                description: >-
                  <p>Get a list of workflow steps that are waiting for action
                  for workflows in your Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Waiting
                  - Workflows
                  - Steps
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
            /ListWorkflowBuildVersions:
              POST:
                summary: ListWorkflowBuildVersions
                description: >-
                  <p>Returns a list of build versions for a specific workflow
                  resource.</p>
                tags:
                  - Lists
                  - Workflows
                  - Build
                  - Versions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
            /ListWorkflowExecutions:
              POST:
                summary: ListWorkflowExecutions
                description: >-
                  <p>Returns a list of workflow runtime instance metadata
                  objects for a specific image build version.</p>
                tags:
                  - Lists
                  - Workflows
                  - Executions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
            /ListWorkflowStepExecutions:
              POST:
                summary: ListWorkflowStepExecutions
                description: >-
                  <p>Returns runtime data for each step in a runtime instance of
                  the workflow that you specify in the request.</p>
                tags:
                  - Lists
                  - Workflows
                  - Steps
                  - Executions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
            /ListWorkflows:
              POST:
                summary: ListWorkflows
                description: >-
                  <p>Lists workflow build versions based on filtering
                  parameters.</p>
                tags:
                  - Lists
                  - Workflows
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
            /PutComponentPolicy:
              PUT:
                summary: PutComponentPolicy
                description: >-
                  <p>Applies a policy to a component. We recommend that you call
                  the RAM API <a
                  href="https://docs.aws.amazon.com/ram/latest/APIReference/API_CreateResourceShare.html">CreateResourceShare</a>
                  to share resources. If you call the Image Builder API
                  <code>PutComponentPolicy</code>, you must also call the RAM
                  API <a
                  href="https://docs.aws.amazon.com/ram/latest/APIReference/API_PromoteResourceShareCreatedFromPolicy.html">PromoteResourceShareCreatedFromPolicy</a>
                  in order for the resource to be visible to all principals with
                  whom the resource is shared.</p>
                tags:
                  - Put
                  - Components
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
            /PutContainerRecipePolicy:
              PUT:
                summary: PutContainerRecipePolicy
                description: >-
                  <p>Applies a policy to a container image. We recommend that
                  you call the RAM API CreateResourceShare
                  (https://docs.aws.amazon.com//ram/latest/APIReference/API_CreateResourceShare.html)
                  to share resources. If you call the Image Builder API
                  <code>PutContainerImagePolicy</code>, you must also call the
                  RAM API PromoteResourceShareCreatedFromPolicy
                  (https://docs.aws.amazon.com//ram/latest/APIReference/API_PromoteResourceShareCreatedFromPolicy.html)
                  in order for the resource to be visible to all principals with
                  whom the resource is shared.</p>
                tags:
                  - Put
                  - Container
                  - Recipes
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
            /PutImagePolicy:
              PUT:
                summary: PutImagePolicy
                description: >-
                  <p>Applies a policy to an image. We recommend that you call
                  the RAM API <a
                  href="https://docs.aws.amazon.com/ram/latest/APIReference/API_CreateResourceShare.html">CreateResourceShare</a>
                  to share resources. If you call the Image Builder API
                  <code>PutImagePolicy</code>, you must also call the RAM API <a
                  href="https://docs.aws.amazon.com/ram/latest/APIReference/API_PromoteResourceShareCreatedFromPolicy.html">PromoteResourceShareCreatedFromPolicy</a>
                  in order for the resource to be visible to all principals with
                  whom the resource is shared.</p>
                tags:
                  - Put
                  - Images
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
            /PutImageRecipePolicy:
              PUT:
                summary: PutImageRecipePolicy
                description: >-
                  <p>Applies a policy to an image recipe. We recommend that you
                  call the RAM API <a
                  href="https://docs.aws.amazon.com/ram/latest/APIReference/API_CreateResourceShare.html">CreateResourceShare</a>
                  to share resources. If you call the Image Builder API
                  <code>PutImageRecipePolicy</code>, you must also call the RAM
                  API <a
                  href="https://docs.aws.amazon.com/ram/latest/APIReference/API_PromoteResourceShareCreatedFromPolicy.html">PromoteResourceShareCreatedFromPolicy</a>
                  in order for the resource to be visible to all principals with
                  whom the resource is shared.</p>
                tags:
                  - Put
                  - Images
                  - Recipes
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
            /SendWorkflowStepAction:
              PUT:
                summary: SendWorkflowStepAction
                description: >-
                  <p>Pauses or resumes image creation when the associated
                  workflow runs a <code>WaitForAction</code> step.</p>
                tags:
                  - Send
                  - Workflows
                  - Steps
                  - Actions
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
            /StartImagePipelineExecution:
              PUT:
                summary: StartImagePipelineExecution
                description: <p>Manually triggers a pipeline to create an image.</p>
                tags:
                  - Start
                  - Images
                  - Pipelines
                  - Execution
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
                  - Start
            /StartResourceStateUpdate:
              PUT:
                summary: StartResourceStateUpdate
                description: >-
                  <p>Begin asynchronous resource state update for lifecycle
                  changes to the specified image resources.</p>
                tags:
                  - Start
                  - Resources
                  - States
                  - Update
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
                  - Start
                  - Resources
                  - States
                  - Update
            /UpdateDistributionConfiguration:
              PUT:
                summary: UpdateDistributionConfiguration
                description: >-
                  <p>Updates a new distribution configuration. Distribution
                  configurations define and configure the outputs of your
                  pipeline.</p>
                tags:
                  - Update
                  - Distributions
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
                  - Start
                  - Resources
                  - States
                  - Update
            /UpdateImagePipeline:
              PUT:
                summary: UpdateImagePipeline
                description: >-
                  <p>Updates an image pipeline. Image pipelines enable you to
                  automate the creation and distribution of images. You must
                  specify exactly one recipe for your image, using either a
                  <code>containerRecipeArn</code> or an
                  <code>imageRecipeArn</code>.</p> <note> <p>UpdateImagePipeline
                  does not support selective updates for the pipeline. You must
                  specify all of the required properties in the update request,
                  not just the properties that have changed.</p> </note>
                tags:
                  - Update
                  - Images
                  - Pipelines
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
                  - Start
                  - Resources
                  - States
                  - Update
            /UpdateInfrastructureConfiguration:
              PUT:
                summary: UpdateInfrastructureConfiguration
                description: >-
                  <p>Updates a new infrastructure configuration. An
                  infrastructure configuration defines the environment in which
                  your image will be built and tested.</p>
                tags:
                  - Update
                  - Infrastructure
                  - Configurations
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
                  - Start
                  - Resources
                  - States
                  - Update
            /UpdateLifecyclePolicy:
              PUT:
                summary: UpdateLifecyclePolicy
                description: <p>Update the specified lifecycle p
                tags:
                  - Update
                  - Lifecycle
                  - Policies
                  - Cancel
                  - Images
                  - Creation
                  - Lifecycle
                  - Execution
                  - Create
                  - Components
                  - Container
                  - Recipes
                  - Distributions
                  - Configurations
                  - Pipelines
                  - Infrastructure
                  - Policies
                  - Workflows
                  - Delete
                  - Get
                  - Steps
                  - Import
                  - Vm
                  - Lists
                  - Build
                  - Versions
                  - Components
                  - Recipes
                  - Configurations
                  - Packages
                  - Images
                  - Pipelines
                  - Scans
                  - Findings
                  - Aggregations
                  - Findings
                  - Resources
                  - Executions
                  - Policies
                  - ARN
                  - Waiting
                  - Steps
                  - Workflows
                  - Put
                  - Send
                  - Actions
                  - Start
                  - Resources
                  - States
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/imagebuilder-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/imagebuilder-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:imagebuilder
  - name: inspector2
    description: >-
      <p>Amazon Inspector is a vulnerability discovery service that automates
      continuous scanning for security vulnerabilities within your Amazon EC2,
      Amazon ECR, and Amazon Web Services Lambda environments.</p>
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
            title: inspector2
          paths:
            /members/associate:
              POST:
                summary: AssociateMember
                description: >-
                  <p>Associates an Amazon Web Services account with an Amazon
                  Inspector delegated administrator. An HTTP 200 response
                  indicates the association was successfully started, but
                  doesn’t indicate whether it was completed. You can check if
                  the association completed by using <a
                  href="https://docs.aws.amazon.com/inspector/v2/APIReference/API_ListMembers.html">ListMembers</a>
                  for multiple accounts or <a
                  href="https://docs.aws.amazon.com/inspector/v2/APIReference/API_GetMember.html">GetMembers</a>
                  for a single account.</p>
                tags:
                  - Associate
                  - Members
                  - Members
                  - Associate
            /status/batch/get:
              POST:
                summary: BatchGetAccountStatus
                description: >-
                  <p>Retrieves the Amazon Inspector status of multiple Amazon
                  Web Services accounts within your environment.</p>
                tags:
                  - Batches
                  - Get
                  - Account
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
            /codesnippet/batchget:
              POST:
                summary: BatchGetCodeSnippet
                description: >-
                  <p>Retrieves code snippets from findings that Amazon Inspector
                  detected code vulnerabilities in.</p>
                tags:
                  - Batches
                  - Get
                  - Code
                  - Snippets
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
            /findings/details/batch/get:
              POST:
                summary: BatchGetFindingDetails
                description: <p>Gets vulnerability details for findings.</p>
                tags:
                  - Batches
                  - Get
                  - Findings
                  - Details
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
            /freetrialinfo/batchget:
              POST:
                summary: BatchGetFreeTrialInfo
                description: >-
                  <p>Gets free trial status for multiple Amazon Web Services
                  accounts.</p>
                tags:
                  - Batches
                  - Get
                  - Free
                  - Trials
                  - Info
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
            /ec2deepinspectionstatus/member/batch/get:
              POST:
                summary: BatchGetMemberEc2DeepInspectionStatus
                description: >-
                  <p>Retrieves Amazon Inspector deep inspection activation
                  status of multiple member accounts within your organization.
                  You must be the delegated administrator of an organization in
                  Amazon Inspector to use this API.</p>
                tags:
                  - Batches
                  - Get
                  - Members
                  - EC2
                  - Deep
                  - Inspections
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
            /ec2deepinspectionstatus/member/batch/update:
              POST:
                summary: BatchUpdateMemberEc2DeepInspectionStatus
                description: >-
                  <p>Activates or deactivates Amazon Inspector deep inspection
                  for the provided member accounts in your organization. You
                  must be the delegated administrator of an organization in
                  Amazon Inspector to use this API.</p>
                tags:
                  - Batches
                  - Update
                  - Members
                  - EC2
                  - Deep
                  - Inspections
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
            /reporting/cancel:
              POST:
                summary: CancelFindingsReport
                description: <p>Cancels the given findings report.</p>
                tags:
                  - Cancel
                  - Findings
                  - Reports
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
            /sbomexport/cancel:
              POST:
                summary: CancelSbomExport
                description: <p>Cancels a software bill of materials (SBOM) report.</p>
                tags:
                  - Cancel
                  - Sbom
                  - Export
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
            /cis/scan-configuration/create:
              POST:
                summary: CreateCisScanConfiguration
                description: <p>Creates a CIS scan configuration.</p>
                tags:
                  - Create
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
            /filters/create:
              POST:
                summary: CreateFilter
                description: >-
                  <p>Creates a filter resource using specified filter criteria.
                  When the filter action is set to <code>SUPPRESS</code> this
                  action creates a suppression rule.</p>
                tags:
                  - Create
                  - Filter
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
            /reporting/create:
              POST:
                summary: CreateFindingsReport
                description: >-
                  <p>Creates a finding report. By default only
                  <code>ACTIVE</code> findings are returned in the report. To
                  see <code>SUPRESSED</code> or <code>CLOSED</code> findings you
                  must specify a value for the <code>findingStatus</code> filter
                  criteria. </p>
                tags:
                  - Create
                  - Findings
                  - Reports
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
            /sbomexport/create:
              POST:
                summary: CreateSbomExport
                description: <p>Creates a software bill of materials (SBOM) report.</p>
                tags:
                  - Create
                  - Sbom
                  - Export
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
            /cis/scan-configuration/delete:
              POST:
                summary: DeleteCisScanConfiguration
                description: <p>Deletes a CIS scan configuration.</p>
                tags:
                  - Delete
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
            /filters/delete:
              POST:
                summary: DeleteFilter
                description: <p>Deletes a filter resource.</p>
                tags:
                  - Delete
                  - Filter
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
            /organizationconfiguration/describe:
              POST:
                summary: DescribeOrganizationConfiguration
                description: >-
                  <p>Describe Amazon Inspector configuration settings for an
                  Amazon Web Services organization.</p>
                tags:
                  - Describe
                  - Organizations
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
            /disable:
              POST:
                summary: Disable
                description: >-
                  <p>Disables Amazon Inspector scans for one or more Amazon Web
                  Services accounts. Disabling all scan types in an account
                  disables the Amazon Inspector service.</p>
                tags:
                  - Disable
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
            /delegatedadminaccounts/disable:
              POST:
                summary: DisableDelegatedAdminAccount
                description: >-
                  <p>Disables the Amazon Inspector delegated administrator for
                  your organization.</p>
                tags:
                  - Disable
                  - Delegated
                  - Administrative
                  - Account
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
            /members/disassociate:
              POST:
                summary: DisassociateMember
                description: >-
                  <p>Disassociates a member account from an Amazon Inspector
                  delegated administrator.</p>
                tags:
                  - Disassociate
                  - Members
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
            /enable:
              POST:
                summary: Enable
                description: >-
                  <p>Enables Amazon Inspector scans for one or more Amazon Web
                  Services accounts.</p>
                tags:
                  - Enable
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
            /delegatedadminaccounts/enable:
              POST:
                summary: EnableDelegatedAdminAccount
                description: >-
                  <p>Enables the Amazon Inspector delegated administrator for
                  your Organizations organization.</p>
                tags:
                  - Enable
                  - Delegated
                  - Administrative
                  - Account
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
            /cis/scan/report/get:
              POST:
                summary: GetCisScanReport
                description: <p>Retrieves a CIS scan report.</p>
                tags:
                  - Get
                  - ~~
                  - Scans
                  - Reports
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
            /cis/scan-result/details/get:
              POST:
                summary: GetCisScanResultDetails
                description: <p>Retrieves CIS scan result details.</p>
                tags:
                  - Get
                  - ~~
                  - Scans
                  - Results
                  - Details
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
            /configuration/get:
              POST:
                summary: GetConfiguration
                description: <p>Retrieves setting configurations for Inspector scans.</p>
                tags:
                  - Get
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
            /delegatedadminaccounts/get:
              POST:
                summary: GetDelegatedAdminAccount
                description: >-
                  <p>Retrieves information about the Amazon Inspector delegated
                  administrator for your organization.</p>
                tags:
                  - Get
                  - Delegated
                  - Administrative
                  - Account
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
            /ec2deepinspectionconfiguration/get:
              POST:
                summary: GetEc2DeepInspectionConfiguration
                description: >-
                  <p>Retrieves the activation status of Amazon Inspector deep
                  inspection and custom paths associated with your account. </p>
                tags:
                  - Get
                  - EC2
                  - Deep
                  - Inspections
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
            /encryptionkey/get:
              GET:
                summary: GetEncryptionKey
                description: <p>Gets an encryption key.</p>
                tags:
                  - Get
                  - Encryption
                  - Keys
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /reporting/status/get:
              POST:
                summary: GetFindingsReportStatus
                description: <p>Gets the status of a findings report.</p>
                tags:
                  - Get
                  - Findings
                  - Reports
                  - Status
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /members/get:
              POST:
                summary: GetMember
                description: <p>Gets member information for your organization.</p>
                tags:
                  - Get
                  - Members
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /sbomexport/get:
              POST:
                summary: GetSbomExport
                description: >-
                  <p>Gets details of a software bill of materials (SBOM)
                  report.</p>
                tags:
                  - Get
                  - Sbom
                  - Export
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
            /accountpermissions/list:
              POST:
                summary: ListAccountPermissions
                description: >-
                  <p>Lists the permissions an account has to configure Amazon
                  Inspector.</p>
                tags:
                  - Lists
                  - Account
                  - Permissions
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
            /cis/scan-configuration/list:
              POST:
                summary: ListCisScanConfigurations
                description: <p>Lists CIS scan configurations.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
            /cis/scan-result/check/list:
              POST:
                summary: ListCisScanResultsAggregatedByChecks
                description: <p>Lists scan results aggregated by checks.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Results
                  - Aggregated
                  - By
                  - Checks
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
            /cis/scan-result/resource/list:
              POST:
                summary: ListCisScanResultsAggregatedByTargetResource
                description: <p>Lists scan results aggregated by a target resource.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Results
                  - Aggregated
                  - By
                  - Target
                  - Resources
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
            /cis/scan/list:
              POST:
                summary: ListCisScans
                description: <p>Returns a CIS scan list.</p>
                tags:
                  - Lists
                  - ~~
                  - Scans
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
            /coverage/list:
              POST:
                summary: ListCoverage
                description: <p>Lists coverage details for you environment.</p>
                tags:
                  - Lists
                  - Coverage
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
            /coverage/statistics/list:
              POST:
                summary: ListCoverageStatistics
                description: >-
                  <p>Lists Amazon Inspector coverage statistics for your
                  environment.</p>
                tags:
                  - Lists
                  - Coverage
                  - Statistics
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
            /delegatedadminaccounts/list:
              POST:
                summary: ListDelegatedAdminAccounts
                description: >-
                  <p>Lists information about the Amazon Inspector delegated
                  administrator of your organization.</p>
                tags:
                  - Lists
                  - Delegated
                  - Administrative
                  - Accounts
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
            /filters/list:
              POST:
                summary: ListFilters
                description: <p>Lists the filters associated with your account.</p>
                tags:
                  - Lists
                  - Filters
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
            /findings/aggregation/list:
              POST:
                summary: ListFindingAggregations
                description: >-
                  <p>Lists aggregated finding data for your environment based on
                  specific criteria.</p>
                tags:
                  - Lists
                  - Findings
                  - Aggregations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
            /findings/list:
              POST:
                summary: ListFindings
                description: <p>Lists findings for your environment.</p>
                tags:
                  - Lists
                  - Findings
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
            /members/list:
              POST:
                summary: ListMembers
                description: >-
                  <p>List members associated with the Amazon Inspector delegated
                  administrator for your organization.</p>
                tags:
                  - Lists
                  - Members
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
            /usage/list:
              POST:
                summary: ListUsageTotals
                description: >-
                  <p>Lists the Amazon Inspector usage totals over the last 30
                  days.</p>
                tags:
                  - Lists
                  - Usage
                  - Totals
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
            /encryptionkey/reset:
              PUT:
                summary: ResetEncryptionKey
                description: >-
                  <p>Resets an encryption key. After the key is reset your
                  resources will be encrypted by an Amazon Web Services owned
                  key.</p>
                tags:
                  - Reset
                  - Encryption
                  - Keys
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
            /vulnerabilities/search:
              POST:
                summary: SearchVulnerabilities
                description: >-
                  <p>Lists Amazon Inspector coverage details for a specific
                  vulnerability.</p>
                tags:
                  - Search
                  - Vulnerabilities
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
            /cissession/health/send:
              PUT:
                summary: SendCisSessionHealth
                description: >-
                  <p> Sends a CIS session health. This API is used by the Amazon
                  Inspector SSM plugin to communicate with the Amazon Inspector
                  service. The Amazon Inspector SSM plugin calls this API to
                  start a CIS scan session for the scan ID supplied by the
                  service. </p>
                tags:
                  - Send
                  - ~~
                  - Sessions
                  - Health
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
            /cissession/telemetry/send:
              PUT:
                summary: SendCisSessionTelemetry
                description: >-
                  <p> Sends a CIS session telemetry. This API is used by the
                  Amazon Inspector SSM plugin to communicate with the Amazon
                  Inspector service. The Amazon Inspector SSM plugin calls this
                  API to start a CIS scan session for the scan ID supplied by
                  the service. </p>
                tags:
                  - Send
                  - ~~
                  - Sessions
                  - Telemetry
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
            /cissession/start:
              PUT:
                summary: StartCisSession
                description: >-
                  <p> Starts a CIS session. This API is used by the Amazon
                  Inspector SSM plugin to communicate with the Amazon Inspector
                  service. The Amazon Inspector SSM plugin calls this API to
                  start a CIS scan session for the scan ID supplied by the
                  service. </p>
                tags:
                  - Start
                  - ~~
                  - Sessions
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
            /cissession/stop:
              PUT:
                summary: StopCisSession
                description: >-
                  <p> Stops a CIS session. This API is used by the Amazon
                  Inspector SSM plugin to communicate with the Amazon Inspector
                  service. The Amazon Inspector SSM plugin calls this API to
                  start a CIS scan session for the scan ID supplied by the
                  service. </p>
                tags:
                  - Stop
                  - ~~
                  - Sessions
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /cis/scan-configuration/update:
              POST:
                summary: UpdateCisScanConfiguration
                description: <p>Updates a CIS scan configuration.</p>
                tags:
                  - Update
                  - ~~
                  - Scans
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /configuration/update:
              POST:
                summary: UpdateConfiguration
                description: >-
                  <p>Updates setting configurations for your Amazon Inspector
                  account. When you use this API as an Amazon Inspector
                  delegated administrator this updates the setting for all
                  accounts you manage. Member accounts in an organization cannot
                  update this setting.</p>
                tags:
                  - Update
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /ec2deepinspectionconfiguration/update:
              POST:
                summary: UpdateEc2DeepInspectionConfiguration
                description: >-
                  <p>Activates, deactivates Amazon Inspector deep inspection, or
                  updates custom paths for your account. </p>
                tags:
                  - Update
                  - EC2
                  - Deep
                  - Inspections
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /encryptionkey/update:
              PUT:
                summary: UpdateEncryptionKey
                description: >-
                  <p>Updates an encryption key. A
                  <code>ResourceNotFoundException</code> means that an Amazon
                  Web Services owned key is being used for encryption.</p>
                tags:
                  - Update
                  - Encryption
                  - Keys
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /filters/update:
              POST:
                summary: UpdateFilter
                description: >-
                  <p>Specifies the action that is to be applied to the findings
                  that match the filter.</p>
                tags:
                  - Update
                  - Filter
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
            /ec2deepinspectionconfiguration/org/update:
              POST:
                summary: UpdateOrgEc2DeepInspectionConfiguration
                description: >-
                  <p>Updates the Amazon Inspector deep inspection custom paths
                  for your organization. You must be an Amazon Inspector
                  delegated administrator to use this API.</p>
                tags:
                  - Update
                  - Organizations
                  - EC2
                  - Deep
                  - Inspections
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
                  - Organizations
            /organizationconfiguration/update:
              POST:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the configurations for your Amazon Inspector
                  organiz
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Members
                  - Associate
                  - Status
                  - Batches
                  - Get
                  - Code Snippets
                  - Batches
                  - Findings
                  - Details
                  - Free Trials
                  - EC2 Deep Inspection Status
                  - Members
                  - Update
                  - Reporting
                  - Cancel
                  - Sbomexport
                  - ~~
                  - Scans
                  - Configurations
                  - Create
                  - Filters
                  - Delete
                  - Organization Configurations
                  - Describe
                  - Disable
                  - Delegated Administrative Accounts
                  - Disassociate
                  - Enable
                  - Reports
                  - Results
                  - EC2 Deep Inspection Configurations
                  - Encryption Key
                  - Account Permissions
                  - Lists
                  - Checks
                  - Resources
                  - Coverage
                  - Statistics
                  - Aggregation
                  - ARN
                  - Usage
                  - Reset
                  - Vulnerabilities
                  - Search
                  - Cissession
                  - Health
                  - Send
                  - Telemetry
                  - Start
                  - Stop
                  - O
    overlays:
      - type: APIs.io Search
        url: overlays/inspector2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/inspector2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:inspector2
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---