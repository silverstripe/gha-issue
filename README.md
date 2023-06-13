# GitHub Actions - Issue

Create a new issue using a github-actions user as the author. These will be created on the account/repo that called the action.

## Usage

**workflow.yml**
```yml
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
