# gemoc-studio-jenkins
This repository contains the jenkins configuration file working on forked repositories.

This file is used to drive the builds done on the GEMOC initiative's Continuous integration server.

Basically, it provides a Jenkinsfile that allows to configure a CI to uses the forked repositories of the GEMOC initiative instead of the eclipse official ones.

It helps prepare and validate branches suitable for creating Pull Request as external contributor (see https://github.com/eclipse/gemoc-studio/wiki/External-contributor-memo


# How to use

- create a branch for your feature in the repositories (gemoc/gemoc-studio and/or gemoc/gemoc-studio-modeldebugging). 
- create a branch in this repositoy (ie. gemoc/gemoc-studio-jenkins) with the same name. After some delay (5 min max), the CI will discover your new branch and create a new job for it here: https://ci.inria.fr/gemoc/job/gemoc-studio-eclipsefork/
- from time to time do not forget to fetch and merge the content from the official repositories into the forks and your branches (see the [contributor memo](https://github.com/eclipse/gemoc-studio/wiki/External-contributor-memo)).

You can then test and propose your branch as a pull request in the corresponding eclipse repositories. Once accepted you should consider removing the branch in order to save disk space on the CI.


# Advanced use
With some understanding of jenkins pipeline, in a specific branch, you can also use it to integrate more repositories than the forked ones.
