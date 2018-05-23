
allows rules to create civi activities 

this module started as a helper function for 
PhillyCAM content moderation

when this funciton is called by a rule 
it needs to be passed the current node; 
the logged in user taking the action; 
the civicrm activity id to be created
 
cma_moderation_rules_civi_create_activity($node,$user,00);

an activity of the type specified will be added 
to the node author's contact record and that activity 
will be 'with' or 'added by' the user taking the action 

at the moment the subject/message for the activity detail
is hard coded. this will be changed soon to also come from
a value passed in by the rule. 
