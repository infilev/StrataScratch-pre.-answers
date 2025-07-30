## Find all posts that were reacted to with a heart
SELECT b.* FROM

facebook_reactions a JOIN facebook_posts b

ON a.post_id = b.post_id 

WHERE a.reaction = 'heart'

## Find all inspections which are part of an inactive program

select * FROM los_angeles_restaurant_health_inspections a

WHERE program_status = 'INACTIVE'


    
                
