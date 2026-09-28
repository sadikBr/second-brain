---

kanban-plugin: board

---

## Backlog

- [ ] For the personal practice view, I should be able to set which days of the week are for memorization and which one are for practicing what is already memorized.
- [ ] **Riwayah-aware reading progress**
	
	Keep separate reading positions for Hafs and Warsh. Switching riwayah would return users to the correct page and ayah instead of reusing an incompatible location. This is relatively small and prevents another class of numbering bugs.
- [ ] **Push Notifications??**
	
	Reminders, when about to loose a streak....
- [ ] **Keep the screen awake**
	
	Add a reader preference that prevents the device from sleeping during active reading. Very small implementation effort and genuinely useful on phones.
- [ ] **Fix the warsh audio for ayah by ayah**
	
	Maybe use the Quranpedia api for this??
- [ ] **Ayah repetition controls**
	
	Let users repeat one ayah or a selected range 3, 5, 10 times, with an optional pause between repetitions. Excellent for memorization and pronunciation practice.


## Todo

- [ ] Add quran memorization completion tracking for every user, track hizbs completed. So the user will have a goal to reach 60/60 which is the whole quran and make it look interesting.
- [ ] **Shareable ayah cards**
	
	Generate attractive cards containing the ayah, surah reference, translation, and optional app branding. Users could copy or download them for sharing.


## Done

**Complete**
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