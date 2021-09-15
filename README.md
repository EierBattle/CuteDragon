Start here:
- [Example of a round](https://github.com/EierBattle/CuteDragon/blob/main/Battle_Alpha.ipynb)
- [Fully Functional ReadMe](https://hackmd.io/5ZSoPyVNRdejWNkfEhMAAA?view)
- [Code in progress for on Word2Vec NPC interactions](https://github.com/EierBattle/CuteDragon/blob/main/word2vec.ipynb)

# Battle Alpha Ver. 0.1

![](https://i.imgur.com/BFl5kyB.png)


## [Whiteboard Sketch Link ](https://expl.ai/PMDKNHBV)

### :thought_balloon: Overall game concept

Co-op party Slay the Spire with DnD elements for non-combat. Players must plan their turns together to succeed.

<!--### Explanation video
{%youtube jrGuvjjH0n8%}-->

## :sunrise_over_mountains: Gameflow

1. Players select class (starting deck)
  - One Combat
    - Barbarian
    - Mage
    - Rogue
    - Druid
  - One Social
    - Charmer
    - Logician
    - Deceiver
    - Saint
3. Friendly area with NPCs to upgrade and modify deck
4. Dungeon
    - Small mobs (no heal / break between)
    - Boss
6. Repeat 2&3 n times
7. Final boss (no mobs)

## :crossed_swords: Combat flow
* ONLY ACCEPT CHANGES IF THEY IMPROVE OVERALL DAMAGE!*
- each player must choose 3 cards to lay down and then they are resolved in orseder  
  - Play area in the center is always (2x number of players)-1
  - playwrs can play between 1-3 cards
n = num players
```flow
st=>start: Player Turn

op1=>operation: Discard hand &
Draw Cards (5)
op2=>operation: Players
Play Cards
Simultaneously into the
**Play Area**
(~30secs)
monster_attack=>operation: Monster Attack!
(30secs)

cond=>condition: Monster
defeated?
e=>end
monster_attack
st->op1->op2->cond
cond(yes)->e
cond(no)->op1

```
:::info
After players die, remaining players fight on, getting "enraged" by their death.
:::



### :memo: Brainstorming

- DM can add cards to players decks (like curses) that stay temporary
- Players can create their own cards by infusing raw ingredients


## Cards:
First few fights are easy but may cause some permanent dmg if not perfected like in slay the spire

- Barbarian
	- [Axe](https://cdn11.bigcommerce.com/s-0kvv9/images/stencil/1280x1280/products/287262/403630/transformerstcgwave1energonaxe__08679.1549921215.jpg?c=2)
	    - 2 dmg to two
	- Combine: Halve
	  - Split the ranged card before this one into 2 x 75% versions of it (at sepaeate targets if possible)
  - ~Go all out
      - 6dmg (draw 2 cards max next turn)

- Owl Mage
	- Magic Missle (frozen salami attack)
	    - 1 dmg to all
	- Combine: Emblazen
	    - 2x damage to card ahead of this one

- Ranger
	- Arrow
	    - 4 dmg
	- Combine: Hunter's Mark
	    - All cards after me get +1

- Druid
    - Claw
        - 2x2 to one
    - Comb-Attack: Beast Bond
        - + 1 attack instance of 2dmg to the next card
    -  Combine: weaken
       -  all cards after this one du Bonus damage to the target
     - Combine: Roar
         - Empower all other attacks before and after + 1 card_list.index(all_damage_cards)


### Enemies:
- Wolf
    - Attributes
        - He's too quick for anything over 5 dmg
    - Init:
        - Add negative status effects? (Maybe to characters who are afraid of dogs)
    - Attack
        - Bite
            - 3dmg to DM's choice
        - Howl
            - Add two "omg I'm scared" cards to each players deck
    -

### Card types:
- Attack
- Support
- Combination attack
  - Tri-chroma clash: does nothing, or maasove dmg wifh ofjer 2 pieces
- Negative Cards
    - Status effects
    - From enemy / negative RP
    - Permanent / temporary (combat)



### Negative Effect Cards
- Terrified
    - Can't play anything this turn if this is in your hand
- I'm hurt!
    - Play this card and lose 1 health


![permalink setting demo](https://i.imgur.com/PN8TmMI.gif)

ideas for later:
- card effects that effect things next turn (your cards or others)
