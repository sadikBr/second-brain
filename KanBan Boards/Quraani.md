---

kanban-plugin: board

---

## Backlog

- [ ] If a chosen reciter does not have an audio for a given surah then don't show the option to play the full surah on the surahs that are not recorded for him
- [ ] Add the printed tajweed mushaf from some other source for warsh
- [ ] **Use Google’s recognition only to follow along, not to judge.** For example, in practice mode the next words could appear as you recite, so you don’t tap. Its “corrections” matter less when it’s only tracking where you are. But it would still miss your mistakes, so it must never look like a checker. I’d only do this if hands-free matters to you.
- [ ] 1. **Memorisation map («خريطة الحفظ»).** All 604 pages coloured by how solid your memorisation is, based on your التسميع results and revision dates. Tap the weakest page to practise it.
	2. **Tap a tajweed colour to learn the rule.** With tajweed colours on, tap a coloured letter to see a short explanation of the rule and hear an example. The app already knows which rule each colour is.
	3. **Warsh–Hafs differences («فروق الروايتين»).** Words where Warsh differs from Hafs, highlighted in the ayah with the Hafs reading beside them. This is helpful if you learned Hafs first, and the app already has both texts aligned ayah by ayah.
	4. **Find an ayah by voice.** Recite a few words, or let it hear a recitation playing nearby, and it opens that ayah. This would reuse the same model as idea 1.
	5. **Recitation playlists («قوائم التلاوة»).** Queue surahs or ranges to play in order, with saved lists like Al-Kahf for Friday, or Al-Baqarah from start to finish across days.
	6. **Share an ayah with its recitation.** Share an ayah as a short clip: the share card you already have, plus the reciter’s audio, ready for a WhatsApp status.
	7. **Offline pack.** One download for the whole printed mushaf and a tafsir, so everything works with no internet, for example while travelling.
- [ ] ai recitation with mistakes highlighting
	
	(impossible to achieve this for warsh at the moment)
	
	#OnHold


## Todo

- [ ] Try to find a tumun per page for warsh if possible from somewhere and give an option to the users, to use that layout for the mushaf pages
- [ ] Check if there are ready printed pages for the thumun per page quran
- [ ] When logging in to another device and I choose to keep what is on the database, the preferences that are saved in supabase are not applied to the current device


## In Progress



## Done

**Complete**
- [x] Keep the screen awake while the app is open
- [x] All the inputs in the application now look left to right, update them to be right to left
- [x] uploading an image does not work
- [x] Creating one of the recurring goals like al kahf every friday causes the app to crash and close
	
	It seems like all the goals make the application crash for some reason
	
	(Maybe just those template are affected!!, this bug is really tricky sometimes it happens sometimes not)
	
	#Bug
- [x] There is some snapping that happens when I click on the reader
	
	#UX
- [x] The bottom tool bar can use a re-design (the next and prev arrows are not useful they should be removed.)
	
	Arrange the buttons on a better way, maybe even change how they work. (do something similar to tarteel)
- [x] the highlight of the dots in the adhkar interface is not looking good
- [x] The text in the button to increase the text size in the adhkar screen does not look correct, it should be centered??
- [x] In the settings page the back button says mushaf but sometimes it does not send the user back to the mushaf, for example if open the settings page from the home
- [x] in the tasmee3 we can remove that kaima I don't think it is useful anymore
- [x] Add qibla direction in the prayer times screen
- [x] Quranpedia has a lot of options for ayah actions. Add all the possible actions to the ayah actions modal
- [x] Add a filter on the index page, to filter meccan/medinan surahs
- [x] The audio for the adhan is not good, search for another source of adhan audio and use it instead of the current one.
	
	I want a rich collection of sounds and takbiirs
- [x] There are a lot of pickers throughout the application.
	
	Try to refactor them into one reusable component
- [x] **Memorisation test («اختبار الحفظ»).** Like a teacher’s exam, drawn from what you’ve memorised: “continue from here”, “what comes before this ayah”, “which surah is this in”. You get a score, and missed places go to revision.
- [x] I want to add an option, instead of doing tasmee3 for myself I would use it to help someone that is trying to memorize so it should not target me as the one doing the tasmee3
- [x] The quran text in the practice view does not match my preferences with tajweed colors and stuff
	
	#UX
- [x] Improve the tasmee3 feature.
	
	add «ما قبلها» as a third mode, add the «في أي سورة؟» question
- [x] Fixing some characters not rendering correctly when using the mashriqi font characters with the riwayat warsh quran text
	
	Mark the maghribi letter style as the default for warsh
- [x] Add thumun per page for riwayat warsh
- [x] Fix settings page layout and UI design
- [x] Check if it is possible to change the warsh quran text font (add an option for warsh to change the look of the characters)
- [x] Maybe add a way to increase the font size in the dhikr card
	
	#UX
- [x] Some adhkar need a little bit of fixing. (e.g. cards that contain quran)
	
	#UI
- [x] the settings page should support swiping right and left to navigate
- [x] I would like to have a sample audio to listen to reciters before choosing one, instead of having to choose go back to the reader and come back again
	
	#UX
- [x] For reciters, give me the option to use ones that recite the whole surah somehow.
	
	Maybe there will be two types of audio, that the user can select, one for ayah by ayah and the other will be the whole surah.
- [x] Would be good if I can swipe left and right to navigate the home screen tabs
- [x] Extract a prayer times settings section and improve the prayers screen.
	
	I would like to be able to see upcoming and previous weeks's prayer times
- [x] the home page is going to get very messy with the addition of more screens and features. We need to think of a better way to display those information
	
	#UI
- [x] the permanent prayer times notification looks flipped on my phone, and it looks also fully round on the corners.
	
	fix this!
- [x] The athan full page screen is ugly as hell.
	
	Make it look better, use some background image showing the haram al makki or something (mosque...)
	
	Also, one good feature would be to let me design how that page should look.
- [x] Add an option to always show a notification on the phone that displays the prayer times.
	
	Make sure to design it to look very pretty
- [x] Add prayers reminder with athan and everything
	
	#Feature
- [x] If the tool bars are showing and I swipe to another page, the buttons on the tool bars no longer work and I should hide the tool bars and show them again for the buttons to work (this is annoying)
	
	#Bug
- [x] I am not able to use the keyboard on some inputs. Once it shows it disappears again
	
	#Bug
- [x] Implement a practice sessions feature.
	
	the user can choose whether they want to practice their memorized quran, a custom range, surah...
	
	then they should get, the first ayah or some words and they should continue reciting from memory
- [x] In the quick navigation, instead of asking for surah number. Give a select with all the available surah names.
- [x] Add support for adhkar
- [x] Revise the application's arabic wording.
	
	It is not good at the moment. Make it sound like a native arabic person wrote it, not like some one to one translations from english
- [x] We have text strings thrown all around the application.
	
	We can refactor that into files, to lay the foundation for introducing internationalization later.
- [x] Make the ayah card look better
- [x] the hamburger menu should not show all of those cards, as they are not necessary and we already have access to all of that from the top and bottom tool bars.
	
	Also, I don't like how it look now.
	Can you please think of a clever way to make it better instead of showing a bunch of clickable cards.
- [x] reduce the roundness, I don't want the app to have so much round corners.
	
	Also, do a pass on the app and improve the used design, make it look modern and very appealing to users to user and enjoy
- [x] Creating a memorization goal with some memorized quran set throws an error
- [x] In the memorized quran selection, I would like to have hizbs in there also




%% kanban:settings
```
{"kanban-plugin":"board","list-collapse":[false,false,false,false]}
```
%%