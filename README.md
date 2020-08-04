# Portfolio #1

# 1) Experimenting with Markdown from Assignment 1
##  Name
**My name is Amara Huntington**
### Photo
![Pic](https://user-images.githubusercontent.com/69179367/89253756-dffeac00-d5f3-11ea-8a35-362c7cff7db7.jpg)
### Year
~~I'm currently in my fourth year~~
### Major
**_Neuroscience_**
### Reason for Enrollment 
**To fulfill the lab requirement for my degree program. I also hope to expand my skill set in this unfamiliar field in order to become a well rounded student.**
### Interest in Neuroscience
>I became interested in Neuroscience because I love to learn about the complexities of life. I remember being mind-blown once I had learned about cells as a child, as it shifted my entire perspective of existence. Neuroscience is an amazing field because it goes in depth into these intricacies of life but it also explores broader topics in psychology and sociology.
### Future Plans
I currently do not have a set career path that I've decided upon. After graduation I plan to travel in hopes to learn about the various options that are available to me.

# 2) Writing a loop to convert seconds to milliseconds from Assignment 2
import numpy as np
import pandas as pd
rt = [0.551714007, 0.344355373, 0.282130643, 0.388339099, 0.741976576, 0.426807824, 0.589848489, 0.341542697, 0.287110004, 0.322289797, 0.379822366, 0.336714422, 0.333802666, 0.293643588, 0.386914908, 0.282874789, 0.383207132, 0.416732649, 0.329448009, 0.554469006, 0.523510978, 0.341133708, 0.508971072, 0.389857974, 0.404175466]
rt_ms= []
for var in rt:
    print(var * 1000)
print(rt_ms)

# 3) Reading and Examining Datafiles
import pandas as pd
import numpy as np

subjects = ['spid10_2014_06_17_17_44', 'spid12_2014_06_20_15_11']

in_file = (subjects[0]+ "/"+ subjects[0]+ '_data.txt')
df= pd.read_csv(in_file, sep='\t')
df.head()

# 4) Creating a barplot with subgroups and subplots

# Set the figure style to "dark"
sns.set_style("dark")  

# Adjust to add subplots per gender
g = sns.catplot(x="Village - town", y="Likes Techno", 
                data=survey_data, kind="bar", hue="Gender", col="Gender")

# Add title and axis labels
g.fig.suptitle("Percentage of Young People Who Like Techno", y=1.02)
g.set(xlabel="Location of Residence", 
       ylabel="% Who Like Techno")

# Show plot
plt.show()

# 5) Manipulating Dictionaries

# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Add italy to europe
europe['italy']= 'rome'

# Print out italy in europe
print('italy' in europe)

# Add poland to europe
europe['poland']= 'warsaw'

# Print europe
print(europe)

# Grouping and aggregating Categorical Data
# Group titanic by 'pclass' 

by_class = titanic.groupby('pclass') 

Aggregate 'survived' column of by_class by count 

count_by_class = by_class['survived'].count() 

Print count_by_class 

print(count_by_class)  

# Group titanic by 'embarked' and 'pclass' 

by_mult = titanic.groupby(['embarked','pclass'])  

# Aggregate 'survived' column of by_mult by count 

count_mult = by_mult['survived'].count() 

  

# Print count_mult 

print(count_mult) 
