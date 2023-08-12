
# CodeFolio   
Tagline: < code. cultivate. create />

Objective: To deliver an adaptive learning ecosystem where users can seamlessly organize educational materials, experiment with code in real-time, build a professional online presence, and find solace in moments of cognitive intensity.



## Tech Stack

- Frontend: React
- Backend: Django
- Database: PostgreSQL
- Code Editor: via 3rd party API (for the coding playground)


## Features

- Resource Cataloguing

        Allows users to upload and organize various educational materials like videos, files, images, etc., making it easier for them to reference back at any point.

        Enhanced organization with "Favorites" and "Search/Filter" functionalities.

- Interactive Coding Playground

        Users can practice coding, run scripts, and see real-time results.

        Based on 3rd party API

- Project Storage

        A dedicated space for users to store, manage, and showcase coding projects they've built over time.

- Portfolio Builder

        A built-in project for users to code and create their portfolio from scratch (in coding playground), reflecting their journey and achievements. Sharable via QR code (also have ability to upload from external source)

- Resume Vault

        A space for students to store multiple copies of their resume. Sharable via QR code.

- Zen Den

        Offers short meditation sessions, calming visualizations, and soothing frequencies.

        Periodic reminders for users to take a break, refresh, and refocus.

        * May only introduce as beta/coming soon? 


## Additional Features
- Personalized Sharing

        Unique QR code assigned to each user's resume and portfolio for easy sharing with potential employers or on social media.

        An accompanying written link provided for alternative access.

- Inbox/Notification Center
        
        Feature for users to receive comments/notes/messages from viewers.
## Components Guide
1. Atomic Component Breakdown:

    Atoms:

        Button (Sign in, Register, Submit, etc.)

        Input Field (Username, Password, etc.)

        Icons (For Learning Hub, Code Playground, Zen Den, etc.)

        Checkbox (Favorites)

    Molecules:

        Sign In Form (Username + Password + Remember me + Submit Button)

        Registration Form

        Message/Notification Alert

        Navbar Items (Combination of Icon + Label)

        User Resource Card (Title, Link, Thumbnail, Description, etc.)

    Organisms:

        Navbar

        Sign In/Register Modal

        Code Playground Interface

        Zen Den Interface

        Portfolio Builder Interface

        Resume Vault Interface

    Templates:

        Home Page without specific user data

        Learning Hub Page Template

        Code Playground Page Template

        Zen Den Page Template

    Pages:
       
        Welcome 
        
        Home Page/Learning Hub (User Logged in)
        
        Coding Playground/Projects 

        Professional Development

        Zen Den





2. State Management:

- User authentication status (Logged in / Logged out)

- User-specific data (For resources, projects, etc.)

- Current page/view state

- Notification/Message state

3. Reusable Components:

- Navbar

- Input Field

- Button

- Icons

4. Routing:

- /: Home Page (user)
- /welcome: Welcome Page (guest)

- /about: About Us

- /learning-hub: Learning Hub/Resources

- /playground: Code Playground

- /development: Professional Development

- /zen-den: Zen Den

5. API/Data Interaction:

- User registration and authentication

- Fetching user-specific resources, projects, and progress

- Storing new resources, notes, and projects

- Updating existing resources and projects

- 3rd party API for code editor integration
## Major Functionalities
1. User Authentication:

- Functionality: Enables a user to register and login.
- Funnels:

        >>> Registration:

        User clicks on "Sign In/Register".

        Option to "Register" is presented.

        User fills in details and submits.

        Success message is shown; user is redirected to their personal dashboard.



        >>> Login:

        User clicks on "Sign In/Register".

        User enters login credentials.

        Successful login redirects to user's personal dashboard.

        * No duplicate emails allowed 

2. Resource Cataloging:

- Functionality: Allows users to upload, annotate, and organize learning materials.
- Funnels:

        >>>Uploading Materials:

        User navigates to "Learning Hub".

        User clicks on "Add Resource".

        User uploads material (video, image, document) and adds description/notes.

        Resource is added to user's catalog.



        >>>Viewing & Organizing Materials:

        User browses through uploaded materials.

        User can search, filter, or categorize resources.

        Option to edit, delete, or add further annotations.

3. Interactive Code Playground:

- Functionality: Provides an environment for users to write, test, and see the output of their code.
- Funnels:

        User navigates to "Code Playground".

        User writes or pastes code.

        User runs code and views results.

        Option to save code snippets or projects.

4. Invite Code:

- Functionality: Includes the QR code(invite) for selected portfolio and resume
- Funnels:

        >>>Resume Vault:

        User uploads resumes.

        User selects a default resume to be linked with the QR code.

        User views or downloads uploaded resumes.

        >>>Portfolio

        User builds portfolio in "projects" via code editor

        User links portfolio project to QR data 

5. Zen Den:
- Functionality: Encourages users to take healthy breaks while promoting mindfulness through multiple activities
- Funnels:
        
        User accesses the "Zen Den".

        User selects and engages with relaxation or inspiration modules.

6. Navbar Personalization:

- Functionality: Navbar's contents change based on the user's authentication status.
- Funnels:

        >>>Logged Out: Only "Home", "About Us", and "Sign In/Register" are visible.

        >>>Logged In: "Home", "Learning Hub", "Code Playground", "Professional Development", and a notification center become accessible.

7. Notifications & Interactions:

- Functionality: Users receive feedback and notifications, including comments on their portfolios.
- Funnels:

        User receives a notification about a comment on their portfolio.
        
        User views the comment in their personal dashboard's "inbox".

        User has the option to delete the comment.
## User Stories
Resource Cataloguing

    - As a student, I want to upload and catalog various educational materials (like videos, files, images) so I can easily access and review them later.

    - As a user, I wish to organize my resources into categories or topics (like HTML, CSS, JavaScript, etc.) for efficient retrieval.

    - As a learner, I want to make additional comments or notes on each uploaded material to provide context or reminders about the content.

    - As a student, I want the ability to use favorites and search/filter functionalities to swiftly locate specific resources.

    - As a user, I want the ability to delete any material as I desire to manage my storage and keep relevant resources.

Interactive Code Playground

    - As a student, I want a dedicated space where I can write, test, and run code snippets to practice my programming skills.

    - As a user, I wish to see real-time results/output of the code I run, ensuring immediate feedback and correction.

    - As a learner, I want integrated documentation or hints to help me when I'm stuck or to provide information on certain coding constructs.

Portfolio Builder

    - As a user, I want a space where I can create a coding portfolio from scratch, showcasing my projects, skills, and learning progression.

    - As a student, I want to be able to share my portfolio via a unique QR code, ensuring easy access for potential employers, colleagues, or mentors.

    - As a user, I want the QR code to also provide a direct written link to my portfolio for users who might have issues with QR scanning.

    - As a learner, I want to receive comments/notes/messages on my portfolio, visible only to me, for feedback or collaboration purposes.

Resume Vault

    - As a user, I want to upload and store multiple versions of my resume in a centralized location.

    - As a student, I want to choose a primary resume that will be the version shared when using my unique QR code.

    - As a learner, I want the ability to make additional comments or notes alongside each uploaded version of my resume.

    - As a user, I want the assurance that while viewers can access my primary resume and portfolio, only I have the ability to make edits or updates to them.

    - As a student, I want a written link embedded in or alongside the QR code to ensure alternate access.

Zen Den

    - As a user, when feeling overwhelmed, I want a dedicated space within the platform to relax.

    - As a student, I want calming visualizations to momentarily distract from coding challenges.

    - As a learner, I'd like quick mental exercises or games to help shift focus and take a cognitive break.

    - As a student, I want a timer feature to manage relaxation intervals and study breaks effectively.

    - As a user, I want the Zen Den to be easily accessible from anywhere on the platform.
## Database Schema
https://drawsql.app/teams/grlcode/diagrams/codefolio/embed

## Design Plan
https://www.tldraw.com/s/v2_c_TgpjRPUPt_I0wc4kzrhqk?viewport=-5402%2C-3600%2C12690%2C7140&page=page%3ApB8rnUWTCDXc5Hz5loztz