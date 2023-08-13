https://git-scm.com/book/en/v2/Git-Tools-Submodules
https://www.atlassian.com/git/tutorials/git-submodule
https://beta.cloudcraft.info/huong-dan-dung-tinh-nang-submodule-cua-git/

A git submodule is a record within a host git repository that points to a specific commit in another external repository. Submodules are very static and only track specific commits. Submodules do not track git refs or branches and are not automatically updated when the host repository is updated. When adding a submodule to a repository a new .gitmodules file will be created. The .gitmodules file contains meta data about the mapping between the submodule project's URL and local directory. If the host repository has multiple submodules, the .gitmodules file will have an entry  for each submodule.

If you need to maintain a strict version management over your external dependencies,  it can make sense to use git submodules. The following are a few best use cases for git submodules.

- When an external component or subproject is changing too fast or upcoming changes will break the API, you can lock the code to a specific commit for your own safety.
- When you have a component that isn’t updated very often and you want to track it as a vendor dependency.
- When you are delegating a piece of the project to a third party and you want to integrate their work at a specific time or release. Again this works when updates are not too frequent.