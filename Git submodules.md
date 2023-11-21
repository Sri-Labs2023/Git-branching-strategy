# Git submodules
~~~
Git submodules allow you to keep a Git repository as a subdirectory of another Git repository. 
Git submodules are simply a reference to another repository at a particular snapshot in time. 
Git submodules enable a Git repository to incorporate and track version history of external code.
~~~
# What is a Git submodule?

Often a code repository will depend upon external code. This external code can be incorporated in a few different ways. The external code can be directly copied and pasted into the main repository. This method has the downside of losing any upstream changes to the external repository. Another method of incorporating external code is through the use of a language's package management system like Ruby Gems or NPM. This method has the downside of requiring installation and version management at all places the origin code is deployed. Both of these suggested incorporation methods do not enable tracking edits and changes to the external repository.

A Git submodule is a record within a host Git repository that points to a specific commit in another external repository. Submodules are very static and only track specific commits. Submodules do not track Git refs or branches and are not automatically updated when the host repository is updated. When adding a submodule to a repository a new .gitmodules file will be created. The .gitmodules file contains meta data about the mapping between the submodule project's URL and local directory. If the host repository has multiple submodules, the .gitmodules file will have an entry  for each submodule.
