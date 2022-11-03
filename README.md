# DSA4262-Project-2
*The following showcases 2 sets of instructions - 1 set of instruction showing how to train a model and use that model to predict the probability that the DRACH sites in the test data are m6A positive, while the other set showing how to use a model (gradientboostingclassifier.sav) for prediction.* For my coursemates, please follow **I. Prediction using model**

<H1>I. Prediction using model</H1>
<p>
1. Start up an AWS ubuntu instance before proceeding to the next steps to install Jupyter Notebook. You can also follow the video demonstration if you are not sure how to install it on your own. <b>Before proceeding any further, please shut down your local Jupyter Notebook if it is using port 8889.</b>
</p>
<p>
  2. Using powershell (<i>For Windows Users</i>)/ terminal (<i>For Mac Users</i>), run the following code first to connect to the AWS instance before proceeding to run the rest of the codes: <b>ssh -i {pem_file_directory} -L 8889:localhost:8889 ubuntu@{aws_instance_ip_address}</b> 
</p>
3. Copy paste the rest of the codes into powershell/ terminal to install and open jupyter notebook.
<ul>
  <li> sudo apt update </li>
  <li> sudo apt install python3-pip python3-dev </li>
  <li> sudo -H pip3 install --upgrade pip </li>
  <li> sudo -H pip3 install virtualenv </li>
  <li> mkdir ~/my_project_dir </li>
  <li> cd ~/my_project_dir </li>
  <li> virtualenv my_project_env </li>
  <li> source my_project_env/bin/activate </li>
  <li> pip install jupyter </li>
  <li> jupyter notebook --port 8889 </li>
</ul>
<p>
4. Once jupyter notebook has been opened, start a new notebook instance. Within this notebook instance, run the following command: <b>!git clone https://github.com/Jinghan987/DSA4262-Project-2-Repo.git</b>, which will clone the codes in this repository into Jupyter Notebook.
</p>
<p>
5. In order to do predictions using the model that has been trained, manually navigate to <b>DSA4262-Project-2-Repo</b> within Jupyter Notebook and open up <b>Project 2 - Prediction Script for Github</b> and run all the codes. At the end of the script, the predictions for the test dataset (<i>test_set_github.csv</i>) will be outputted in the form of a csv file (<i>predictions.csv</i>). From <i>predictions.csv</i>, we will be able to observe which DRACH sites are predicted to be m6A positive and which are not.
</p>
  
<H1>II. Model training and prediction using model</H1>
<p>
1. Start up an AWS ubuntu instance before running the following codes to install Jupyter Notebook. You can also follow the video demonstration if you are not sure how to install it on your own. <b>Before proceeding any further, please shut down your local Jupyter Notebook if it is using port 8889.</b>
</p>
<p>
2. Using powershell (<i>For Windows Users</i>)/ terminal (<i>For Mac Users</i>), run the following code first to connect to the AWS instance before proceeding to run the rest of the codes: <b>ssh -i {pem_file_directory} -L 8889:localhost:8889 ubuntu@{aws_instance_ip_address}</b> 
</p>
<p>
3. Copy paste the rest of the codes into powershell/ terminal to install and open jupyter notebook.
</p>
<ul>
  <li> sudo apt update </li>
  <li> sudo apt install python3-pip python3-dev </li>
  <li> sudo -H pip3 install --upgrade pip </li>
  <li> sudo -H pip3 install virtualenv </li>
  <li> mkdir ~/my_project_dir </li>
  <li> cd ~/my_project_dir </li>
  <li> virtualenv my_project_env </li>
  <li> source my_project_env/bin/activate </li>
  <li> pip install jupyter </li>
  <li> jupyter notebook --port 8889 </li>
</ul>
<p>
4. Once jupyter notebook has been opened, start a new notebook instance. Within this notebook instance, run the following command: <b>!git clone https://github.com/Jinghan987/DSA4262-Project-2-Repo.git</b>, which will clone the codes in this repository into Jupyter Notebook. Then manually navigate to <b>DSA4262-Project-2-Repo</b> within Jupyter Notebook and open up <b>Project 2 - Training Script for Github.ipynb</b>
</p>
<p>
5. We will first be using <b>Project 2 - Training Script for Github.ipynb</b> to train a GradientBoostingClassifier. This script will be using <i>train_set_github.csv</i> as an input, and the output from this script will be a model (<b>gradientboostingclassfier.sav</b>), which will be used in <b>Project 2 - Prediction Script for Github.ipynb</b>. This model will then be able to predict the probability that a DRACH site is m6A positive.
</p>
<p>
6. Once the model has been outputted from <b>Project 2 - Training Script for Github.ipynb</b>, we move on to <b>Project 2 - Prediction Script for Github.ipynb</b>, where we will be using the model to predict the probability that a DRACH site in the test data is m6A positive.
</p>
<p>
7. <b>Project 2 - Prediction Script for Github.ipynb</b> will be using <i>test_set_github.csv</i> as an input and through this script, we will be able to obtain the outputs for the test data in the form of a csv file (<i>predictions.csv</i>). From <i>predictions.csv</i>, we will be able to observe which DRACH sites are predicted to be m6A positive and which are not.
</p>
