# Changelog
## 3.0.2 (2022-01-10)
### Fix
- "back" in "Follow Back" is not uppercase anymore
### Performance improvements
- better handling for not loaded profiles
## 3.0.1 (2022-01-05)
### Fix
- missing argument in analytics report

### Others
- new logo for the readme.md
- added some useful info for the user

## 3.0.0 (2022-01-05)
### New Features

- use the cloned app instead the official, if the dialog box get displayed (this is currently supporter for MIUI devices)
- new filter options: *interact_if_public* and *interact_if_private*
- *interact_only_private* has been removed, delete it from your filters.yml

### Performance improvements

- limit check was wrong in interact_blogger plugin
- feed job was ignoring limits
- don't throw an error if config files \*.yaml instead of \*.yml are used
- likes_limit was referring to total_likes_limit and not current_likes_limit (that caused an error if you specify an interval)

### Performance improvements

- jobs have been split in "active-" and "unfollow-" jobs. That means, for example, that the bot won't stop the activity if it reached the likes limit and you scheduled the unfollow.
- you can pass how many users have to be processed when working with \*.text (unfollow-from-list and interact-from-list)
- bot flow improved
- feed job improvements
- looking for description improvements
- better handle of empty biographies
- showing session ending conditions at bot start
- countdown before starting, so you can check that everything is ok (filters and ending conditions)
- before starting, the bot will tell you the filters you are going to use (there is no spell check there, if you wrote them wrong they will be displayed there but not get considered)
- disable head notifications while the bot is running
- removed unnecessary argument in check_limit function
- removed some unnecessary classes in story view
- move Filter instance outside of plugins
## 2.10.6 (2021-11-24)

#### Performance improvements

* the parsing of the number of posts / followers / following could fail for someone

Full set of changes: [`2.10.4...2.10.6`](https://github.com/GramAddict/bot/compare/2.10.4...2.10.6)
## 2.10.5 (2021-11-18)

#### Fixes

* 'NoneType' object has no attribute '_is_post_liked'
#### Others

* removed a typo

Full set of changes: [`2.10.4...2.10.5`](https://github.com/GramAddict/bot/compare/2.10.4...2.10.5)

## 2.10.4 (2021-11-08)

#### Fixes

* scraped is now counted as successful interaction

Full set of changes: [`2.10.3...2.10.4`](https://github.com/GramAddict/bot/compare/2.10.3...2.10.4)

## 2.10.3 (2021-11-06)

#### Fixes

* the bot did not inform about the skip in case of the filter on mutual friends or on the link in bio
* false positive for link check in bio

Full set of changes: [`2.10.2...2.10.3`](https://github.com/GramAddict/bot/compare/2.10.2...2.10.3)

## 2.10.2 (2021-11-06)

#### Fixes

* link in bio object exists even if it's empty

Full set of changes: [`2.10.1...2.10.2`](https://github.com/GramAddict/bot/compare/2.10.1...2.10.2)

## 2.10.1 (2021-10-31)

#### Fixes

* someone in the world has a " ’ " as thousands separator instead of " , "

Full set of changes: [`2.10.0...2.10.1`](https://github.com/GramAddict/bot/compare/2.10.0...2.10.1)

## 2.10.0 (2021-10-27)

#### New Features

* you can control if comment carousels
* support for connect_adb_wifi uia2 method
* support for watching videos and check for already liked posts
#### Fixes

* trying to close the android pop-up if ig crashes
* looking for the like button on the following video instead of the one being played
* comment fails on some media types
* checking media_type could fail
* empty files in unfollow from list job
* unfollow from list loop
* removed unexpected keyword argument in getFollowinCount method
* method connect_adb_wifi contained some errors
* was being imported nan by numpy instead of the math module
* ig is not opened but the bot tries to do operations
#### Performance improvements

* video recording
* posts-from-file job improved and fixed
* little improvements to the module mode

Full set of changes: [`2.9.2...2.10.0`](https://github.com/GramAddict/bot/compare/2.9.2...2.10.0)

## 2.9.2 (2021-10-06)

#### Fixes

* other incompatibilities in the latest IG version

Full set of changes: [`2.9.1...2.9.2`](https://github.com/GramAddict/bot/compare/2.9.1...2.9.2)

## 2.9.1 (2021-10-06)

#### New Features

* module version thanks to @patbengr
* if a username in *.txt file is not found, it will be appended to a *_not_found.txt
* from now you can customize the session ending conditions
#### Fixes

* compatibility with IG: 208.0.0.32.135
* cannot check the language of Ig if not at the top of the account
* handle an exception in case you start the bot without specifying the config file
* it could happen that you are not at the top of your main profile in some circumstances
#### Performance improvements

* clean code for open and close ig

Full set of changes: [`2.9.0...2.9.1`](https://github.com/GramAddict/bot/compare/2.9.0...2.9.1)

## 2.9.0 (2021-08-25)

#### New Features

* new argument to control how many skips in jobs with posts (e.g.: hashtag-post-top) are allowed before moving to another source / job
* new job to unfollow people who are following you
* new filter for skipping accounts with banned biography language
#### Performance improvements

* improved readability of the code and correct some typos
* moving sibling folders of run.py will no longer executed automatically

Full set of changes: [`2.8.0...2.9.0`](https://github.com/GramAddict/bot/compare/2.8.0...2.9.0)

## 2.8.0 (2021-08-04)

#### New Features

* new filters: 'skip_if_link_in_bio: true/false' and 'mutual_friends: a_number' min count
* new feature added: pre and post script execution

Full set of changes: [`2.7.7...2.8.0`](https://github.com/GramAddict/bot/compare/2.7.7...2.8.0)

## 2.7.7 (2021-08-03)

#### Fixes

* place first post not found [#208](https://github.com/GramAddict/bot/issues/208)
* replace detect-block with disable-block-detection
#### Performance improvements

* removed unneeded class and sort imports

Full set of changes: [`2.7.6...2.7.7`](https://github.com/GramAddict/bot/compare/2.7.6...2.7.7)

## 2.7.6 (2021-07-31)

#### Fixes

* missing resource id for sorting following list

Full set of changes: [`2.7.5...2.7.6`](https://github.com/GramAddict/bot/compare/2.7.5...2.7.6)

## 2.7.5 (2021-07-30)

#### New Features

* new argument "detect_block: true/false" to enable/ disable block check after every action
#### Fixes

* a better way to sort following list [#207](https://github.com/GramAddict/bot/issues/207)
#### Performance improvements

* add debug info for swipes
#### Refactorings

* sort imports

Full set of changes: [`2.7.4...2.7.5`](https://github.com/GramAddict/bot/compare/2.7.4...2.7.5)

## 2.7.4 (2021-07-25)

#### Fixes

* support for Ig v. 197.0.0.26.119

Full set of changes: [`2.7.3...2.7.4`](https://github.com/GramAddict/bot/compare/2.7.3...2.7.4)

## 2.7.3 (2021-07-14)

#### Fixes

* sometimes the bot press on 'Switch IME' instead of open your profile
* automatic change in English locale stopped working

Full set of changes: [`2.7.2...2.7.3`](https://github.com/GramAddict/bot/compare/2.7.2...2.7.3)

## 2.7.2 (2021-07-14)

#### Fixes

* bug in open post container when someone in your 'following list' has also liked the post
#### Performance improvements

* lowered a little bit the swipe up in sorting `Following accounts`

Full set of changes: [`2.7.1...2.7.2`](https://github.com/GramAddict/bot/compare/2.7.1...2.7.2)

## 2.7.1 (2021-07-13)

#### New Features

* you can dump your current screen with that command `gramaddict dump`
#### Performance improvements

* we don't need to click on a obj if we are already on it

Full set of changes: [`2.7.0...2.7.1`](https://github.com/GramAddict/bot/compare/2.7.0...2.7.1)

## 2.7.0 (2021-07-12)

#### New Features

* you can use spintax for comments and PM from now
#### Fixes

* forgot to remove 'time_left' when calling print_telegram_reports at the end of all sessions
* in config-examples forgot 'comment_blogger' and fix typo in 'comment_blogger_following'

Full set of changes: [`2.6.5...2.7.0`](https://github.com/GramAddict/bot/compare/2.6.5...2.7.0)

## 2.6.5 (2021-07-06)

#### Fixes

* the count of items in the carousels stopped at the first match
* from now on, every type of interaction is counted as successful and not just likes

Full set of changes: [`2.6.4...2.6.5`](https://github.com/GramAddict/bot/compare/2.6.4...2.6.5)

## 2.6.4 (2021-07-01)

#### Fixes

* telegram-reports when out of working hours crashed
#### Performance improvements

* improve update checking
#### Docs

* text improvement and typo corrections

Full set of changes: [`2.6.3...2.6.4`](https://github.com/GramAddict/bot/compare/2.6.3...2.6.4)

## 2.6.3 (2021-06-26)

#### Fixes

* time left in telegram-reports was wrong

Full set of changes: [`2.6.2...2.6.3`](https://github.com/GramAddict/bot/compare/2.6.2...2.6.3)

## 2.6.2 (2021-06-25)

#### Fixes

* there was a problem with likers list
* there was a problem with the way I moved the reports at the end of sessions
#### Performance improvements

* the bot can recognize hashtag suggestions in feed
* telegram-reports improved
#### Docs

* typo in readme

Full set of changes: [`2.6.1...2.6.2`](https://github.com/GramAddict/bot/compare/2.6.1...2.6.2)

## 2.6.1 (2021-06-24)

#### Performance improvements

* we can use an entry point from now
#### Docs

* correct a typo in telegram-reports
* improved the README

Full set of changes: [`2.6.0...2.6.1`](https://github.com/GramAddict/bot/compare/2.6.0...2.6.1)

## 2.6.0 (2021-06-24)

#### New Features

* you can run GramAddict from the command line for initializing your account folder with all the files needed
* add support for allow re-interaction after a given amount of hours
#### Fixes

* too many `filters.yml is not loaded`
* telegram-reports typo in report
* add support for viewers count where likes count is missing
* browse the carousel could fail in some circumstances
#### Docs

* completely rewrote the README.md
#### Others

* donation alert when bot stops by pressing CTRL+C
