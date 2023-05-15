## Main differences between GitHub Flow and Trunk Based Development:

1.  Branch lifetimes:
    -   In GitHub Flow, branches are created for each feature, bugfix, or change, and can live longer depending on the time taken to develop and review the changes.
    -   In TBD, branches are typically short-lived, and developers are encouraged to commit their changes directly to the trunk or to use feature branches that are merged back quickly (usually within a day or two).
2.  Code reviews:
    -   In GitHub Flow, code reviews are an integral part of the process. Pull requests are opened for each change, allowing team members to review and collaborate before merging the changes into the main branch.
    -   In TBD, code reviews can be less formal or optional, depending on the team's practices. Some teams may use pre-commit reviews or rely on post-commit reviews to ensure code quality.
3.  Deployment and integration:
    -   GitHub Flow emphasizes continuous integration and deployment, with changes being deployed to production or staging environments after merging into the main branch.
    -   In TBD, continuous integration is also promoted, but the focus is on keeping the mainline branch stable and ready for deployment at any time. This might involve practices like feature toggles or branch by abstraction to hide incomplete features until they are ready for release.
4.  Simplicity and structure:
    -   GitHub Flow provides a simple and straightforward workflow, suitable for small to medium-sized teams.
    -   Trunk Based Development, while also relatively simple, might require more discipline and additional practices (e.g., feature toggles) to maintain the stability of the mainline branch.


## Main notes dealing with the subject
[[Trunk based development]]
[[Github Flow]]



#git #github-flow #git-trunk #branching 