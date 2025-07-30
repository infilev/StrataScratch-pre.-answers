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
    
                
