<h2 align="center"> STEP 1 - Get the machinery running ⚙️ </h2>

<h3 align="center"> Fork this repository </h3>

<p align="center"><img src="https://github.com/channelCS/github-buttons/blob/master/2x/github_fork.png"></p>


<h3 align="center"> Enable actions </h3>
<h3 align="center"> ✅</h3>

<p align="center">Go to the <code>Actions</code> tab in your forked repo, and click the green button that says "I understand my actions, go ahead and enable them".</p>


<h3 align="center">  Create a GitHub access token </h3>
<h3 align="center"> 🔑 </h3>

<p align="center">Follow <a href="https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token#creating-a-token">these steps</a> and make sure that you check the <b>repo</b>, <b>admin:repo_hook</b> and <b>workflow</b> boxes while creating your access token.</p> 


<h3 align="center"> Create an encrypted secret for your repo </h3>
<h3 align="center"> 🕵️‍♀️ </h3>


<p align="center"> Simply follow <a href="https://docs.github.com/en/free-pro-team@latest/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository">these steps</a>.</p>

<p align="center">  The name of the secret must be <code>PAT_BOT</code> and the value must be the key you obtained from the previous step. </p>


<h3 align="center"> Push a dummy change to the <code>master</code> </h3>
<h3 align="center"> 📤 </h3>

<p align="center"> It can be anything, such as simply editing this <code>README.md</code> file you are reading at the moment. </p>


<h3 align="center"> What now ?  </h3>
<h3 align="center"> 👀 </h3>

<p align="center">After pushing your changes to the <code>master</code> branch, visit the <b>Actions</b> tab of your repository. You should see an action named <b>Build proceeding PDF</b>, which consists of two steps <code>buildPDF</code> and <code>buildHugo</code>.</p>  

<p align="center">Soon after a successful action run, your web page will be deployed. You should see <b>Environments</b> section appeared in your repository (on the right column). In the <b>Environments</b> page, click the <code>View Deployment</code> button to visit your report page! At this stage, it should be identical to the <a href="http://brainhack-proceedings.github.io/template">BrainHack proceedings template webpage</a>.</p>

<p align="center">Unless you change the name of the repo you forked from <code>template</code> to something else, your page will be published at <i>your_GitHub_handle.github.io/template</i>.</p> 


## STEP 2 - Edit your report ✍️
  

* Place your figures in the [`figures`](figures) folder. 

* Edit [`report.md`](report.md) file to create your own report. The template markdown will walk you through how to cite references, add figures and equations etc.

* Edit [`report.bib`](report.bib) to add your bibliography in [BibTeX](http://www.bibtex.org/) format.


| ⚠️ Warning|
| :--- |
|Please do not change the name or the location of [report.md](report.md) and [report.bib](report.bib). Unless you provide an absolute path for your figures, they will be looked for in the `figures` folder.|


**Whenever you push your changes to the `master` branch** (either directly or via merging a branch), GitHub actions will be triggered to update your report. That's it! 

If actions run completes successfully, 🟠 (running) will turn into ✅ (success). If your build fails, you will see ❌ instead. In that case, you can read the logs to see what went wrong.
