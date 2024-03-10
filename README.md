<hr>
<bold></bold>Technologies Used:<bold/>

    Database: MongoDB
    Backend: Express.js, Node.js
    Frontend: React.js
<hr>
Features:
Authentication:

    Login: Job seekers and providers can log in to their accounts.
    Sign Up: New users can register as job seekers or providers.
    Logout: Users can securely log out of their accounts.

Job Seeker Operations:

    Apply for Jobs: Job seekers can apply for multiple jobs available on the platform.
    Update Data: Job seekers can update their profile information.
    Resume Upload: Job seekers can upload their resumes for job applications.
    Withdraw Applications: Job seekers can withdraw their applications if needed.
    Delete Account: Job seekers have the option to delete their accounts.

Job Provider Operations:

    Post Jobs: Employers can post job listings on the platform.
    Review Applications: Employers can review applications submitted by job seekers.

Admin Operations:

    Update and Modify Data: Administrators have the authority to update and modify data on the platform.
    Account Review: Administrators can review user accounts for compliance and management.
    API Endpoint Documentation for GetMeScript (Job Portal)

<hr>
User Operations-
<bold>Endpoints<bold/>
<hr>
1. User Registration

    Endpoint: localhost:4000/api/v1/user/register
    Method: POST
    Description: Registers a new user on the GetMeScript job portal.
    Request Body: JSON containing user details (e.g., username, email, password).
    Response: Success message or error if registration fails.

2. User Login

    Endpoint: localhost:4000/api/v1/user/login
    Method: POST
    Description: Allows users to log in to their GetMeScript job portal accounts.
    Request Body: JSON containing user credentials (e.g., username/email and password).
    Response: Authentication token or error if login fails.

3. User Logout

    Endpoint: localhost:4000/api/v1/user/logout
    Method: GET
    Description: Logs out the currently authenticated user from the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Response: Success message or error if logout fails.

4. Get User Information

    Endpoint: localhost:4000/api/v1/user/getuser
    Method: GET
    Description: Retrieves information about the currently authenticated user on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Response: User details or error if retrieval fails.

Job Seeker Operations
1. Apply for Job

    Endpoint: localhost:4000/api/v1/application/post
    Method: POST
    Description: Allows job seekers to apply for multiple jobs on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Request Body: JSON containing application details (e.g., job ID, cover letter).
    Response: Success message or error if posting fails.

2. Update Job Seeker Data

    Endpoint: localhost:4000/api/v1/jobseeker/update
    Method: PUT
    Description: Allows job seekers to update their profile data on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Request Body: JSON containing updated job seeker details.
    Response: Success message or error if update fails.

3. Upload Resume

    Endpoint: localhost:4000/api/v1/jobseeker/resume/upload
    Method: POST
    Description: Allows job seekers to upload their resumes on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Request Body: Form-data containing the resume file.
    Response: Success message or error if upload fails.

4. Withdraw Application

    Endpoint: localhost:4000/api/v1/application/withdraw/{application_id}
    Method: DELETE
    Description: Allows job seekers to withdraw their application for a specific job on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Response: Success message or error if withdrawal fails.

5. Delete Account

    Endpoint: localhost:4000/api/v1/jobseeker/delete
    Method: DELETE
    Description: Allows job seekers to delete their account on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Response: Success message or error if deletion fails.

Job Provider Operations
1. Post a Job

    Endpoint: localhost:4000/api/v1/job/post
    Method: POST
    Description: Allows employers to post new job listings on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers.
    Request Body: JSON containing job details (e.g., title, description).
    Response: Success message or error if posting fails.

2. Review Applications

    Endpoint: localhost:4000/api/v1/application/provider/getall
    Method: GET
    Description: Retrieves all applications submitted for job listings posted by the employer on the GetMeScript job portal.
    Authorization: Requires authentication token in the request headers (for job provider).
    Response: List of applications or error if retrieval fails.

Admin Operations
1. Update and Modify Data

    Endpoint: localhost:4000/api/v1/admin/data/update
    Method: PUT
    Description: Allows admin to update and modify data on the GetMeScript job portal.
    Authorization: Requires admin privileges.
    Request Body: JSON containing updated data.
    Response: Success message or error if update fails.

2. Review Accounts

    Endpoint: localhost:4000/api/v1/admin/accounts/review
    Method: GET
    Description: Allows admin to review user accounts on the GetMeScript job portal.
    Authorization: Requires admin privileges.
    Response: List of user accounts or error if retrieval fails.

