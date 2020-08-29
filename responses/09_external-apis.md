## Fetch from an external API

The next action we write is going to reach out to an external API and fetch data for consumption. Although your action is bound to a step, which is bound to a workflow within your repository it is NOT bound to an isolated network. This means that we can leverage APIs from our favorite cloud providers, favorite pizza shops, social media or whatever API our developers need.

You learned what an API is last lesson, so we'll skip that explanation this time 😂.

### How does that apply to our next action?

We are now going to write an action that reaches out to a service through its REST API to get us a random cat fact. We will then display that fact on the [Actions tab]({{actionsUrl}}).

For our purposes the API we use will not require authentication, however that is a limitation of the course content and not the GitHub Actions platform. If you need to store secrets, like API keys, for your workflow to use you will need to configure [secrets](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/creating-and-using-encrypted-secrets) as inputs.

What are we waiting for, let's get started! 😉
