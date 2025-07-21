
# Modified-JaseOwns-Magebot
Modified JaseOwns MageBot that identifies if target has higher MR or Armor and uses the appropriate rotation. Anything balanced will use a default rotation. All adjustable through the init. Don't recommend touching ANYTHING in the base. ONLY CREATE A HOTKEY FOR THE INIT TO START THE SCRIPT

------------------------------ADJUST THESE FOR YOUR ROTATIONS (DONT WORRY ABOUT THE DEFAULT ROTATION IT WILL BE OVERRIDDEN BASED ON TARGET TYPE! ONLY ADJUST HIGH ARMOR/HIGH MR/BALANCED ROTATIONS ALSO THE AOE DOESNT REALLY DO ANYTHING)-------------------------------

#####
## Setup your Spells
###

# 5     Magic Arrow
# 12    Harm
# 18    Fireball
# 20    Poison
# 27    Curse
# 30    Lightning
# 31    Mana Drain
# 37    Mind Blast
# 42    Energy Bolt
# 43    Explosion
# 46    Mass Curse
# 49    Chain Lightning
# 51    Flamestrike
# 53    Mana Vampire
# 55    Meteor Swarm
# 57    Earthquake

# Poison  ## Set jaseowns_CastPoisonTimerCD to 0 if you want to spam for Lethal
@setvar! jaseowns_CastPoison 0
@setvar! jaseowns_CastPoisonTimerCD 2000
@setvar! jaseowns_CastPoisonMinMana 20

# Curse 27, Mana Drain 31 - Set as 0 if not needed
@setvar! jaseowns_Precast_Spell_One 0
@setvar! jaseowns_Precast_Spell_Two 0

# Define spell rotations for different target types
# High Armor targets (Mind Blast, Energy Bolt, Magic Arrow, Lightning)
@setvar! jaseowns_HighArmor_1st_Spell 37
@setvar! jaseowns_HighArmor_1st_SpellMinMana 20
@setvar! jaseowns_HighArmor_1st_SpellTimerCD 0

@setvar! jaseowns_HighArmor_2nd_Spell 42
@setvar! jaseowns_HighArmor_2nd_SpellMinMana 20
@setvar! jaseowns_HighArmor_2nd_SpellTimerCD 2500

@setvar! jaseowns_HighArmor_3rd_Spell 5
@setvar! jaseowns_HighArmor_3rd_SpellMinMana 12
@setvar! jaseowns_HighArmor_3rd_SpellTimerCD 20000

@setvar! jaseowns_HighArmor_4th_Spell 30
@setvar! jaseowns_HighArmor_4th_SpellMinMana 12
@setvar! jaseowns_HighArmor_4th_SpellTimerCD 20000

# High Magic Resist targets (Flamestrike, Lightning, Explosion, Energy Bolt)
@setvar! jaseowns_HighMR_1st_Spell 51
@setvar! jaseowns_HighMR_1st_SpellMinMana 70
@setvar! jaseowns_HighMR_1st_SpellTimerCD 2500

@setvar! jaseowns_HighMR_2nd_Spell 30
@setvar! jaseowns_HighMR_2nd_SpellMinMana 12
@setvar! jaseowns_HighMR_2nd_SpellTimerCD 20000

@setvar! jaseowns_HighMR_3rd_Spell 43
@setvar! jaseowns_HighMR_3rd_SpellMinMana 40
@setvar! jaseowns_HighMR_3rd_SpellTimerCD 2500

@setvar! jaseowns_HighMR_4th_Spell 42
@setvar! jaseowns_HighMR_4th_SpellMinMana 20
@setvar! jaseowns_HighMR_4th_SpellTimerCD 2500

# Balanced targets (Lightning, Magic Arrow, Flamestrike, Mind Blast)
@setvar! jaseowns_Balanced_1st_Spell 30
@setvar! jaseowns_Balanced_1st_SpellMinMana 12
@setvar! jaseowns_Balanced_1st_SpellTimerCD 20000

@setvar! jaseowns_Balanced_2nd_Spell 5
@setvar! jaseowns_Balanced_2nd_SpellMinMana 12
@setvar! jaseowns_Balanced_2nd_SpellTimerCD 20000

@setvar! jaseowns_Balanced_3rd_Spell 51
@setvar! jaseowns_Balanced_3rd_SpellMinMana 70
@setvar! jaseowns_Balanced_3rd_SpellTimerCD 2500

@setvar! jaseowns_Balanced_4th_Spell 37
@setvar! jaseowns_Balanced_4th_SpellMinMana 20
@setvar! jaseowns_Balanced_4th_SpellTimerCD 2500

# AoE spells (Explosion, Chain Lightning)
@setvar! jaseowns_AoE_1st_Spell 43
@setvar! jaseowns_AoE_1st_SpellMinMana 40
@setvar! jaseowns_AoE_1st_SpellTimerCD 2500

*IGNORE* @setvar! jaseowns_AoE_2nd_Spell 49       *IGNORE*
@setvar! jaseowns_AoE_2nd_SpellMinMana 40
@setvar! jaseowns_AoE_2nd_SpellTimerCD 2500
