# workout-app-backend
Workout app using Node js , express and mysql

Main components of the app:

1.  User registration and login: This will allow users to create an
    account and log in to the app, which will enable them to access
    their saved workout plans and progress tracking data.
2.  Workout planner: Users will be able to create custom workout plans
    by selecting exercises, setting the number of sets and reps, and
    specifying rest times. The app will generate a plan that the user
    can follow during their workout.
3.  Workout tracker: The app will allow users to track their progress
    during their workout by recording the number of sets, reps, and
    weights lifted. Users can also track their rest times, as well as
    any notes about how they felt during the workout.
4.  Progress tracker: The app will keep a record of the user's progress
    over time, including the number of reps, sets, and weights lifted.
    Users will be able to view their progress in the form of graphs and
    charts, which will help them see how they're improving over time.
5.  Database: The app will store all user data in a secure database,
    which will allow users to access their workout plans and progress
    tracking data from any device.
6.  Notifications: The app will be able to send users notifications
    reminding them to workout or prompting them to enter their progress
    data.
-------------------
 1.  `users`: This table stores information about registered users, including their unique `id`, `username`, and `password`.

2.  `workout_plans`: This table stores information about the workout plans created by each user, including a unique `id`, the `user_id` of the user who created the plan, the plan `name`, a JSON array of `exercises` included in the plan, and the `created_at` timestamp.

3.  `progress`: This table stores information about the progress made by each user, including a unique `id`, the `user_id` of the user who made the progress, the `workout_id` of the workout plan associated with the progress, the number of `sets` performed, the number of `reps` performed, the amount of `weight` lifted, optional `notes`, and the `created_at` timestamp.

The relationships between the tables are

Something went wrong

also defined in the script. Specifically:

-   The `users` table has a one-to-many relationship with both the `workout_plans` and `progress` tables, as each user can create multiple workout plans and track progress on multiple workouts.

-   The `workout_plans` table has a one-to-many relationship with the `progress` table, as each workout plan can be associated with multiple progress records.
1.  `users`: This table stores information about registered users, including their unique `id`, `username`, and `password`.

2.  `workout_plans`: This table stores information about the workout plans created by each user, including a unique `id`, the `user_id` of the user who created the plan, the plan `name`, a JSON array of `exercises` included in the plan, and the `created_at` timestamp.

3.  `progress`: This table stores information about the progress made by each user, including a unique `id`, the `user_id` of the user who made the progress, the `workout_id` of the workout plan associated with the progress, the number of `sets` performed, the number of `reps` performed, the amount of `weight` lifted, optional `notes`, and the `created_at` timestamp.

The relationships between the tables are

Something went wrong

also defined in the script. Specifically:

-   The `users` table has a one-to-many relationship with both the `workout_plans` and `progress` tables, as each user can create multiple workout plans and track progress on multiple workouts.

-   The `workout_plans` table has a one-to-many relationship with the `progress` table, as each workout plan can be associated with multiple progress records.### users
---------------------
### user

| Column | Type | Constraints |
| --- | --- | --- |
| id | INT | PRIMARY KEY |
| username | VARCHAR(255) | UNIQUE, NOT NULL |
| password | VARCHAR(255) | NOT NULL |

### workout_plans

| Column | Type | Constraints |
| --- | --- | --- |
| id | INT | PRIMARY KEY |
| user_id | INT | NOT NULL |
| name | VARCHAR(255) | NOT NULL |
| exercises | JSON | NOT NULL |
| created_at | TIMESTAMP | DEFAULT CURRENT_TIME |

### progress

| Column | Type | Constraints |
| --- | --- | --- |
| id | INT | PRIMARY KEY |
| user_id | INT | NOT NULL |
| workout_id | INT | NOT NULL |
| sets | INT | NOT NULL |
| reps | INT | NOT NULL |
| weight | FLOAT | NOT NULL |
| notes | TEXT |\
 |
| created_at | TIMESTAMP | DEFAULT CURRENT_TIME |
-----------------------------------


-   The `users` table has a one-to-many relationship with both the `workout_plans` and `progress` tables, as each user can create multiple workout plans and track progress on multiple workouts.

-   The `workout_plans` table has a one-to-many relationship with the `progress` table, as each workout plan can be associated with multiple progress records.
1.  `users`: This table stores information about registered users, including their unique `id`, `username`, and `password`.

2.  `workout_plans`: This table stores information about the workout plans created by each user, including a unique `id`, the `user_id` of the user who created the plan, the plan `name`, a JSON array of `exercises` included in the plan, and the `created_at` timestamp.

3.  `progress`: This table stores information about the progress made by each user, including a unique `id`, the `user_id` of the user who made the progress, the `workout_id` of the workout plan associated with the progress, the number of `sets` performed, the number of `reps` performed, the amount of `weight` lifted, optional `notes`, and the `created_at` timestamp.

The relationships between the tables are

Something went wrong

also defined in the script. Specifically:

-   The `users` table has a one-to-many relationship with both the `workout_plans` and `progress` tables, as each user can create multiple workout plans and track progress on multiple workouts.

-   The `workout_plans` table has a one-to-many relationship with the `progress` table, as each workout plan can be associated with multiple progress records.
