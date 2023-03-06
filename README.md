# web-development
js,css, html
The HTML structure is composed of three different elements: a div.cd-schedule__timeline for the events timeline(09:00, 09:30, ..), a div.cd-schedule__events wrapping the events list and a div.cd-schedule-modal for the modal window used to provide more details about the selected event.
On small devices (window width smaller than 800px) and if JavaScript is disabed, all the events inside a .cd-schedule__group are lined up horizontally: we set a display: flex to the .cd-schedule__group > ul element and an overflow-x: scroll to make the events scrollable.As for the .cd-schedule-modal, the opening/closing animation is created using JavaScript combined with CSS Transitions and Transformations (more in the Events handling section).
Events handling: To implement this event schedule, we created a ScheduleTemplate object and used the scheduleReset() and initEvents() functions to init the schedule and attach event handlers to the proper elements.
When the user selects an event, Ajax is used to load the content of the event just selected (its data-content is used to determine the file content to be loaded).
In addition to that, on big devices, the .cd-schedule-modal is animated to show the event content.
First, the .cd-schedule-modal is placed on top of the selected event and its height and width are changed to be equal to the ones of the selected event; then the .cd-schedule-modal__header-bg and .cd-schedule-modal__body-bg elements are scaled up to create the morphing animation; at the end of this animation, the modal content is revealed.


-Maithri S
