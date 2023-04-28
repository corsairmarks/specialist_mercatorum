# Overview

This mod adds a brand-new specialist subject type - the Mercatorum! As an overlord, you can now charter one of your subjects as your very own megacorporation. Unlike other other specialist subject types, overlords are limited to a maximum of one Mercatorum, however that Mercatorum subject does not count for purposes of Divided Patronage (the loyalty penalty for having multiple subjects).

# Changes

Mercatorum subjects are focused on boosting the trade economy of their overlord and fellow subjects, at the cost for their own infrastructure resource (food, minerals, and alloys) production and military capacity. They are converted to have the Corporate authority as part of the specialization process (and are forced to keep it as long as they are aMercatorum specialist, although they may reform their civics). They gain bonuses to energy and consumer goods production as well as trade production, collection, and protection. Commercial Pacts between a Mercatorum and their overlord or a fellow subject of the same overlord do not cost influence. Furthermore, each branch office owned by a Mercatorum on a planet owned by their overlord or a fellow subject generates a bonus of three Unity.

As the majority shareholder, the overlord of a Mercatorum can expect semi-regular dividends based on the monthly income and specialist tier of their subject. These dividends are generated through "investment activity" and do not impact the resource stockpiles of the Mercatorum. By default, the subject is entitled to 15% of dividends as their commission - however, that percentage is negotiable as part of the subject agreement. Mercatorum subjects might not be able to pay dividends if they are suffering a resource deficit - as their financier, their overlord has the option to make a resource payment to end a resource shortage situation. Beware - allowing your Mercatorum subject to default will have a ripple effect on your economy!

Also included are features similar to the other specialist subject types: special trade actions, specialist leader traits, and an overlord holding (the Mercatorum Corporate Headquarters). Mercatorum subjects also gain access to a new branch office building (the Mercatorum National Headquarters) which it can construct on one branch office in their overlord and once per fellow subject. Both buildings provide a boost to the local economy of their host planets, and the branch office building is accompanied by a small boost across the entire host empire. The buildings provide overlord-centric Executives/Manager jobs that generate unity for the overlord empire while generating trade value and amenities for the subject as well as inspire improved monthly loyalty towards the subjects' common overlord.

Beyond the new specialist subject type, there are also three new hyper relay network edicts: Networked Trade Routes (trade value), Networked Customs Patrols (trade protection range), and Networked Customs Checkpoints (trade protection). These are available to any non-gestalt empire with the appropriate technologies.

## Compatibility

Built for Stellaris version 3.7 "Canis Minor." Not compatible with achievements.

Adding the Mercatorum specialist subject type required modifying a few built-in game objects in order to support them as a new specialist, and some to support their unique functionality. The most notable overwrites are a few diplomatic actions (Propose Commercial Pact, Break Commercial Pact, Release Subject, Request Independence), some subject agreement term values (Integration Permitted, Limited Diplomacy, Expansion Prohibited, Basic Resource Subsidies, Advanced Resource Subsidies), and the diplomatic economy file (to make Commercial Pacts free between Mercatorum subjects and their overlord and fellow subjects). Also included is a scripted trigger related to specialist leader traits, two scripted effects related to Divided Patronage and economic default, and the Independence war goal.

What this means for you, the player, is that this mod may conflict with other mods that make changes to diplomatic actions, subject agreement term values, of the diplomatic economy file. This mod has built-in compatibility for [Civic: Organic Zealots](https://steamcommunity.com/sharedfiles/filedetails/?id=2920668465) - both mods affect overlapping diplomatic actions and the Independence war goal.

### When to Install

This mod can be safely added to your savegame after the game has started. Because it adds gameplay objects (most notably things related to the Mercatorum subject specialization), it should not be removed during a game.

### Recommended Companion Mods

* [Colony Designation: Ecumenopolis Commercial](https://steamcommunity.com/sharedfiles/filedetails/?id=2597129991) adds commercial districts to ecumenopolis planets, to be further boosted by your Mercatorum subject
* [Enhanced Trade Districts and Designations](https://steamcommunity.com/sharedfiles/filedetails/?id=2641081470) enhances existing trade districts and colony designations - more jobs for more trade

## Known Issues

Overriding many types of game objects causes the game to log errors noting each override. Expect to see thirteen lines in the error.log file like these:

```
[00:12:20][game_singleobjectdatabase.h:165]: Object with key: action_form_commercial_pact already exists, using the one at  file: common/diplomatic_actions/specialist_mercatorum_diplomatic_actions.txt line: 4
[00:12:20][game_singleobjectdatabase.h:165]: Object with key: action_break_commercial_pact already exists, using the one at  file: common/diplomatic_actions/specialist_mercatorum_diplomatic_actions.txt line: 199
[00:12:20][game_singleobjectdatabase.h:165]: Object with key: has_specialist_subject_leader_trait already exists, using the one at  file: common/scripted_triggers/10_specialist_mercatorum_scripted_trigger_overrides.txt line: 3
[00:12:20][game_singleobjectdatabase.h:165]: Object with key: refresh_subject_count_loyalty_penalty already exists, using the one at  file: common/scripted_effects/specialist_mercatorum_overlord_scripted_effect_overrides.txt line: 2
[00:12:20][game_singleobjectdatabase.h:165]: Object with key: country_defaulted_effect already exists, using the one at  file: common/scripted_effects/specialist_mercatorum_scripted_effect_overrides.txt line: 6
[00:12:23][eventmanager.cpp:369]: an event with id [origin.5705] already exists!  file: events/origin_events_3.txt line: 1651
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: subject_can_be_integrated already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 37
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: subject_can_not_do_diplomacy already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 91
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: subject_cannot_expand already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 138
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: resource_subsidies_basic already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 200
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: resource_subsidies_advanced already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 259
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: resource_subsidies_research already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 311
[00:12:25][game_singleobjectdatabase.h:165]: Object with key: resource_subsidies_strategic already exists, using the one at  file: common/agreement_term_values/specialist_mercatorum_agreement_term_value_overrides.txt line: 380
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Improve planet modifier cleanup when an overlord loses its Mercatorum subject
* 1.0.2 Bugfixes
    * Resolve incorrect text on the event for overlords that notifies them when a Mercatorum subject defaults on a deficit (special thanks to [Sel Und Irae](https://steamcommunity.com/profiles/76561198202023932))
    * Ensure that the opinion bonus for bailing out a Mercatorum subject decays
    * Ensure the Mercatorum Dividends situation cannot incorrectly end during a deficit
    * Upon conversion, Mercatorum subjects adopt the Mercantile diplomatic stance
* 1.1.0 Imperial Vassals can choose to begin the game as a Mercatorum
    * Only one Imperial Vassal can choose to become a Mercatorum
    * Fix the title of the Overlord Special Dividends event which incorrectly referred to the Overlord itself
    * Refactor economic subsidies for Mercatora so that they do not break normal Basic and Advanced subsidies for other subjects - however, you will need to renegotiate the agreement with your Mercatorum to re-establish commercial or infrastructure taxes/subsidies (they are no longer resource sliders and appear near the bottom of agreement terms)
    * Significantly simplify event code for enforcing the limit of one Mercatorum subject
    * Mercatorum HQ buildings (both branch office and holding) give +1 envoys to the building owner (the Mercatorum or Overlord respectively)
    * Mercatora now have a narrower range of Research and Strategic taxes/subsidies

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/specialist_mercatorum)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property. That will ensure the game can see the files, and also that CWTools will parse them. Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.