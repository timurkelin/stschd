# Evaluation of the Static Scheduler
SystemC Simulator of the Static Scheduler

Timing, timing hierarchy, time tick issues a named event ot a scheduler <br />
```
frames: 
[{ "name": <this_frame_string_name>, 
   "seq":  [{"delay":<time+unit>}, OR
            {"event":<event_string_name>}, OR
            {"frame":<another_frame_string_name>}, 
            .....
           ]
 },          
.....
]

generate:
[{ "name": <gen_string_name>, 
   "seq":  [{"delay":<time+unit>}, OR
            {"event":<event_string_name>}, OR
            {"frame":<frame_string_name>}, OR
            .....
           ]
 },          
.....
]
```
Tasks, triggering event (regex), task dependencies, task durations, list of the executors for the task in the form: (resA | resB | ... ) & ( resX | resY ) & resZ <br />
Executors. each executor can use a part of a common pool <br />
common pools: if requested common resource exceeds the volume of the common pool then all executors slow down (DVFS, througput) <br />

