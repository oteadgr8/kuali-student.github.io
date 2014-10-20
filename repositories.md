---
layout: default
---

# Kuali Student Repositories

The full repository conversion is located here: [archived-from-svn](https://github.com/kuali-student/archived-from-svn)

Most of the other repositories are different sets of branches from this base, although some like the [git-workflow-maven-plugin](https://github.com/kuali-student/git-workflow-maven-plugin) are not.

Below are more detailed descriptions of the contents of the different repositories.


## [ks-development](https://github.com/kuali-student/ks-development)

Holds **master** branch for continued KS develpoment.  Git doesn't work as well when you have thousands of branches so this repository holds the master branch seperate from the history of the project (this branch was extracted from the ks repository).  

### Note Regarding Impex

In order to reduce the size of the kuali student repository for storage in github the contents of the .MPX files were removed.

The **master** branch has been adjusted to contain the necessary refactoring to use the seperate **ks-development-impex** repository artifacts.

## [ks-development-impex](https://github.com/kuali-student/ks-development-impex)

For current KS development, this holds the .mpx files which were generated from a specific version of the ks-development repository branch.

## [ks](https://github.com/kuali-student/ks)

Contains the full set of *enrollment_* prefixed branch names.

**master** is the fused *enrollment_aggregate_trunk* branch.

The idea is that development work will be conducted on this fused branch in an isolated repository (for end user performance reasons) and then approved commits fed back into this repository.

## [cm-contribution](https://github.com/kuali-student/cm-contribution)

The **master** branch is the fused *contrib_CM_aggregate_trunk* branch which was based on the fused *enrollment_aggregate_branches_CM-2.0* branch.

After the CM 2.0 release this repository was used to hold institutional contributions back in a way more easily mergable into the mainline branch.

## [git-repository-tools](https://github.com/kuali-student/git-repository-tools)

The **master** branch contains the maven project used to perform the Kuali Student Subversion to Git Conversion.  Some of the artifacts are shared with the *fusion-maven-plugin* and the *git-workflow-maven-plugin*.

## [archived-from-svn](https://github.com/kuali-student/archived-from-svn)

The kuali-student subversion repository contained 77740 revisions between April 2008 and October 2014.

The [git-repository-tools](https://github.com/kuali-student/git-repository-tools) project was used to perform the conversion of the entire repository into a single git repository.  

Most of the other repositories contain a portion of the commit graph contained here.

### Key Alterations

1. To reduce the repository size all .MPX files were modified to remove their content.
2. Two large files were removed to reduce the repository size and pass the github requirement of no files being > 100 MB in size.
3. Commits changed in steps 1 and 2 were rewritted with updated *fusion-maven-plugin.dat* values to allow the fusion-maven-plugin to continue to work.

