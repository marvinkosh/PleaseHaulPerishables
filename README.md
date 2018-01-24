# PleaseHaulPerishables
Adds new WorkGivers for hauling, which prioritise hauling perishables or food over non-perishables. Items will be considered perishable if they would rot in less than a year or deteriorate to zero hitpoints in ten days or less.

Rain, which causes higher deterioration rates, will be taken into account.

Perishable items will only be given priority for hauling if they are not under a roof or (in the case of rottable things) can be hauled somewhere colder.

A check is made to see if the perishable has a large enough stack size. Things which have a maximum stack size of 1 (weapons and apparel for example) pass automatically. Other perishables must have a stack count of 40% of the maximum stack count for that kind of item. For example, a stack of 30 potatoes would be a large enough stack size, but 29 would not be. The perishable can still pass the check if there are other perishables of the same type nearby, or if it would deteriorate to zero hitpoints in ten days or less.

Food will also be hauled if it needs to go from low to high priority storage. Items will be considered food if a colonist would be happy to eat them as-is, or if an animal of the colony could eat them. For animal food, consideration will be given to whether moving the food would make it accessible to the animal.

A new general hauling routine prefers valuable items like silver or big stacks of items (60% of max stack size) for hauling, regardless of whether they are perishable or not. It will look at a square grid and a plus-shaped grid of cells to see if a big stack of the same type of item could be made. The normal general hauling routine picks up any leftovers.
