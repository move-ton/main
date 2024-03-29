# Free TON DevOps Governance Repository

## How to participate in Contests

1. Each Contest is operated by Sub-Governance (SG) - a group of people responsible for specific domain. Each SG has a separate repository where all Contest materials are hosted. Each Contest participant should know which SG operates the Contest.

2. Fork SG repository https://github.com/freeton-org/SG_REPO_NAME to your account
   ![image](https://user-images.githubusercontent.com/15122233/114208472-30d65980-9966-11eb-800f-bf1a4425e4ca.png)

3. Clone the fork and add your repo to submission directory **using git subtree** functionality:

```sh
git clone https://github.com/<YOUR_NAME>/<SG_REPO_NAME>.git
cd <SG_REPO_NAME>
git subtree add --prefix proposal-<PROPOSAL_NUM>/submission-<SUBMISSION_NUM>/<REPO_NAME> https://github.com/<REPO_USER>/<REPO_NAME>.git <BRANCH_NAME> --squash
git push
```

- `<SG_REPO_NAME>` - SG repository name
- `<YOUR_NAME>` - participant GitHub account name
- `<PROPOSAL_NUM>` - proposal number
- `<SUBMISSION_NUM>` - submission number
- `<REPO_USER>` - participant solution repo owner (it may be an organization as well as Github user)
- `<REPO_NAME>` - participant solution name
- `<BRANCH_NAME>` - branch with contest submission (should exist in `<REPO_USER>`/`<REPO_NAME>` repository)

4. Open pull request into SG repo from your fork
   ![image](https://user-images.githubusercontent.com/15122233/114210462-7ac03f00-9968-11eb-980e-2ac4bafbd5d5.png)

5. If Contest has not ended yet, you may want to push some changes in it. Feel free to do so! Just continue working in your **original repo** and when you're done, pull your changes into existing fork using the same technique (`subtree pull` instead of `subtree add`):

```sh
git subtree pull --prefix proposal-<PROPOSAL_NUM>/submission-<SUBMISSION_NUM>/<REPO_NAME> https://github.com/<REPO_USER>/<REPO_NAME>.git <BRANCH_NAME> --squash

git push
```

6. Changes are in your fork now. Don't forget to submit a separate pull request with changes as was shown before
