This app lets users create new workouts and schedule the workouts on a calendar. Workouts consist of strength/resistance exercises as well as cardio.

### User
    - has many stats
    - has many exercises through stats
    - has many appointments
    - has many workouts
*name
*age:integer
*height:integer
*weight:integer
*admin boolean
*username
*email
*password

### Appointment
    - belongs to user
    - belongs to workout
*date:date
*time:time
*workout_id:integer
*user_id:integer
*location

### Stat
    - belongs to user
    - belongs to exercise
*user_id:integer
*exercise_id:integer
*weight:integer, default null
*time:integer, default null
*comment

### Exercise
    -has many stats
    - has many exercise_workouts
    - has many workouts through exercise_workouts
*name
*description
*video
*category

### Exercise_Workout
    - belongs to exercise
    - belongs to workout
*exercise_id:integer
*workout_id:integer
*reps:integer
*sets:integer

### Workout
    - belongs to user
    - has many users through appointments
    - has many appointments
    - has many exercise_workouts
    - has many exercises through exercise_workouts
*title
*user_id:integer

