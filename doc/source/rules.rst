==========
Game rules
==========

Each team owns two Bots, and each Bot is controlled by a Player. Bots in
their homezone are called "Destroyers", and "Harvesters" when in the
enemy’s homezone.

**Eating**: when a Bot eats a food pellet, the food is permanently removed and
*one point* is scored for that Bot’s team.

**Eating another Bot**: when a Bot is eaten by an opposing destroyer, it
returns to its starting position (as a harvester). *5 points*
are awarded for eating an opponent.

**Observations**: Bots can only observe an opponent’s exact position, if they
or their teammate are within 5 squares of the opponent bot (in Manhattan
distance, see :ref:`maze_distances`). If they are further away, the opponent’s
positions are noised (see :ref:`noisy_positions`).

**Timeout**: each Player only has 3 seconds to return a valid move. If it
doesn’t return in time or if it doesn’t return a move that is legal, then a
random move is executed and all later return values are discarded. 5 timeouts
and you’re out!

**End of game**: the game ends when either one team eats all of the opponents’
food pellets, or after 300 rounds.

**Winning**: the team with more points at the end of the game wins, regardless
of which team ate all the food pellets!
