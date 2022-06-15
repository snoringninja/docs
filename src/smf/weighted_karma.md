Karma/Rep Weight System
===
---
###### Current Release: 1.5.1
###### By: [Snoring Ninja](https://snoring.ninja)

---

This mod does a few different things, all of which can be ignored and not enabled:
 
- Provides a weighted system for giving reputation only (taking reputation is always one)
- Limit the amount of karma to go along with weight to prevent outrageous amounts of karma being given
- Option in Admin > Maintenance > Forum Maintenance > Routine to reset all user good karma to a set level while setting negative karma to 0
- Instead of using post count for determining when a user can give reputation, use the user's current reputation to decide
- "Pool" the Karma to prevent any new karma from being added to the game; more information can be found by clicking the help icon next to the option

## Weighted Karma
Weighted karma is a simple idea: take a user's karma and divide by the weight set in the admin panel to give that amount of karma instead of 1. So, if the weight is 15 and a user has 200 karma, they would give 13 karma.  I did not add weight to negative karma, as I am against that.  The weight system comes with two options.

* Weight to divide by
* Max amount that can be given (prevents outrageous amounts)

### Give Karma Based on User Karma, Not Post Count
One gripe I have with SMF's karma is that it relies on post count when determining if a user is able to give karma.  To go around this, I decided that I would rather use a person's karma count to determine whether or not a user is able to give karma.  This works just like it sounds and if the option is enabled it ignores the post count option and uses a user's karma count. The message box can be left blank for a default message if a user without enough karma attempts to give another user karma.  Setting a message here will be shown in place of the default message.

### "Pooled Karma"
"Pooled" Karma System: no new karma is ever introduced into the community after the initial karma is set (i.e. giving certain users enough karma to give karma a few times). This new system works in a manner that when a user gives karma, they also lose the amount they give. For example, if I have 200 karma and it’s weighted by 50 I can give four karma. When I decide to give karma, not only I increase the recipients karma by four, but I also lose four karma for a total of 196 following the giving of karma.

### 2.1 Support
Right now, this won't work on 2.1, mostly because 2.1 did away with the karma system; however, there is a modification someone wrote to port the karma system that you can modify to include the changes from this modification.  I have no plans or interest in combining the two.

This mod is released under the [MIT License](https://opensource.org/licenses/MIT).

Questions/Comments/Concerns:

* Post in the SMF support thread [here](https://www.simplemachines.org/community/index.php?topic=527025.0)
* [GitHub Issue Tracking  ](https://github.com/snoringninja/smf-weighted-karma/issues)

---
### Final Note
This modification is for the Simple Machines Forum Software (SMF) and designed for the 2.0.x branch of the software.  This modification is not, and will not, work on a base install of the 2.1.x branch of the software.  This modification is no longer actively maintained.
