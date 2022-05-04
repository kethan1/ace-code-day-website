---
title: "Schedule"
---

<h1 class="text-outline-shadow before:content-['Schedule']">Schedule</h1>

ACE Code Day is divided into 3 hour-long workshop tracks. You may sign up for however many tracks as you'd like, but **you may only sign up for a single workshop per track**.

For hackathon participants, the 3rd workshop track is reserved as a hackathon work period and you will not be able to attend any 3rd track ACE Code Day workshops if you choose to participate in the hackathon.

Refer to the schedules below for the specific timings of workshop tracks and the hackathon.

<div class="flex flex-col space-y-3 lg:space-y-0 lg:flex-row lg:space-x-4 lg:items-start">

<Schedule title="Workshop Schedule" class="flex-1" :data="[
    { time: '12:30 to 1:30 PM', title: 'Workshop Check-in', description: '(For workshop teachers)' },
    { time: '1:30 PM to 2:00 PM', title: 'Opening Ceremony' },
    { time: '2:00 PM to 3:00 PM', title: 'Workshop Track 1' },
    { time: '3:00 PM to 3:15 PM', title: 'Break' },
    { time: '3:15 PM to 4:15 PM', title: 'Workshop Track 2' },
    { time: '4:15 PM to 4:30 PM', title: 'Break' },
    { time: '4:30 PM to 5:30 PM', title: 'Workshop Track 3', description: '(Work period for students in the hackathon)' },
    { time: '5:30 PM to 6:30 PM', title: 'Dinner' },
]"></Schedule>

<Schedule title="Hackathon Schedule" class="flex-1" :data="[
    { time: '8:00 AM to 9:00 AM', title: 'Hackathon Check-in' },
    { time: '9:00 AM to 6:00 PM', title: 'Hackathon Work' },
    { time: '7:00 PM to 8:00 PM', title: 'Hackathon Award Ceremony' },
]"></Schedule>
</div>