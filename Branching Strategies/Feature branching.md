In addtion to the main branch (this is always present - as in [[Trunk based development]]) but we create a new branch for each hot fix and each new feature.
Feature branches should be as small as possible and we create pull requests to have the feature branch merged into main.

1. One branch per feature
2. Short delivery
3. Pull request is reviewed and automated testing
4. Continuous delivery
5. Feature toggles are not necissary, but a nice to have features.
6. Low level of complexity when the branching strategy is isolated from the other tasks.


Feature branching is a popular Git branching strategy that involves creating separate branches for individual features or tasks, and later merging them back into the main branch upon completion. This approach can be especially useful for small teams, as it allows developers to work independently on their assigned tasks without affecting the main branch. However, like any strategy, feature branching has its pros and cons.

In general Feature branching is a *general branching strategy that does not take a stance on deployment flow.*


**Pros:**

1.  Isolation: Feature branches provide a safe and isolated environment for developers to work on their tasks without interfering with others' work or the stability of the main branch.
2.  Code review: When using feature branches, developers can submit pull requests to merge their changes back into the main branch. This allows for easy code reviews, enabling team members to provide feedback and maintain code quality.
3.  Collaboration: If multiple developers need to work on the same feature, they can collaborate within the same feature branch without affecting others.
4.  Continuous integration compatibility: Feature branching works well with continuous integration (CI) systems, as each branch can be built and tested independently, allowing issues to be identified and resolved before merging the changes into the main branch.
5.  Version control: Feature branches make it easier to track and manage the development history of individual features, making it simpler to revert or cherry-pick specific changes if needed.
    

**Cons:**

1.  Merge conflicts: If feature branches are not kept up-to-date with the main branch, there is a higher likelihood of merge conflicts arising when it's time to merge the changes back in. This can be mitigated by frequently rebasing or merging the main branch into the feature branch.
2.  Integration challenges: If features are developed in isolation, integration issues may not be discovered until the branches are merged back into the main branch. To minimize such issues, regular merging or rebasing, as well as continuous integration, can help ensure that features remain compatible with the main branch.
3.  Overhead: Feature branching requires developers to manage multiple branches and ensure that they are up-to-date with the main branch. This can increase overhead and complexity, especially if there are numerous active branches.
4.  Long-lived branches: If a feature branch takes a long time to complete, it may become increasingly difficult to merge back into the main branch due to significant changes and divergent code. It's essential to keep feature branches short-lived and focused on specific tasks to minimize this issue.
5.  Incomplete features: If a feature branch is merged into the main branch before it's fully completed, it can introduce bugs or incomplete functionality. This can be mitigated by adhering to a strict definition of "done" and ensuring that all features are thoroughly tested before merging.

In summary, feature branching can be an effective Git branching strategy for small teams, as it provides an isolated environment for developers to work on individual tasks. However, it's essential to be aware of potential issues like merge conflicts and integration challenges, and address them proactively by keeping branches up-to-date and leveraging continuous integration tools.


