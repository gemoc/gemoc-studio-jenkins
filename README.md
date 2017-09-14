# gemoc-studio-jenkins
contains the jenkins configuration to launch forked repositories.

This file is used to drive the builds done on the GEMOC initiative's Continuous integration server.

Basically, it provides a Jenkinsfile that allows to configure a CI to uses the forked repositories instead of the official ones.

It helps prepare and validate branches suitable for creating Pull Request.


# How to use

- create a branch for your feature in the repositories (gemoc/gemoc-studio and/or gemoc/gemoc-studio-modeldebugging). 
- create a branch in this repositoy (ie. gemoc/gemoc-studio-jenkins) with the same name. After some delay (5 min max), the CI will discover your new branch and create a new job for it here: https://ci.inria.fr/gemoc/job/gemoc-studio-eclipsefork/

You can then test and propose your branch as a pull request in the eclipse repositories. Once accepted you should consider removing the branch in order to save disk space on the CI.


# Advanced use
With some understanding of jenkins pipeline, in a specific branch, you can also use it to integrate more repositories than the forked ones.
