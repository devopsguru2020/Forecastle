# Forecastle

[![Get started with Stakater](https://stakater.github.io/README/stakater-github-banner.png)](http://stakater.com/?utm_source=IngressMonitorController&utm_medium=github)

## Why name Forecastle?

Forecastle is the section of the upper deck of a ship located at the bow forward of the foremast. This Forecastle will act as a control panel and show all your running applications.

## Problem

We would like to have a central place where we can easily look for and use our applications running in a cluster.

## Solution

Forecastle gives you access to a control panel where you can see your running applications and access them.

## Configuration

Forecastle looks for a specific annotations on ingresses.

- Add the following annotations to your ingresses in order to be used by forecastle:

|           Annotation           |                                           Description                                           |
|:------------------------------:|:-----------------------------------------------------------------------------------------------:|
| `forecastle.stakater.com/expose` | **[Required]** Add this with value `true` to the ingress of the app you want to show in Forecastle  |
| `forecastle.stakater.com/icon`   | **[Optional]** Icon/Image URL of the application                                                    |

- Once you have added these annotations, you need to specify namespaces to look for the ingresses in configmap of Forecastle. Modify the `namespaces.conf` key with a comma separated list of namespaces, in the manifest file.

## Deploying to Kubernetes

### Vanilla Manifests

You can apply vanilla manifests by running the following command:

```bash
kubecl apply -f https://raw.githubusercontent.com/stakater/Forecastle/master/deployments/kubernetes/forecastle.yaml
```

### Helm Charts

If you configured `helm` on your cluster, you can deploy Forecastle via helm chart located under `deployments/kubernetes/chart/Forecastle` folder.

## Help

**Got a question?**
File a GitHub [issue](https://github.com/stakater/Forecastle/issues), or send us an [email](mailto:stakater@gmail.com).

### Talk to us on Slack
Join and talk to us on the #tools-imc channel for discussing Forecastle

[![Join Slack](https://stakater.github.io/README/stakater-join-slack-btn.png)](https://stakater-slack.herokuapp.com/)
[![Chat](https://stakater.github.io/README/stakater-chat-btn.png)](https://stakater.slack.com/messages/CAN960CTG/)

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/stakater/Forecastle/issues) to report any bugs or file feature requests.

### Developing

PRs are welcome. In general, we follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

## Changelog

View our closed [Pull Requests](https://github.com/stakater/Forecastle/pulls?q=is%3Apr+is%3Aclosed).

## License

Apache2 © [Stakater](http://stakater.com)

## About

`Forecastle` is maintained by [Stakater][website]. Like it? Please let us know at <hello@stakater.com>

See [our other projects][community]
or contact us in case of professional services and queries on <hello@stakater.com>

  [website]: http://stakater.com/
  [community]: https://github.com/stakater/
