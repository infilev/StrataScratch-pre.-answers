## Find all posts that were reacted to with a heart
SELECT b.* FROM

facebook_reactions a JOIN facebook_posts b

ON a.post_id = b.post_id 

WHERE a.reaction = 'heart'

## Find all inspections which are part of an inactive program

select * FROM los_angeles_restaurant_health_inspections a

WHERE program_status = 'INACTIVE'

## Unique Order Values

   def non_duplicate(input):
   
    """ 
    :type input: List[int]
    :rtype: List[int]
    """
    st = set()
    
    ans = []
    
    for value in input:
    
        if value not in st:
        
            st.add(value)
            
            ans.append(value)
            
    return ans 

    OR
    nums = [4, 5, 4, -1, 5, 6, -1]  # example input
    
    new_list = []

    for i in range(len(nums)):

        if nums[i] not in new_list:   # add only if it's not already there
    
              new_list.append(nums[i])

    print(new_list)

## Word Count Challenge

def count_words(sentence):
  
    count = 0
    
    for value in sentence.split():
    
        count = count+1
        
    return count 

    OR

    def word_count(sentence):
    
         words = sentence.split()
    
    return len(words)

## Website visitors tracking

import matplotlib.pyplot as plt

df.head()

plt.figure(figsize=(14,7))

plt.plot(df['date'], df['visitors'], color = 'midnightblue')

plt.title("Visitors", fontsize= 16)

plt.xlabel("Date", fontsize = 12)

plt.ylabel("Number of Visitors", fontsize= 12)

plt.xticks(rotation=45)

plt.grid(True, alpha=0.3)

plt.tight_layout()

plt.show()
    
## Abigail Breslin Nominations

SELECT count(DISTINCT movie) 

FROM oscar_nominees 

WHERE nominee = 'Abigail Breslin'

## Common Words in Two Sentences

import re

def find_common_words(input):
   
    sentence1=input[0].lower()
    
    sentence2=input[1].lower()
    
    # for splitting and removing !, ? etc
    
    words1 = re.findall(r'\b\w+\b', sentence1)
    
    words2 = re.findall(r'\b\w+\b', sentence2)
    
    st = set()
    
    l = []
    
    for val1 in words1:
    
        for val2 in words2:
        
            if val1 == val2 and val1 not in st:
            
                st.add(val1)
                
                l.append(val1) 
                
    return sorted(l)           
                
    
## Smartphone market share
import matplotlib.pyplot as plt

df.head()

plt.figure(figsize=(8, 6))

plt.pie(df['market_share'], labels=df['brand'], colors=['turquoise', 'tomato', 'orchid'])

plt.title("Smartphone")

plt.show()


## Number of Comments Per User in 30 days before 2020-02-10

select user_id, SUM(number_of_comments)  AS total_comments

FROM fb_comments_count 

WHERE created_at BETWEEN '2020-01-11' AND '2020-02-09'

GROUP BY user_id

HAVING sum(number_of_comments)>0

## Replace Nulls with Preceding Non-nulls

def replace_null_values(lst):

    prev = None
    
    for i in range(len(lst)):
    
        if lst[i] is not None:
        
            prev = lst[i]
            
        elif prev is not None:
        
            lst[i] = prev
            
    return lst


 ## Feedback word cloud
 
 from wordcloud import WordCloud
 
import matplotlib.pyplot as plt


feedback = [
    "The new dashboard is amazing and very responsive.",
    "I love the integration with third-party apps.",
    "Dark mode is a fantastic addition!",
    "Performance has improved significantly.",
    "Would be great to have more export options."
]

key_features = {"dashboard", "integration", "dark", "performance", "export"}


text = " ".join(feedback)


def color_func(word, *args, **kwargs):

    return 'violet' if word.lower() in key_features else 'lavender'


wordcloud = WordCloud(width=800, height=400, background_color='white', color_func=color_func).generate(text)

plt.figure(figsize=(10, 5))

plt.imshow(wordcloud, interpolation='bilinear')

plt.axis("off")

plt.show()

## Captain Base Pay

SELECT employeename, basepay

FROM sf_public_salaries

WHERE jobtitle LIKE '%CAPTAIN%';

## Discovering Max Value in Dictionary

def find_max_value(dictionary):

    max_value = float('-inf')
    
    max_key = None
    
    max_index = -1

    for index, key in enumerate(dictionary):
    
        value = dictionary[key]
        
        if value > max_value:
        
            max_value = value
            
            max_key = key
            
            max_index = index

    return [max_value, max_key, max_index]
