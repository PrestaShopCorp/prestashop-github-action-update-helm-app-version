# README for 'Update Helm App Version' GitHub Action

## Description

<!-- AUTO-DOC-DESCRIPTION:START - Do not remove or modify this section -->

Updates the app version in the specified Helm values file and pushes the change.

<!-- AUTO-DOC-DESCRIPTION:END -->

The GitHub Action 'Update Helm App Version' is designed to automatically update the version of an application in a Helm values file and commit/push the change to the repository. This is typically used in CI/CD pipelines to update GitOps repositories with new image tags.

## Features

- **Automated Version Update**: Updates the `tag` field in the specified Helm values file.
- **GitOps Friendly**: Commits and pushes the change back to the repository.
- **Robustness**: Includes retries for push operations to handle concurrent updates.
- **Path Resolution**: Automatically constructs the file path based on app name and environment.

## Inputs

<!-- AUTO-DOC-INPUT:START - Do not remove or modify this section -->

|                               INPUT                               |  TYPE  | REQUIRED | DEFAULT |                             DESCRIPTION                             |
|-------------------------------------------------------------------|--------|----------|---------|---------------------------------------------------------------------|
|     <a name="input_app_name"></a>[app_name](#input_app_name)      | string |   true   |         |     The name of the application <br>(e.g., krew-test-app-api)       |
| <a name="input_environment"></a>[environment](#input_environment) | string |   true   |         | The environment to update (e.g., integration-sandbox, integration)  |
|       <a name="input_version"></a>[version](#input_version)       | string |   true   |         |                         The new version tag                         |

<!-- AUTO-DOC-INPUT:END -->
