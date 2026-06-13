# Test Cases. Level 1: General Form Validation and Filling in Required Fields

* **Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
* **Testing Scope:** User Registration (Sign Up) Form

---

## Item 1.1 Successful registration when all fields are filled with valid data
* **Test Data:** 
  First Name : John | Last Name : Doe 
  DoB : 1990-05-15 | Address : 123 Main Street 
  Postcode : 10001 | City/State : New York 
  Country : United States | Phone: 12125550199
  Email : john.doe.test@gmail.com | Password : Qwerty12345!

𝗘𝘅𝗽𝗲𝗰𝘁𝗲𝗱 𝗥𝗲𝘀𝘂𝗹𝘁 (𝗨𝗜): The fields accept values ​​without validation errors (no red highlights or error text). After clicking the "Register" button, a successful redirect to the profile page occurs.

𝗜𝘁𝗲𝗺 𝟭.𝟮 𝗡𝗲𝗴𝗮𝘁𝗶𝘃𝗲 𝘁𝗲𝘀𝘁: 𝗙𝗼𝗿𝗺 𝘃𝗮𝗹𝗶𝗱𝗮𝘁𝗶𝗼𝗻 𝘄𝗵𝗲𝗻 𝘀𝘂𝗯𝗺𝗶𝘁𝘁𝗲𝗱 𝘄𝗶𝘁𝗵 𝗲𝗺𝗽𝘁𝘆 𝗿𝗲𝗾𝘂𝗶𝗿𝗲𝗱 𝗳𝗶𝗲𝗹𝗱𝘀 (𝗳𝗼𝗿 𝗲𝘅𝗮𝗺𝗽𝗹𝗲, 𝗗𝗮𝘁𝗲 𝗼𝗳 𝗕𝗶𝗿𝘁𝗵 𝗮𝗻𝗱 𝗔𝗱𝗱𝗿𝗲𝘀𝘀)
Steps: 1. Fill in the First Name, Last Name, Email, and Password fields with valid information.
2. Leave the Date of Birth and Address fields completely blank.
3. Click the "Register" button.
𝗘𝘅𝗽𝗲𝗰𝘁𝗲𝗱 𝗥𝗲𝘀𝘂𝗹𝘁 : The form is blocked from submission, and registration fails. Empty fields are highlighted in red, and error messages appear underneath them (e.g., "Please enter a valid date in YYYY-MM-DD format. Date of Birth is required").

𝗜𝘁𝗲𝗺 𝟭.𝟯 𝗜𝗻𝘁𝗲𝗿𝗮𝗰𝘁𝗶𝗼𝗻 𝘄𝗶𝘁𝗵 𝘀𝗽𝗲𝗰𝗶𝗮𝗹 𝗶𝗻𝘁𝗲𝗿𝗳𝗮𝗰𝗲 𝗲𝗹𝗲𝗺𝗲𝗻𝘁𝘀 (𝗗𝗿𝗼𝗽-𝗱𝗼𝘄𝗻 𝗹𝗶𝘀𝘁)
Steps: 1. Click on the Country field.
2. Select the country from the drop-down list.
𝗘𝘅𝗽𝗲𝗰𝘁𝗲𝗱 𝗥𝗲𝘀𝘂𝗹𝘁 : A drop-down list of countries opens, containing available options (including United States); the selected country is fixed in the field.

