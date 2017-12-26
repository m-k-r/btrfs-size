unlike zfs, btrfs has no bult-in tool to show the space used by each subvolume

This tool geathers informations from different btrfs tools and merge all snapshots that belong to the same snapshot.

**At least in theory.** If the parent of a snapshot is deleted it doesn't get linked with the parent of the parent. So the parent of the parent and this parents will be displayed als a unrelated subvolume. This is a shortcoming of the current btrfs-tools.

The output can be customized to show only the subvolumes or with their snapshots and to sort them according to name, snapshot number, size total and size exclusively by each snapshot.

### usage

btrfs-size -p $PATH -s (show snapshots) -r $RESTRICTION -l $LISTOPTION
