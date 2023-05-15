Source: [Stop Using Branches for Deploying to Different GitOps Environments | Codefresh](https://codefresh.io/blog/stop-using-branches-deploying-different-gitops-environments/)

## Summary and take aways
The blog post takes aim at environments and not application source code. The origial [[GitFlow]] approach that was the foundation of this approach is mainly aimed at the latter.
Main argument boils down to the potential of unwanted consequences due to temptation for change in upstream and the very limited scaling potential of such a solution.

The follow-up part of this blog series is found here [[How to model gitops environments and releases]]

## What not to do

We should avoid using Git branches for different environments. The main reasons for this is according to the author ():

1. Using different Git branches for deployment environments is a legacy of the past.
2. Pull requests and merges between different branches becomes problematic.
3. Temptation to include environment specific code and create **configuration drift.**
4. Maintenance of all the environments quickly get out of hand
5. Branch per environment goes against the existing Kubernetes ecosystem.

### Apply only for legacy systems
As with everything, if it is working and people are comfortable with the methods being used and changing things will cause breaking, then keep using it. Otherwise as noted here: [[GitFlow#^b65369]] one of the authors of this approach is now warning against using it.

The GitFlow model is focused on application source control, not the infrastructure as code part. Refer to note on [[GitFlow]] for more information on pros and cons of that approach in general.

In the context of GitOps, source code for application and the configuration for environments should be kept separate. This allows both parts to be handled independently and we can chose which strategies best fit our different needs.

### Difficulty of pull requests and merges between branches

The theory of a promotion being a simple git merge away is not true. The reason for this is the potential for large merge conflicts, unwanted changes as part of the merges and that changes might happen in the wrong order.

Just remembering which changes to take from one environment into the next and then taking just those changes is a task with many potential pit falls. Having to rely on manual routines or tools such as *git cherry picking* is far from ideal.
Even in cases where we are aware of which changes should be brought over to the next branch, we are not necessarily on top of the order of promotion compared to the order of committing. In Kubernetes there are certain items that need to be in place before others, such as config maps, secrets that must be in place before a deployment etc.

### Configuration drift

In theory this should not be an issue. Making a change in test or staging and merging that into production should result in all the changes being transferred to the new environment.
The issue arise due to merging only happening in one direction and the potential temptation for maintainers to make changes in upstream branches without then backporting these.

Hot fixing in production and then forgetting to apply the same fix in the lower environments then causes an issue the next time we are promoting a branch not containing the hotfix upstream. 

### Maintenance

Managing a different branches for a large number of environments is a losing battle. For a 3 environment setup it is complicated, but not impossible. When you start having additional environments such as load testing, integration testing, staging etc. All the previous problems start to multiply and we will quickly find ourself in a bog of configuration conflicts etc.

### Against existing Kubernetes ecosystem

Use Helm or Kustomize (Or just [[ArgoCD]]?) to keep track of it all. As these are the de-facto standard methods of administering the infrastructure when it comes to Kubernetes.





Tags: #github #branching #cicd #gitops #git #kubernetes 