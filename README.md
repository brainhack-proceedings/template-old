## STEP 1 - Get the machinery running ⚙️

### ⑂ Fork this repository

### ✅ Enable actions 

Go to the `Actions` tab in your forked repo, and click the green button that says "I understand my actions, go ahead and enable them".

### 🔑 Create a GitHub access token

Read the warning below and follow [these steps](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token#creating-a-token). 

| ⚠️ Warning|
| :--- |
|Make sure that you check the **repo**, **admin:repo_hook** and **workflow** boxes while creating your access token. Please not lose the generated key, at least until the next step :)|

###  🕵️‍♀️ Create an encrypted secret for your repo

Simply follow [these steps](https://docs.github.com/en/free-pro-team@latest/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository).

The name of the secret must be `PAT_BOT` and the value must be the key you obtained from the previous step.

### ⬆️ Push a dummy change to the `master` 

It can be anything, such as simply editing this README.md file you are reading at the moment. 

### 👀 What now ?  

After pushing your changes to the `master` branch, visit the **Actions** tab of your repository. You should see an action named **Build proceeding PDF**, which consists of two steps `buildPDF` and `buildHugo`.  

Soon after a successful action run, your web page will be deployed. You should see **Environments** section appeared in your repository (on the right column). In the **Environments** page, click the `View Deployment` button to visit your report page! At this stage, it should be identical to the [BrainHack proceedings template webpage](http://brainhack-proceedings.github.io/template).

Unless you change the name of the repo you forked from `template` to something else, your page will be published at _your_GitHub_handle.github.io/template_. 


## STEP 2 - Edit your report ✍️

* Place your figures in the [`figures`](figures) folder. 

* Edit [`report.md`](report.md) file to create your own report. The template markdown will walk you through how to cite references, add figures and equations etc.

* Edit [`report.bib`](report.bib) to add your bibliography in [BibTeX](http://www.bibtex.org/) format.


| ⚠️ Warning|
| :--- |
|Please do not change the name or the location of [report.md](report.md) and [report.bib](report.bib). Unless you provide an absolute path for your figures, they will be looked for in the `figures` folder.|


Whenever you push your changes to the `master` branch (either directly or via merging a branch), GitHub actions will be triggered to update your report. That's it! 

If actions run completes successfully, orange points (running) will turn into green checks (success). If your build fails, you will see a red cross instead. In that case, you can read the logs to see what went wrong.
