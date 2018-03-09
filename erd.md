The following are the schemas that I am planning to use for the project:
(this will be in sql)
------------------------------------------------------------------------

users(
  admin
  owner
  guest
)

owner_property_join(    --properties can have multiple owners
    owner_id
    property_id
)


properties(   
  property_name
  property_picture
  property_location
)

property_o_c_join(    --each property can have only 1 of each list
  property_id
  opening_list_id
  closing_list_id
)

opening_closing(  
  opening_list
  closing_list
)

chores(  
  chore_name
  chore_notes
)

task_property_join(   --each task will only apply to 1 property
  task_id
  property_id
)

visits(  
  visit_start_date
  visit_end_date
  visit_guest_count
)

visit_property_join(    
  visit_id
  property_id
  user_id
)
