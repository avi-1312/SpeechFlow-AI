Database V1 Design

Users

Stores platform users.

Fied	Type	Description
id	UUID	Unique user ID
name	String	Username
email	String	User email
role	Enum	Contributor,Reviewer,Admin
Created_at Timestamp	Account creation date

Recordings
Stores speech recording information

	Field	Type 	Description
id 		UUID	Unique recording ID
file_name	String	Audio file name
language	String	Recording language
transcript	Text 	Submitted transcript
duration	Float	Audio duration in seconds
status		Enum	Pending, Approved, Rejected
user_id		UUID	Contributor ID
created_id	Timestamp Upload date

Reviews
Stores recording review decisions

  Field	 	Type	Description
id		UUID	Review ID
recording_id	UUID	Reviewed recording
reviewer_id	UUID	Reviewer
decision	Enum	Approved, Rejected
comments	Text	Reviewer comments
created_at 	Timestamp Review date
