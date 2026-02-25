# Data Dictionary

Created by Erick Busuulwa ([devericklasco](https://github.com/devericklasco)).

| field_name | type | required | description | notes |
|---|---|---|---|---|
| start | start | no | Interview start timestamp | Metadata auto-captured by SurveyCTO. |
| end | end | no | Interview end timestamp | Metadata auto-captured by SurveyCTO. |
| today | today | no | Interview date | Metadata auto-captured by SurveyCTO. |
| deviceid | deviceid | no | Device identifier | Supports device-level QA. |
| enumerator_id | text | yes | Enumerator code | Constraint enforces E001-style format. |
| respondent_code | text | yes | Unique respondent code | Alphanumeric plus hyphen, 4-20 chars. |
| district | select_one district_list | yes | Interview district | Controlled choice list. |
| subcounty | text | yes | Interview sub-county | Free text for local admin unit. |
| parish | text | yes | Interview parish | Free text for local admin unit. |
| farm_gps | geopoint | no | Farm GPS point | Capture near farm entrance when safe. |
| gps_accuracy_m | calculate | no | GPS accuracy in meters | Extracted from geopoint 4th value. |
| duration_sec | calculate | no | Interview duration in seconds | Computed from end-start timestamps. |
| consent_given | select_one yes_no | yes | Informed consent status | Core gate for main modules. |
| respondent_age | integer | yes | Respondent age in years | Must be 18-99. |
| respondent_gender | select_one gender_list | yes | Respondent gender | Single choice. |
| household_size | integer | yes | Household member count | Must be 1-25. |
| total_land_acres | decimal | yes | Total land holding in acres | Range constrained 0-100. |
| coffee_acreage | decimal | yes | Land under coffee in acres | Cannot exceed total_land_acres. |
| coffee_type_main | select_one coffee_type | yes | Primary coffee type | Arabica/Robusta/Unknown. |
| land_tenure | select_one tenure_type | yes | Land tenure status | Owned, rented, shared, or other. |
| water_access | select_one water_access | yes | Water availability for farm work | Reliability level of access. |
| income_sources | select_multiple income_sources | yes | Main household income sources | Multiple selections allowed. |
| income_source_other | text | yes (conditional) | Other income source detail | Required when income_sources includes other. |
| management_practices | select_multiple practice_list | yes | Coffee management practices in use | Multiple selections allowed. |
| fertilizer_use | select_one yes_no | yes | Fertilizer use in last 12 months | Controls fertilizer follow-up. |
| fertilizer_type | select_one fertilizer_type | yes (conditional) | Main fertilizer type | Required when fertilizer_use is yes. |
| fertilizer_type_other | text | yes (conditional) | Other fertilizer type detail | Required when fertilizer_type is other. |
| coffee_yield_kg | decimal | yes | Estimated coffee harvest (kg) | Range constrained 0-50,000. |
| yield_per_acre_kg | calculate | no | Yield per acre (kg/ac) | Safe divide: blank when coffee_acreage is zero. |
| major_challenges | select_multiple challenge_list | yes | Main production challenges | Multiple selections allowed. |
| challenge_other | text | yes (conditional) | Other challenge detail | Required when major_challenges includes other. |
| sales_last_season | select_one yes_no | yes | Coffee sales last season | Controls price question relevance. |
| avg_price_ugxkg | decimal | yes (conditional) | Average selling price (UGX/kg) | Required when sales_last_season is yes; constrained range. |
| climate_shocks_past12m | select_multiple shock_list | yes | Shocks experienced in last 12 months | Multiple selections allowed. |
| irrigation_access | select_one yes_no | yes | Access to irrigation or stored water | Binary response. |
| received_weather_info | select_one yes_no | yes | Received weather information recently | Binary response. |
| training_access | select_one training_access | yes | Primary source of farm training | Includes none and other. |
| training_source_other | text | yes (conditional) | Other training source detail | Required when training_access is other. |
| csa_practices | select_multiple csa_practices | yes | Climate-smart practices used | Multiple selections allowed. |
| advice_topics | select_multiple advice_topic | yes | Preferred advisory topics | Multiple selections allowed. |
| advice_topic_other | text | yes (conditional) | Other advisory topic detail | Required when advice_topics includes other. |
| preferred_language | select_one lang_pref | yes | Preferred language for advisory | Luganda/English/Both/Other local. |
| delivery_channels | select_multiple channel_pref | yes | Preferred delivery channels | At least one required. |
| delivery_channel_other | text | yes (conditional) | Other delivery channel detail | Required when delivery_channels includes other. |
| availability_slots | select_multiple availability_slots | yes | Preferred time windows | Multiple selections allowed. |
| willing_followup | select_one yes_no | yes | Willingness for follow-up pilot | Controls phone contact field. |
| preferred_contact_number | text | yes (conditional) | Preferred phone contact | Required when willing_followup is yes; 9-15 digits. |
| interview_completed | select_one yes_no | yes (conditional) | Whether interview was completed | Asked when consent is yes. |
| incomplete_reason | select_one incomplete_reason | yes (conditional) | Main reason for incomplete interview | Asked when consent is no or interview not completed. |
| incomplete_reason_other | text | yes (conditional) | Other incomplete reason detail | Required when incomplete_reason is other. |
| visit_notes | text | no | Enumerator notes | Short factual notes only. |
| form_status | calculate | no | Final submission status | complete, incomplete, or terminated_no_consent. |
