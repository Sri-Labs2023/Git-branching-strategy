# Git submodules
~~~
Git submodules allow you to keep a Git repository as a subdirectory of another Git repository. 
Git submodules are simply a reference to another repository at a particular snapshot in time. 
Git submodules enable a Git repository to incorporate and track version history of external code.
~~~
# What is a Git submodule?

Often a code repository will depend upon external code. This external code can be incorporated in a few different ways. The external code can be directly copied and pasted into the main repository. This method has the downside of losing any upstream changes to the external repository. Another method of incorporating external code is through the use of a language's package management system like Ruby Gems or NPM. This method has the downside of requiring installation and version management at all places the origin code is deployed. Both of these suggested incorporation methods do not enable tracking edits and changes to the external repository.

A Git submodule is a record within a host Git repository that points to a specific commit in another external repository. Submodules are very static and only track specific commits. Submodules do not track Git refs or branches and are not automatically updated when the host repository is updated. When adding a submodule to a repository a new .gitmodules file will be created. The .gitmodules file contains meta data about the mapping between the submodule project's URL and local directory. If the host repository has multiple submodules, the .gitmodules file will have an entry  for each submodule.

# When should you use a Git submodule?

If you need to maintain a strict version management over your external dependencies,  

it can make sense to use Git submodules. The following are a few best use cases for Git submodules.

~~~
- When an external component or subproject is changing too fast or upcoming changes will break the API,
you can lock the code to a specific commit for your own safety.

- When you have a component that isn’t updated very often and you want to track it as a vendor dependency.

- When you are delegating a piece of the project to a third party and you want to integrate their work at a specific time or release.
Again this works when updates are not too frequent.
~~~


# Common commands for Git submodules

https://www.atlassian.com/git/tutorials/git-submodule
https://medium.com/@porteneuve/mastering-git-submodules-34c65e940407

# Conclusion

Git submodules are a powerful way to leverage Git as an external dependency management tool. 
Weigh the pros and cons of Git submodules before using them, as they are an advanced feature and may take a learning curve for team members to adopt.
