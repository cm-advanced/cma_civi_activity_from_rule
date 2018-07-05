# cma_civi_activity_from_rule

This module started as a helper function for PhillyCAM content moderation. It provides a way for rules to create civi activities. 

It is intended to act on node save but might work in other contexts. 

The node author and current logged in user both must have a civi contact record. 

This module requires the drupal core php module be enabled so you can call the function from the ruleset or rule 


when this funciton is called by a rule 
it should be passed the current node; 
 * the logged in user taking the action; 
 * the civicrm activity id to be created;
 * the title/subject of the activity to be created;
 * the details of the activity to be created;
 * add a link to the node in the detail (0 for no, 1 for yes): default is 1/yes  
 
example

cma_moderation_rules_civi_create_activity($node,$user,15,$subject,$message,$add_link);


an activity of the type specified will be added to the node author's contact record 
and that activity will be 'with' or 'added by' the user taking the action

at the moment the subject/message for the activity detail is hard coded. 
this will be changed soon to also come from a value passed in by the rule.
