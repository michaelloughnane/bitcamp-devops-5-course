## Digging into a step

As I mentioned earlier, a step is a task that is either an action or a command. This can be slightly confusing, so I want to take a little time to ensure I explain it to you before moving on.

#### Actions

Actions are powerful. They are small programs written in either JavaScript or running inside of Docker containers, that add some functionality to your repository.

The things you can do with actions are limited only by your imagination. Want to send a tweet every time you tag a release? What about ordering 🍕just by creating an issue?

Let's not forget the more practical usage of actions, testing the source code of a repository or letting your team know that you are out of office 🏝 when they @ mention your name in issues or pull requests.

You can define an action's inputs, outputs, and environment variables to create reusable building blocks for your workflow.

Actions are portable. You are free to publish your actions to the [Actions Marketplace](https://github.com/marketplace?type=actions) where others can use your creation in their workflows! You can also share actions without publishing them to the marketplace by referencing the repository that contains the actions code!

Actions can even run commands 😏

📖Learn more [About Actions](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/about-actions)

#### Commands

Commands are useful in the own respect, but are much more limited than actions.

Think about the tasks you might do from the command line of your local machine. Maybe you run `npm install` to install all of the dependencies for your project before running your unit tests. Maybe you run `docker build` to execute a Dockerfile.

You can accomplish the same set of tasks inside of a workflow but using `run` as a step in your job.

Commands are not easily shareable. There is no central location where you can consume the popular commands used in workflows. You do not have access to fine tuning the inputs, outputs or environment variables.

This does not mean commands offer no value in a workflow, but you should use them wisely and if you find yourself reusing the same commands repeatedly, consider turning them into actions.

---

<details><summary>Has Learning Lab stopped responding?  Your Actions workflow might be failing. Click here for troubleshooting help.</summary>

When a GitHub Actions workflow is running, you should see some checks in progress, like the screenshot below.

![Checks in progress box](https://i.imgur.com/uO6iqYd.png)

If the checks don't appear or if the checks are stuck in progress, there's a few things you can do to try and trigger them:

- Refresh the page, it's possible the workflow ran and the page just hasn't been updated with that change
- Try making a commit on this branch. Our workflow is triggered with a `push` event, and committing to this branch will result in a new `push`
- Edit the workflow file on GitHub and ensure there are no red lines indicating a syntax problem
  </details>
