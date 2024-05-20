# GitHub Actions - Issue

Create a new issue using a github-actions user as the author. These will be created on the account/repo that called the action.

## Usage

**workflow.yml**
```yml
permissions: {}

jobs:
  createissue:
    # ...
    permissions:
      issue: write
    steps:
      - name: Create issue
        uses: silverstripe/gha-issue@v1
        with:
          title: My issue title
          description: |
            This text will appear in the body of the GitHub issue\n
            \n
            You can add line breaks\n
            \n
            ## My heading\n
            - Markdown is supported\n
```

## Inputs:

### Title
The title of the issue to create. Required.
`title: Title of my issue`

### Description
The description of the issue to create. Required.
`description: Main body of the issue goes here`

### Close existing
Whether to close any existing open issues with the same title that were created by the "github-actions[bot]" user. Default is false, enable with:
`close_existing: true`
