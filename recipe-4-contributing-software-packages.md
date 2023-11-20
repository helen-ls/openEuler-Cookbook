# 💼 Recipe 4: Contributing software packages

Another way to participate is by contributing software packages for openEuler. If you find that openEuler is missing any software package, you can contribute it to the openEuler community. First, you need to understand what is a Linux software package, and how to make a software package. Linux software package is a way of packaging software's source code, compilation scripts, configuration files, dependency relationships, and other information into a file, which is convenient for users to install and manage. Follow the following steps to add your flavorful contribution to the openEuler community:

1. Go to the [community repository](https://gitee.com/openeuler/community) and click **Fork**.
2. Clone the forked community repository to local.
3. Modify the community repository:

* Identify the SIG to which the software package belongs.
* Modify the contents under the SIG folder, such as the project list.
* Modify the **sig-info.yaml** under the relevant SIG folder, adding the new software package in the format "- src-openeuler/zip" to the corresponding SIG's list. Taking ZIP as an example, modify **sig/Base-service/sig-info.yaml**: repositories:
* repo:
  * openeuler/openEuler-rpm-config
  * src-openeuler/abseil-cpp
  * src-openeuler/acl
  * src-openeuler/acpica-tools
  * src-openeuler/adcli
  * src-openeuler/aide
  * src-openeuler/airline
  * ...
  * src-openeuler/jansson
  * src-openeuler/apr
  * src-openeuler/python-lxml
  * src-openeuler/zip

4. Create a new repository in **sig/{SIG directory}/src-openeuler/first letter of the software name** (For projects maintained by the openEuler community: openeuler directory; for packages from other communities: src-openeuler directory):

```YAML
name: pkgname
description: about pkgname
upstream: https://somepkg.org/
branches:
- name: master
  type: protected
type: public
```

* Your task is to modify the files and then submit a PR. Explain clearly in the commit message why you are adding such a package or creating such a repository. The better your commit message, the easier it is to pass the review.
* Once the PR is merged, a repository with the same name will be created on Gitee. You can check the address at src-openeuler. Contributing software packages enhances openEuler functionalities, making openEuler a software ecosystem with anything you need. You can also get recognition and appreciation from the community, and become a valuable contributor to openEuler. So, don't hesitate, contribute your software packages and let your work shine!
