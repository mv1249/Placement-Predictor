# Placement Prediction
Campus recruitment is a strategy for sourcing, engaging and hiring young talent for internship and entry-level positions. College recruiting is typically a tactic for medium- to large-sized companies with high-volume recruiting needs, but can range from small efforts (like working with university career centers to source potential candidates) to large-scale operations (like visiting a wide array of colleges and attending recruiting events throughout the spring and fall semester). Campus recruitment often involves working with university career services centers and attending career fairs to meet in-person with college students and recent graduates. Some industries participate in campus recruiting more than others; finance, technology, business consulting, manufacturing and engineering are a few of the most popular.

![](https://github.com/mv1249/Placement-Predictor/blob/main/placement.jpg)

## Dataset
The dataset is collected from Kaggle website. Here is the link for the dataset : https://www.kaggle.com/benroshan/factors-affecting-campus-placement?select=Placement_Data_Full_Class.csv. I have uploaded the same in [`Dataset`](https://github.com/abhisheks008/ML-ProjectKart/tree/patch-29/Campus%20Recruitment%20-%20Analysis%20and%20Prediction/Dataset) folder too, you can access that!

## Goal
The goal of this project is to analyze the factors that can effect the Campus Recruitment, and also creating a model which will predict the chances of getting placed depending on various factors.


## Conclusion
1. As it can be seen, **high percentage of male candidates got placed**. On the other hand, comparitively lower number of female candidates got placed. This is expected as male candidates are generally higher in most brances. Hence, their chances of getting placed is normally higher as well. Let us check the male to female ratio of this branch.

2. The M/F ratio is approximately 2. This can be interpreted as for every 1 female candiate, there are 2 male candiates sitting for placements. **Males outperformed the female candidates in the batch.**

3. All students scoring 80-100% in 10th grade got placed. **Most students in 60-80% range did get placed** while maximum students below 60% **in 10th standard** couldn't get placed. It shows that generally, a student who has done well in 10th grade is more likely to get placed.

4. Almost entire students with 80-100 % got placed. **Most students in 60-80 % range also got placed**. Just like in the case of 10th boards, most students could not get placed in the 0-60 % range.

5. Upon studying the MBA percentage data, we can see that more students from percentage class 2 got placed as opposed to class 3. However, the difference is not as high as for board and UG percentages. Hence, we can say that MBA percentage is not as big as a factor. This could be because MBA is a branch that places much more importance on speaking skills, internships, case studies, etc rather than academic scores. Hence, the play is much more level fielded in this case.

6. **Maximum students enrolled in the program were either from commerce or science background. Very few students were from Arts background.**

7. For 10th Board, the placement ratio for each of the boards is similar. Hence, **we could say that 10th board of examination doesn't hold much value towards placement.**

8. Unlike the case for 10th board, more students opted for state boards in their 12th examinations. The performance of state board students was better as more students from state board of 12th were placed. However, the placed/unplaced ratio for both is nearly identical once again. Hence, **12th board is not playing a significant role once again.**

9. **Majority of the packages will be in the region of 2-4 LPA.**

# Deployment on Azure Cloud

## Set up your initial environment
<ol>
<li>Have an Azure account with an active subscription. <a href="https://azure.microsoft.com/free/?ref=microsoft.com&amp;utm_source=microsoft.com&amp;utm_medium=docs&amp;utm_campaign=visualstudio" data-linktype="external">Create an account for free</a>.</li>
<li>Install <a href="https://www.python.org/downloads/" target="_blank" data-linktype="external">Python 3.6 or higher</a>.</li>
<li>Install the <a href="/en-us/cli/azure/install-azure-cli" target="_blank" data-linktype="absolute-path">Azure CLI</a>, with which you run commands in any shell to provision and configure Azure resources.</li>
</ol>

## Commands for the CLI 

<br>

##### Check the Python Version 

```
 py -3 --version

```

##### Check the Azure CLI Version 

```
az --version

```

##### Then sign in to Azure through the CLI:

```
az login

```
 A tab will be opened in the browser,login into you're registered azure account,


Post successfull login,go to the folder where the code files are present,using the `cd` command as shown ↓
 

```
cd <project folder>

```

Once the control is inside the project folder,you need to install all the requirements which are mentioned in the `requirements.txt` file,but before that we need to create a virtual environment!,it is very important,so for creating a `virtual environment` follow the commands 

```
py -3 -m venv .venv
```

The above ↑ command will create a virtual environment,then type in 

```
.venv\scripts\activate
```

This command is to activate the virtual environment,after this type in 

```
pip install -r requirements.txt
```

By this command you will install all the packages which are mentioned in the `requirements.txt` file,into the virtual environment,once this is done,the task is almost 80% completed,after this inorder to check if the `Flask` App is running successfully on local host run this command

```
flask run
```
If you face any error while running this command,check out whether you're in the same directory where your `app.py` is residing or not,Once this command is successfully executed,the last step is to deploy the flask app on the `Azure` Platform,so for that follow the following command ↓

```
az webapp up --sku B1 --name <app-name>
```

This will take sometime,after completion of this command,you'll find something like this ↓ in your cmd (for example!)

```
{
  "URL": "https://campusplacementpredictor.azurewebsites.net/",
  
}
```
Copy that url from `URL` and that is your deployment of the web app on the Azure cloud.





