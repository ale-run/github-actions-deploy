# Ale Github Actions - Deploy

this action deploys the source code to Ale.


## Inputs

## `endpoint`

**Required** Ale API Endpoint

## `token`

**Required** Ale API Key

## `project`

**Required** A GitHub Personal Access Token with read/write permissions for managing Deploy Keys.

## `stage`

Name of the stage to deploy. default: the stage set as default stage

## `allStages`

Boolean / if true, deploy to all stages

#### One of the following inputs is required.

## `file`

Deployment configuration yaml file path

## `json`

Deployment configuration JSON string

## `yaml`

Deployment configuration yaml string

---

## Usage Examples
```yaml
uses: ale-run/github-actions-deploy@v1
with:
  endpoint: ${{ secrets.ALE_ENDPOINT }}
  token: ${{ secrets.ALE_TOKEN }}
  project: myproject
  stage: main
  file: ./examples/myservice.yml
```