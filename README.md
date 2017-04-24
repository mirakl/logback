### WARNING ###

This is a fork waiting for some PRs to be merged on origin and the new version released, it will be deleted after.

The repo is public, so don't put internal stuff in it, like urls etc.

# How to keep it up to date with upstream ?

When upstream is performing a mew release, we should strive to keep this fork up to date with our patches.
To do so, just follow these steps:
* update your local clone to fetch the latest commits on upstream
* checkout the tag you want to perform a release for as a new branch, e.g. for 1.2.3, execute `git checkout -b branch_v_1.2.3 v_1.2.3`
* if necessary get the branches from our forks
** git checkout -b obourgain-configure_logback_access_from_system_property master && git pull https://github.com/obourgain/logback.git configure_logback_access_from_system_property
** git checkout -b nmaupu-syslog-for-access master && git pull https://github.com/nmaupu/logback.git syslog-for-access
**
* cherry-pick the the commits we want to apply, here is a list of those at the time of writing:
** e7ffa44ea347ea43e18bf56a12443c2ef0a1445a Update readme
** 7a1b9d9bfdf50960ce446887a8d77ffb2545cbda Added the ability to log to syslog for access
** 6f4dbb97efce4c6e89fe5a167ba65e2d33cfa5f4 Configure logback-access from system property
* you do not need to update master

Then you can perform a release. The Mirakl release named must be the same as the source logback release, with a -mirakl qualifier.
You should create a tag named like the one of the source release, with -mirakl appended. E.g. for the version 1.2.3, the tag is v_1.2.3 so our release is v_1.2.3-mirakl

#About logback

Thank you for your interest in logback, the reliable, generic, fast
and flexible logging library for Java.

The Logback documentation can be found on the [project
web-site](https://logback.qos.ch/documentation.html) as well as under
the docs/ folder of the logback distribution.

#Building logback

Building logback is documented at:

  https://logback.qos.ch/setup.html#ide

#In case of problems

In case of problems please do not hesitate to post an e-mail message
on the logback-user@qos.ch mailing list.  However, please do not
directly e-mail logback developers. The answer to your question might
be useful to other users. Moreover, there are many knowledgeable users
on the logback-user mailing lists who can quickly answer your
questions.


#Pull requests

If you are interested in improving logback, great! The logback community
looks forward to your contribution. Please follow this process:

1. Please file a [bug
   report](https://logback.qos.ch/bugreport.html). Pull requests with
   an associated JIRA issue will get more attention.

   Optional: Start a discussion on the [logback-dev mailing
   list](https://logback.qos.ch/mailinglist.html) about your proposed
   change.

2. Fork qos-ch/logback. Ideally, create a new branch from your fork for
   your contribution to make it easier to merge your changes back.

3. Make your changes on the branch you hopefuly created in Step 2. Be
   sure that your code passes existing unit tests.

4. Please add unit tests for your work if appropriate. It usually is.

5. Push your changes to your fork/branch in github. Don't push it to
   your master! If you do it will make it harder to submit new changes
   later.

6. Submit a pull request to logback from from your commit page on
   github.


# Build Status
[![Build Status](https://travis-ci.org/qos-ch/slf4j.png)](https://travis-ci.org/qos-ch/slf4j)
