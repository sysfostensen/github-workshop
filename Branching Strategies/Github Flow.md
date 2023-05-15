
Follows the agile principles and so it is a fast and streamlined branching strategy with short production cycles and frequent releases.
Does not use a development branch, instead all developers branch of the main branch to create the features they need and continuously merge their changes into the main branch, allowing for a lean approach.

**Main idea is to keep the main branch in a constant deployable state**

## The main components of GitHub Flow are:

1.  Create a branch: For each new task, create a new branch from the main or default branch (usually `master` or `main`).
2.  Add commits: Make changes to the code on the new branch and commit them.
3.  Open a pull request: Once the changes are ready for review, open a pull request to initiate discussions and request feedback.
4.  Discuss and review: Team members review the changes, provide feedback, and iterate on the code.
5.  Merge: Once the pull request is approved, merge the changes into the main branch.
6.  Deploy: After merging, deploy the changes to production or staging environments as needed.

## Downsides
The lack of branches to protect the main branch leads this approach to be more susceptible to bugs and can thus lead to unstable production code. This puts an increased focus on the need of testing before code is merged into the main branch and becomes a part of the release.

1.  Limited support for parallel releases: GitHub Flow may not be suitable for projects that require managing multiple parallel releases, as it doesn't enforce a strict branching hierarchy.
2.  Scalability: For larger teams or more complex projects, GitHub Flow might not provide enough structure or control over the development process.
3.  Lack of long-term release planning: It does not explicitly address long-term release planning or versioning, which might require additional processes or tools to manage.

## Strengths
Fast, easy to visualize and ideal for smaller teams. Ideal for maintaining a single production version.

1.  Simplicity: The GitHub Flow is simple to understand and easy to follow, making it suitable for small to medium-sized teams.
2.  Continuous integration: It promotes continuous integration and deployment, leading to faster releases and quicker feedback.
3.  Collaboration: The pull request system encourages collaboration and code review, improving code quality and team communication.

# Notes dealing with this subject
[[Git Patterns and anti-patterns#^dc1fa5]]

# GitLab Flow
Much the same as the GItHub flow approach, except that it creates a 3 branch approach, master is seen as the development branch. Master is branched into a pre production branch, which in turn is branched of into a production branch when the time is right.

## Advantage
We get a clear separation of different environments, we can develop directly on a master branch, create branches of that to have in one or more pre production environments. Once we are ready we create a new branch for the production environment.

**Suitable for when you dont control the timing of releases**.



Tags: #github #branching #cicd #github-flow #git 