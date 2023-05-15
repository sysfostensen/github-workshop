
Unlike feature branches, release branches are longer lasting than the features. There are a branch per release and there might be different teams for each branch.
Typically there will be additional branches for each hot fix, and these are again are merged into the other branches. Creates a need for administration to ensure that 
all the open branches need to receive the same hotfix through pull requests etc.

1. One branch per release
2. Typicall for low frequency deployments
3. "Waterfall" release schedule.
4. Merge conflicts
5. No continuous integrations, large overhead administration wise.
6. Only use if you are a software vendor that need to support multiple versions.
7. Might need a dedicated person/team to validate and administer the branches.


Sources: [DevOps Toolkit](https://youtu.be/U_IFGpJDbeU?t=504)

Tags: #github #branching #cicd 