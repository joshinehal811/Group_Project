# Group_Project
Group Project for INSY - 695 Adv Topics in IS 1 ( ML in Production)
This brach of repositiry contains the peospect datasets that we had explored

Data_transformed_final is the final dataset after doing some feature_engineering and data cleansing and preprocessing 


Column Name	Description	Possible Values/Examples
**animal_type**-->	The species or type of the animal.	Dog, Cat, Other, Bird

**has_name**-->	Indicates whether the animal has a recorded name.	0 (No name), 1 (Has a name)

**outcome_group**-->	The general outcome category for the animal after shelter stay.	Positive (e.g., adoption), Neutral (e.g., transfer), Negative (e.g., euthanasia)

**age_days_outcome**-->	The age of the animal in days at the time of the outcome.	Numeric values (e.g., 733, 1465)

**age_group_intake**-->	The age group classification of the animal at intake.	Puppy/Kitten, Young Adult, Adult, Senior

**los_at_shelter**-->	Length of stay (in days) at the shelter before the outcome.	Numeric values (e.g., 1, 10)

**month_of_outcome**-->	The month when the outcome occurred.	January, February, etc.

**is_fixed**-->	Indicates whether the animal is spayed/neutered.	0 (Not fixed), 1 (Fixed)

**breed_type**-->	The breed classification of the animal.	Pure (purebred), Mix (mixed breed)

**color_group**-->	The primary color or color group of the animal.	Brown, Black, White, Red, Gold, Grey, Tricolor, Other

**intake_condition_group**-->	The health or condition status of the animal at intake.	Healthy/Normal, Injured, Sick/Medical, Other/Unknown, Life 

Stage/Developmental

**outcome_group**:
Positive might include adoptions, returns to owner, etc.

Negative could involve euthanasia or medical outcomes.

Neutral may represent transfers or other administrative outcomes.

**age_group_intake**:

Puppy/Kitten typically refers to animals under 1 year old.

Young Adult, Adult, and Senior categorize older animals.

**intake_condition_group**:

Life Stage/Developmental may refer to animals needing special care due to age (e.g., neonatal kittens).
