# wl-template
Mer info: https://wiki.miljodir.no/display/DEVOPS/Kodelagring+og+-versjonskontroll

Repository Structure:
---

- .github/workflows : Github actions for terraform plan on pull requests and terraform apply on merge.
- modules/          : Reusable terraform modules.
- platform/         : One or more terraform states in subfolders.

Howto or Setup
---

Install the following
- [az-cli](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli) 
- [terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)  
- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)



Once installed, run `az login`. Your account needs access to subscription(s) you want to work with, go to https://github.com/miljodir/cp-yggdrasil and make a pull request to get access. Once you have access, you can run `terraform init` and `terraform plan` in the subfolders of platform/

Protected branch
---

In this repository the main branch is automatically applied by github actions. The branch is protected and all pull requests must be reviewed, check CODEOWNERS file to see possible code reviewers. 