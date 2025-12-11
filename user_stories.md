# User Story Template

**Title:**
_As a [user role], I want [feature/goal], so that [reason]._

**Acceptance Criteria:**
1. [Criteria 1]
2. [Criteria 2]
3. [Criteria 3]

**Priority:** [High/Medium/Low]
**Story Points:** [Estimated Effort in Points]
**Notes:**
- [Additional information or edge cases]

## Admin User Stories

**Title:**
_As an admin, I want to be able to Log into the portal with username and password, so that I could manage the platform securely._

**Acceptance Criteria:**
1. Verify that the login page is accessible.
2. Verify that the login page accepts a username and password.
3. verify that entering valid credentials redirects the user to the admin dashboard.
4. Verify that entering invalid credentials displays an error message.
5. Ensure password characters are masked.

**Priority:** High
**Story Points:** 3
**Notes:**
- Passwords must be hashed in the database.
- Includes a "forgot password" link.

**Title:**
_As an admin, I want to be able to logout, so that I can protect system access from unauthorized users._

**Acceptance Criteria:**
1. Verify that the logout button is clearly visible in the navigation bar.
2. Verify that clicking the logout button redirects the user to the login page.
3. Ensure that clicking the back button in the browser does not allow the user to access the admin dashboard.

**Priority:** High
**Story Points:** 2
**Notes:**
- session tokens should be invalidated immediately upon logout.

**Title:**
_As an admin, I want to be able to add doctors on the portal, so that they can be accessed by patients for appointments._

**Acceptance Criteria:**
1. Verify the add doctor form has name, license, specialization and contact details fields.
2. Verify that duplicate doctor licenses are not allowed.
3. Verify that the form is submitted successfully upon clicking the submit button.

**Priority:** High
**Story Points:** 5
**Notes:**
- Implement proper validation for the form fields.
- Send a welcome email to the doctor upon successful submission.

**Title:**
_As an admin, I want to be able to delete doctors from the portal, so that it does not contain outdated information._

**Acceptance Criteria:**
1. Verify that the delete button is visible and a confirmation dialog is displayed upon clicking the delete button.
2. Verify that the doctor is removed from the list of doctors upon successful deletion.
3. Ensure that the doctor credentials are revoked upon deletion.

**Priority:** Medium
**Story Points:** 3
**Notes:**
- preserve the historical data of deleted doctors.

**Title:**
_As an Admin, I want to run a stored procedure in MySQL CLI, so that I can get the number of appointments per month and track usage statistics._

**Acceptance Criteria:**
1. Verify that the stored procedure is present in the database.
2. Verify that on running the procedure, two columns are returned: month and count.
3. Verify that the data returned accurately reflects the number of appointments per month.

**Priority:** Low
**Story Points:** 3
**Notes:**
- Ensure that the user has the EXECUTE privilege on the stored procedure.

## Patient User Stories

**Title:**
_As a patient, I want to view a list of doctors without logging in, so that I can explore options before registering._

**Acceptance Criteria:**
1. Verify that the list of doctors is displayed on the home page.
2. Ensure that the list is sorted by specialization.
3. Ensure the page is visible to all users.

**Priority:** High
**Story Points:** 3
**Notes:**
- give other sorting options besides specialization.

**Title:**
_As a patient, I want to sign up using my email and password, so that I can book appointments with doctors._

**Acceptance Criteria:**
1. Verify the signup page is accessible to all users.
2. Verify it asks for a name, email and password.
3. Ensure on submit a patient is created in the database.

**Priority:** High
**Story Points:** 5
**Notes:**
- ensure that the email is unique.

**Title:**
_As a patient, I want to login to the portal, so that I can manage my appointments._

**Acceptance Criteria:**
1. verify that on login with patient credentials, redirects the user to the patient dashboard.
2. verify that on login with invalid credentials, displays an error message.
3. Ensure that the password characters are masked when typing.

**Priority:** High
**Story Points:** 4
**Notes:**
- password characters must be hashed in the database.

**Title:**
_As a patient, I want to logout of my account so that I can secure my account._

**Acceptance Criteria:**
1. Ensure the logout button is visible in the navigation bar.
2. Verify that clicking the logout button redirects the user to the login page.
3. Ensure that clicking the back button in the browser does not allow the user to access the patient dashboard.

**Priority:** High
**Story Points:** 3
**Notes:**
- session tokens should be invalidated immediately upon logout.

**Title:**
_As a patient, I want login and book an appointment, so that I can consult with a doctor._

**Acceptance Criteria:**
1. Verify that the book appointment form can select a doctor from the list of doctors.
2. Verify that on clicking submit the appointment is booked successfully.
3. Ensure that the doctor is unavailable for the selected date and time.

**Priority:** High
**Story Points:** 4
**Notes:**
- email the doctor upon successful booking on future iterations.

**Title:**
_As a patient, I want to view my upcoming appointments, so that I can plan accordingly._

**Acceptance Criteria:**
1. Ensure that the list of appointments is displayed on the dashboard.
2. Ensure that the list is sorted by date.
3. Verify that the appointment details are visible on hover.

**Priority:** Medium
**Story Points:** 3
**Notes:**
- ensure that the user can cancel an appointment.

## Doctor User Stories

**Title:**
_As a doctor, I want to login to the portal, so that I can manage my appointments._

**Acceptance Criteria:**
1. Ensure that on successful login, redirects the user to the doctor dashboard.
2. Verify that on login with invalid credentials, displays an error message.
3. Ensure that the password characters are masked when typing.

**Priority:** High
**Story Points:** 3
**Notes:**
- password characters must be hashed in the database.

**Title:**
_As a doctor, I want to logout of the portal, so that I can protect my data._

**Acceptance Criteria:**
1. Verify that the logout button is visible in the navigation bar.
2. Verify that clicking the logout button redirects the user to the login page.
3. Ensure that clicking the back button in the browser does not allow the user to access the doctor dashboard.

**Priority:** High
**Story Points:** 2
**Notes:**
- kill the session upon logout.

**Title:**
_As a doctor, I want to view my appointment calendar, so that I can stay organized._

**Acceptance Criteria:**
1. Verify that the doctor's appointments are displayed on the calendar.
2. Verify that the appointments are sorted by date.
3. Verify that the appointment details are visible on hover.

**Priority:** Medium
**Story Points:** 4
**Notes:**
- ensure the calendar displays only appointments for the current month.

**Title:**
_As a doctor, I want to mark my unavailability, so that patients get informed of only available timeslot._

**Acceptance Criteria:**
1. Verify that the doctor can mark his/her availability on the calendar.
2. Verify that the doctor's availability is saved in the database.
3. Verify that the appointment form marks the selected timeslot as unavailable.

**Priority:** High
**Story Points:** 4
**Notes:**
- Handle edge cases such as marking an unavailable time slot that is already booked.

**Title:**
_As a doctor, I want to update my profile with specialization and contact information, so that the patients have up-to-date information._

**Acceptance Criteria:**
1. verify that the doctor can update his/her profile with specialization and contact information.
2. verify that the updated information is saved in the database.

**Priority:** Medium
**Story Points:** 2
**Notes:**
- ensure that the contact information is verified before saving.

**Title:**
_As a doctor, I want to view patient details of upcoming appointments, so that I can be prepared accordingly._

**Acceptance Criteria:**
1. Verify that the doctor can view the patient details of upcoming appointments.
2. Verify that the patient details are visible on hover.

**Priority:** Low
**Story Points:** 2
**Notes:**
- make the patient details clickable.