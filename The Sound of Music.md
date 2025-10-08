# Discription

🗼OSINT pt2: citadweller had a newfound interest in tracking the music they last listened to and posting ratings of new albums on various online platforms.

The flag is hidden in these digital footprints across music platforms and split into three segments. You will need to find all three to uncover the complete code and move on to the next floor.

# My team's solve
- The description clearly says that `citadweller` has a new found interest in music and reviewng music, so we just had to figure out which sites offer reviewing music, and which one of those does `citadweller` have an account on.
- The flag is hidden in these digital footprints, divided in three segments, across 3 platforms.
- First we stumbled upon `RYM(Rate your music)` which had a user named `citadweller`, which apparently had the second part of the flag, the middle part of the flag was `_n_started_shar1ng_st0r1es`.
- `RYM` account also had a tinyurl link, in the bio, which was the spotify under the name `citadweller`.
- The third part was in the description of a public spotify playlist, by citadweller, which was `_n_then_they_were_n0where_t0_be_f0und}`.
- Then we found the first part on the shoutbox of user `citadweler`, on `last.fm`, which was `citadel{c0mputers_st0pped_exchang1ng_1nf0rmat10n`.

**Flag : ** `citadel{c0mputers_st0pped_exchang1ng_1nf0rmat10n_n_started_shar1ng_st0r1es_n_then_they_were_n0where_t0_be_f0und}`
