Title: What is RAID?
Author: Bryce McNab
Date: 8/23/2017
Status: published

Oh no! Your hard drive crashed. After pulling a long night of data recovery, you finally think to yourself "how can I stop this from happening again?" 

Well, it's about time you did a little research.

# Backup

First and foremost, for the love of god, please get a backup running on all of your computers. The simplist, and cheapest is to buy an external hard drive and plug it in, set up your favorite backup software to copy everything you have to the external drive and you're good to go.

I would highly recommend that you do the above and also get an online backup solution that you can trust in case your computer is stolen, or is destroyed in a house fire. I personally recommend [Backblaze](https://www.backblaze.com) for any Windows/Mac users out there. I don't know of a good offsite, online linux backup solution, but that's because I live dangerously on the edge.

# RAID

Generally speaking RAID (*R*edundant *A*rray of *I*ndependent/*I*nexpensive *D*isks) is only a solution for those desktop users and server masteres among us. Very simply put RAID combines multiple disks to allow redundancy, so if one drive dies, not only is your data still available and there is 0 downtime, but you can replace the bad disk and it will rebuild itself. There are multiple RAID array types:

## RAID0

Adds absolutely no redundancy, but offers scalable disk size and speed. RAID 0 works buy "striping" multiple disks, of the same size, into one large volume. For example, a RAID0 of 2x2TB (TeraByte=1000GB) would make a single volume of 4TB. But if you lose either disk, all of your data is gone. The biggest benefit here is speed. You're theoretical throughput is 2 times that of a single disk, or n times for n disks.

## RAID1

The simplest of the RAIDS for redundancy, this configuration allows 2 disks of the same size to be mirrored. Taking the above example of 2x2TB disks, in a RAID1 configuration, you would see a 2TB volume. However, if either of the disks dies or has any fault, you would have no downtime, and could replce the dead drive to rebuild the array. 

> Theoretical maximum loss: 50%

> Number of disks: 2

## RAID 5

This configuration allows for much larger volume sizes, with a good amount of redundancy. RAID5 starts at 3 disks minumum, and the rule of thumb is you lose 1 disks worth of space for the parity. The parity allows the RAID to be rebuilt when a drive dies and is replaced. So, to expand the running example, if we had 3x2TB in a RAID5 configuration, you would walk away with a 4TB volume.

> Theoretical maximum loss: 33%

> Number of disks: 3 - ∞

## RAID 6

This configuration isn't used much, from what I have seen. It is the same as a RAID5, but with 2 disks dedicated to parity. This makes the whole array more fault tolerant, but more expensive in that the minimum set of drives is increased to 4 with no free space boost.

> Theoretical max loss: 50%

> Number of disks: 4 - ∞

## Combining RAIDS

RAID configurations can be combined (from what I can tell infinitely). The most popular is the RAID10

### RAID10

RAID10 is RAID1+0. You would first create 2 RAID1 arrays and set up a RAID0 on top of them, giving you the redundancy of RAID1, and the performance and space boost of RAID 0.

> Theoretical max loss: 50%

> Number of disks: 4 - ∞ (in pairs of 2)

### Other RAID

Other combined RAID combos are up to your imagination. Try out a RAID50, RAID51, RAID65, any of these are valid RAID configurations, if not necessarily good ideas.

# In the end

...Does it really matter? If I were a desktop user (I am strictly a laptop user), I would have RAID set up. This blog is hosted on a server, that doesn't have RAID capability (yet) but I am working on that. So if you can, I highly recommend it. But as a warning, RAID is not, in any way, a replacement for a backup. Please make sure, RAID or no, you have a solid, tested backup in place. You want to make sure your backup is tested, or else you just have Schrödinger's backup.
