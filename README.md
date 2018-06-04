FOR PRIVACY AND CODE PROTECTING REASONS THIS IS A SIMPLIFIED VERSION OF CHANGES AND NEW FEATURES

TASK DATE : 15.03.2018 - FINISHED: 15.03.2018

TASK'S LEVEL: (VERY EASY - LIGHT)

TASK SHORT DESCRIPTION: 1412 [
								Donated this year should be payment status = paid only figures 
								(in users record, fundraising tab .../admin-portal/members/edit/1#user-fundraising-tab)
							]
							
GITHUB REPOSITORY CODE: hotfix/task-1412-donated-this-year-on-fundraising-tab

CHANGES
 
	IN FILES: 
		
		members.php

			CHANGED CODE:
			
				Inside edit function 
			
					FROM: $donation_overview['donated_this_year'] = $this->payments_m->total_donations_for_user_by_year($id);
					
					TO: $donation_overview['donated_this_year'] = $this->payments_m->total_donations_for_user_by_year($id, null, 2);
