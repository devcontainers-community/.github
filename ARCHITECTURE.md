There's a few big projects going on under @devcontainers-community:

- The big [devcontainers-community/features] project and the associated
  polyrepos
- The [devcontainers-community/templates] project and associated polyrepos
- The [devcontainers-community/npm-features] monorepo project for
  `npm install`-able tools
- The [devcontainers-community/pip-features] monorepo project for
  `pip install`-able tools
- The various GitHub Action tools

**Why some polyrepos and some monorepos?**

Because sometimes it's best to isolate components and sometimes it's best to
consolidate them. In the case of the vastly different features and associated
maintainer knowledge of sometime like a CMake feature vs a Wasmer feature it's
helpful to allow those groups to work independently of each other more than a
monorepo allows. In reverse, it's helpful for npm-interested people to have all
npm-related features under a single roof since it's all within the JavaScript
ecosystem. Same for the Python pip features.

**Why aren't some of these projects official?**

I don't know. Some of them haven't been formally asked to merge to
[@devcontainers] official, while others are just outside the scope of the
official specification maintainers. For instance, it's highly unlikely that
[@devcontainers] would take on the [devcontainers-community/pip-features]
project as official, but they _might_ take on some of the popular GitHub
Actions. Open a Discussion and chat with them; they seem cool 😎 and won't bite!
😉

**How do the polyrepos merge into the big [devcontainers-community/features]
package namespace?**

This is a trick where packages like `ghcr.io/devcontainers-community/features/*`
images can be published **from other repositories, not just
[devcontainers-community/features]**. This is what lets us have the source code
in [devcontainers-community/features-dart-sdk] and publish the feature to
`ghcr.io/devcontainers-community/features/dart-sdk`. We don't even need a custo
GitHub token to do it!

<!-- TODO: Move some of that 👆 into each relevant repository "Development" section? -->

<!-- prettier-ignore-start -->
[devcontainers-community/features]: https://github.com/devcontainers-community/features
[devcontainers-community/npm-features]: https://github.com/devcontainers-community/npm-features
[devcontainers-community/pip-features]: https://github.com/devcontainers-community/pip-features
[devcontainers-community/templates]: https://github.com/devcontainers-community/templates
[devcontainers-community/features-dart-sdk]: https://github.com/devcontainers-community/features-dart-sdk
[@devcontainers]: https://github.com/devcontainers
<!-- prettier-ignore-end -->
