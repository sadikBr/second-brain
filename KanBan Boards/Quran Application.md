---

kanban-plugin: board

---

## Backlog

- [ ] **Some ideas for app admin**
	
	- Notification health
	- User-reported issues
	- Content correction workflow
	- App announcements
	- Usage overview
	- Service health
	- Feature rollout controls
- [ ] Weekly progress reports for members and admins
- [ ] **role-aware onboarding and empty states**
	
	- **Admin:** a clear path to create the first circle and assign its supervisor.
	- **Supervisor:** guidance to schedule a meeting, invite members, and publish the first assignment.
	- **Member:** an obvious way to join a circle and see what to do next.
	- **Unassigned circle:** clearly explain that it’s waiting for a supervisor, rather than showing inactive controls without context.
- [ ] **Personal calendar integration**
	
	Add halaqah meetings and assignment deadlines to your calendar
- [ ] **Global quick search** 
	
	find a page, saved reflection, dhikr, or assignment from one search box.
- [ ] **Request an assignment adjustment**
	
	Ask for smaller portion or later deadline, with supervisor approval
- [ ] **Weekly planning view**
	
	Distribute tasks across the week and see overloaded days before committing
- [ ] Error monitoring and production health reporting
- [ ] **Personal recurring tasks**
	
	Add your own items, such as studying tafsir every Saturday or something
- [ ] **A catch-up option for missed assignments**
	
	If someone falls behind, let them request a smaller portion or a new deadline. The supervisor can approve it without recreating the assignment.
- [ ] **Similar-ayah study mode — المتشابهات**
	
	Show commonly confused passages side by side, highlighting where their wording differs. This would need carefully reviewed source material.
- [ ] **Personal mistakes notebook**
	
	During a session, the supervisor marks the exact ayah where the learner hesitated or made a mistake. The learner can revisit those passages afterward.
- [ ] **Halaqah resource shelf**
	
	A shared place for lesson documents, useful links, and supervisor guidance
- [ ] **Simple daily plan**
	
	Combine today's wird, revision, adhkar, and assignments into one checklist. Let users choose what appears without turning worship into a competitive score
- [ ] **Post meeting summary for the members**
	
	After a halaqah meeting, each member sees what they recited, the supervisor’s feedback, and what to prepare next.
- [ ] **Revision partners**
	
	Opt in to pairing with another member for mutual practice
- [ ] **Notification inbox**
	
	Revisit reminders and assignments alerts after dismissing the phone notification
- [ ] For the personal practice view, I should be able to set which days of the week are for memorization and which one are for practicing what is already memorized.
- [ ] **Riwayah-aware reading progress**
	
	Keep separate reading positions for Hafs and Warsh. Switching riwayah would return users to the correct page and ayah instead of reusing an incompatible location. This is relatively small and prevents another class of numbering bugs.


## Todo

- [ ] I want to add also a weekly memorization plan along the revision one.
	
	The user can set the amount they want to memorize by week, for example (One quarter hizb per week), and then we can generate this amount split between all their memorization days.
	
	And then we can use this as the source of truth about how to fill the memorization grid. Along with the circle reviews.
- [ ] I would like to add a way for a user to define his revision days and memorization days. The weekly revision plan will then use this instead of requiring the selection of revision days.


## Done

**Complete**
- [x] If the memorization page gets implemented, then we can also implement automatically generating ranges to revise per week for the user given the selected hizbs
- [x] make the memorization tracking page filled in automatically.
	
	When the users first enter this page they will be asked to fill which hizbs they have memorized after that the grid will be locked for manual modification, and it will be filled automatically somehow (We need to figure this out)
- [x] Improve the ayah actions functionality since we are using quranpedia now as our main api and it has a rich actions options ot user
- [x] We need a way to make a group de-activated when we are still preparing the members and stuff.
	
	And once we are ready to start following the group workflow we can enable it.
	
	Maybe this should be done by the app admin?
- [x] Add support for warsh tajweed mushaf
- [x] Bring back the support for tajweed quran for hafs riwayah
- [x] Use the quranpedia for the whole application instead of al quran api for hafs and quranpedia for warsh, this would make the app so much more consistent and also the quranpedia seems to be more feature rich than al quran cloud api
- [x] Make arabic the default language of the UI
- [x] revise the UI and make sure to make it the easiest possible to navigate, I like the look now I just want you to improve it further and also remove any duplicate information or inconsistencies.
- [x] for the halqa, the supervisor is also a normal user, he gets assignments from himself and reviews himself.
	
	This is because I am one of the users of the app and I want to use this with my family members and someone needs to be the reviewer.
	
	Is this a good think, or we should think of another way to handle it.
- [x] Loading ayah actions takes so much time and feels so unresponsive.
	
	Sometime I accidentally click twice thinking that I didn't click it correctly and end up clicking one of the actions on accident
- [x] Improve the audio playback system of the application
- [x] **Ayah repetition controls**
	
	Let users repeat one ayah or a selected range 3, 5, 10 times, with an optional pause between repetitions. Excellent for memorization and pronunciation practice.
- [x] **Fix the warsh audio for ayah by ayah**
	
	Maybe use the Quranpedia api for this??
- [x] **Keep the screen awake & vibration controls**
	
	Add a preference that prevents the device from sleeping during the usage of the app. And maybe another preference to choose how I want the vibration to be.
- [x] **A simple standalone tasbih counter**
	
	For unrestricted personal dhikr, separate from collections with prescribed counts
- [x] run bun lint and bun format for the whole application.
	
	a lot of files will be changed.
- [x] **Better on boarding for new users to show them around the application**
	
	A tutorial like thing that can be dismissed if they don't need it. Or if someone want to see the tutorial we can provide a or a list of things that the user can see the tutorial for
- [x] **Surah opening/ending practice**
	
	test the opening/ending ayahs of a selected surah
- [x] **Random start testing**
	
	Choose your memorized range and receive a random ayah from which to continue, Maybe this can use the hizbs that are checked in the memorization grid. providing a range can be an optional thing
- [x] **Improvements**
	
	- Khatma should not ask users for rest days, normally there is no rest in the daily wird
	- The admin review should have an option for a user that did not complete their assignment (Rejected or something...)
- [x] If a user exits the jitsi meeting without clicking the hang up button and they join again they appear as another user and they appear duplicated in the call and they consume the free quota of jitsi which is not good.
	
	If the user clicks the leave meeting button without hanging the call they should be thrown out of the jitsi call and if they  join again they appear only once and not duplicated.
- [x] The flow now in the application is complicated.
	
	There are a lot of buttons pages and there is no flow between them.
	
	Also every page has a back button to a static page which is not very good, maybe just keep some paths that make sense in the header and remove the navigation links from the page and we can use the built in navigation buttons of the browser or phone.
	
	Please make the flow in the application make sense and try to reduce the number of the clicks that are required by the user to do something.
	
	Also the user menu needs some work to help with the flow of the application and not confuse the users.
- [x] A notification when the admin starts the meeting, clicking the notification would put the user inside the meeting room
- [x] A notification when a review feedback is published
- [x] Meeting agenda and review mode
- [x] Better progress summaries for each member
- [x] Group activity feed showing assignments, submissions, and meetings
- [x] Meeting history and attendance start time and duration
- [x] link this application with zoom, and on group creation whe need to supply when a meeting should be done, we can support having meeting for multiple days of the week and not only a weekly meeting. And we need to provide also the time of the day when the meeting will be had for example:
	
	- Monday 10:00 PM
	- Sunday 11:00 PM
	
	And when the time of the meeting arrives we should have a button that says join meeting (it should open a room in zoom with the admin group as the host if zoom is not available on the user's device send them a toast telling them to install it), and after 3 hours after the meeting time the button should be disabled until next meeting.
- [x] **Push Notifications??**
	
	Reminders, when about to loose a streak....
- [x] **Shareable ayah cards**
	
	Generate attractive cards containing the ayah, surah reference, translation, and optional app branding. Users could copy or download them for sharing.
- [x] Add quran memorization completion tracking for every user, track hizbs completed. So the user will have a goal to reach 60/60 which is the whole quran and make it look interesting.
- [x] **Bookmark collections**
	
	Let users organize saved ayahs into collections such as “Duas,” “Study,” “Memorization,” and “Reflections.” Add simple filtering to the dashboard.
- [x] the quran range selection when practicing should be either by ayah/hiz/quarter/juz
- [x] **Admin review**
	
	- During or after a call with the team members, the admin can mark the assignment
		- Completed
		- Needs more revision
		- Not reviewed
	- Optional short feedback.
	- "Needs more revision" can be carried into the following week.
- [x] **Member's weekly view**
	
	- A clear "This Week" page
	- Each assignment opens directly in the practice reader.
	- The reader keeps the member's checkpoint across sessions
	- The member submits it as "Ready for review"
- [x] **Per member quran assignment**
	
	- Admin selects a member.
	- Chooses memorization or revision.
	- Assigns an exact range from one ayah to another, including ranges across surahs.
	- Sets a due date and optional instructions.
- [x] **Group foundation**
	
	- Create and rename groups
	- Invite members using an invitation system (maybe just a sharable link)
	- Admin and member roles
	- Leave or remove members
- [x] fix the wird card on smaller screens
- [x] the ayah actions in the wird reading interface do not open as model but they open on their page view
- [x] fix the latest read card on smaller screens also (don't like the design) -> this might not be necessary
- [x] wird related pages do not have a loading state
- [x] search does not work for some given arabic sentences
- [x] the home screen should link to the wird page if the user has a wird set and not yet completed for today other wise show the continue reading (page/surah)
- [x] if one ayah is saved when used is using riwayat hafs and they switch to warsh, the saved ayah might be the wrong one as hafs and warsh have different ayah numbering
- [x] Implement practice mode.
	
	User can select a range of the quran that they want to memorize and a range that they want to practice and a dedicated practice view is shown with some dedicated actions.




%% kanban:settings
```
{"kanban-plugin":"board","list-collapse":[false,false,false]}
```
%%