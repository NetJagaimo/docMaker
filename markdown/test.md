# test


# Title 1
## Title 2
jasdkfj
sdfs
### Title 3


| Name | Type | Description | Create Rule |
| ---- | ---- | ---- | ---- |
| source_contact_id | int unsigned | Contact ID of the person scheduling or logging this Activity. Usually the authenticated user. |  |
| source_record_id | int unsigned | Artificial FK to original transaction (e.g. contribution) IF it is not an Activity. Table can be figured out through activity_type_id, and further through component registry. |  |
| activity_type_id | int unsigned | FK to civicrm_option_value.id, that has to be valid, registered activity type. |  |
| target_entity_table | varchar | Name of table where item being referenced is stored. | required |
| target_entity_id | int unsigned | Foreign key to the referenced item. | required |
| subject | varchar | The subject/purpose/short description of the activity. |  |
| scheduled_date | datetime | Date and time meeting is scheduled to occur. |  |
| activity_date_time | datetime | Date and time this activity is scheduled to occur. Formerly named scheduled_date_time. |  |
| due_date_time | datetime | Date and time this activity is due. |  |
| duration_hours | int unsigned | Planned or actual duration of meeting - hours. |  |
| duration_minutes | int unsigned | Planned or actual duration of meeting - minutes. |  |
| duration | int unsigned | Planned or actual duration of activity expressed in minutes. Conglomerate of former duration_hours and duration_minutes. |  |
| location | varchar | Location of the activity (optional, open text). |  |
| phone_id | int unsigned | Phone ID of the number called (optional - used if an existing phone number is selected). |  |
| phone_number | varchar | Phone number in case the number does not exist in the civicrm_phone table. |  |
| details | text | Details about the activity (agenda, notes, etc). |  |
| status | enum | What is the status of this meeting? Completed meeting status results in activity history entry. |  |
| status_id | int unsigned | ID of the status this activity is currently in. Foreign key to civicrm_option_value. |  |
| priority_id | int unsigned | ID of the priority given to this activity. Foreign key to civicrm_option_value. |  |
| parent_id | int unsigned | Parent meeting ID (if this is a follow-up item). This is not currently implemented |  |
| is_test | boolean |  |  |
| medium_id | int unsigned | Activity Medium, Implicit FK to civicrm_option_value where option_group = encounter_medium. |  |
| is_auto | boolean |  |  |
| relationship_id | int unsigned | FK to Relationship ID |  |
| is_current_revision | boolean |  |  |
| original_id | int unsigned | Activity ID of the first activity record in versioning chain. |  |
| result | varchar | Currently being used to store result id for survey activity, FK to option value. |  |
| is_deleted | boolean |  |  |

{{SAMPLE_CODE}}

{{RESULT}}

