This Project is about a Timetable and Room Allocation system for Temasek Polytechnic 
It creates a schedule based on the data , and then optimises room allocation for that schedule.
I used python to create a scheduler thats split as two functions 
- teacher assignment (matches teachers to classes based on balanced working hours) <allocation.py>
- Scheduler (takes the teacher pairings and creates a teacher , class and room schedule )<scheduler.py>

I then wrap the functions as an api using Flask <mpApp.py>
Then i call the api in a html webpage <scheduler.html>

More Information 
teacher assignment checks through the following 
- teaching hours esnuring teachers have balanced and fair workloads
- assigns teachers based on subjects they teach
- assigns teachers based on subjects they have been assigned to teach ( so the teacher can teach the same subjects throughout diff classes )
- max teaching hours

Scheduler 
- sifts though classes , subjects and teacher assignment , finds an available timeslot
- class schedules cannot overlap
- teacher schedules cannot overlap
- room schedules cannot overlap
- lunch hour optimisation (max two hours from 11am-1pm)
- ensures no long breaks between classes 
- accounts for teacher preferences ( teachers can say which dates and times they prefer not to work) <teacherpref.html>
- schedules based on selected dataset (the dataset is created in a powerapps dashboard , that can be uploaded on scheduler.html)
