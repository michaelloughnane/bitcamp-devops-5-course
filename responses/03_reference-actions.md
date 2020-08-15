## Finishing the workflow

@{{user.login}} you're doing great so far 😄! You've had to do a lot of workflow set up so we can begin writing custom actions. We have just one more thing to add to our `my-workflow.yml` file before we get to the action side of things.

#### Recap

Before we make our final workflow change let's do a quick recap about what we've done.

| Action                                                            | Key Takeaways                                                                                                                                                                                                                                          |
| ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Created `my-workflow.yml` inside of `.github/workflows` directory | GitHub repositories look in the `.github/workflows` folder for workflow files.                                                                                                                                                                         |
| Used a templated workflow                                         | GitHub provides many templates for workflow files. This is a great spot to look when setting up a new workflow. If you can't find what you are looking for, you can always click the `setup a workflow yourself` button for a minimal starter template |
| Workflow environment                                              | You learned, from a high level, how a repository uses a workflow file to run commands or actions based on triggers. You also learned that where these commands or actions execute is something that can be specified                                   |
| Workflow syntax                                                   | You were briefly introduced to the workflow YAML syntax.                                                                                                                                                                                               |

If that seems like a lot of things just to get started... well, it is! GitHub Actions is a robust platform designed to automate a wide range of tasks for your repositories.

If you'd like to see more examples of workflows and actions then check out these Learning Lab courses all about GitHub Actions:

- [GitHub Actions: Continuous Integration](https://lab.github.com/githubtraining/github-actions:-continuous-integration)
- [GitHub Actions: Continuous Delivery](https://lab.github.com/githubtraining/github-actions:-continuous-delivery)
- [GitHub Actions: Publish to GitHub Packages](https://lab.github.com/githubtraining/github-actions:-publish-to-github-packages)

## Add an action reference to the workflow

### :keyboard: Activity: Reference our custom action from `my-workflow.yml`

1. [Edit]({{workflowFile}}) the `my-workflow.yml` to have the following contents:

   ```yaml
   name: Docker Actions

   on: [push]

   jobs:
     action:
       runs-on: ubuntu-latest

       steps:
         - uses: actions/checkout@v1

         - name: hello-action
           uses: ./.github/actions/hello-world
   ```

1. Commit these file changes to this branch

---

I'll respond when you push changes to this pull request.
