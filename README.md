TASK DATE (VERY EASY - LIGHT): 15.03.2018 - FINISHED: 15.03.2018


TASK SHORT DESCRIPTION: 1412 [
								Donated this year should be payment status = paid only figures 
								(in users record, fundraising tab .../admin-portal/members/edit/1#user-fundraising-tab)
							]

GITHUB REPOSITORY CODE: hotfix/task-1412-donated-this-year-on-fundraising-tab


ORIGINAL WORK: https://github.com/BusinessBecause/network-site/tree/hotfix/task-1412-donated-this-year-on-fundraising-tab


CHANGES
 
	IN FILES: 
		
		\network-site\addons\default\modules\network_settings\controllers\members.php

			CHANGED CODE:
			
				Inside edit function 
			
					FROM: $donation_overview['donated_this_year'] = $this->payments_m->total_donations_for_user_by_year($id);
					
					TO: $donation_overview['donated_this_year'] = $this->payments_m->total_donations_for_user_by_year($id, null, 2);
