Note not all functions work in classic yet

# Unit
## Constants
- .Pointer
- .Name
- .GUID
- .Player
- .Friend
- .CombatReach
- .ObjectID

## Variables
- .PosX
- .PosY
- .PosZ
- .Distance
- .Dead
- .Health
- .HealthMax
- .HP
- .TTD
- .LoS
- .Attackable
- .ValidEnemy
- .Target
- .Moving
- .Facing
- .Quest

## Functions
- :GetDistance(OtherUnit)
- :LineOfSight(OtherUnit)
- :IsEnemy()
- :IsBoss()
- :HasThreat()
- :GetEnemies(Yards)
- :GetFriends(Yards, HP)
- :HardCC()
- :Interrupt()
- :Dispel(Spell)
- :PredictPosition(Time)
- :AuraByID(SpellID, OnlyPlayer)
- :CCed()
- :IsQuest()
- :GetTTD(targetPercentage)

# Player
## Constants
- .Pointer
- .Name
- .GUID
- .Class
- .CombatReach

## Variables
- .PosX
- .PosY
- .PosZ
- .Health
- .HealthMax
- .HP
- .EID
- .Power
- .PowerMax
- .PowerDeficit
- .PowerPct
- .PowerRegen
- .ComboPoints
- .ComboMax
- .ComboDeficit
- .Instance
- .Casting
- .Moving
- .PetActive
- .InGroup
- .CombatTime
- .CombatLeftTime
- .SwingLast
- .SwingNext

## Functions
- :GCDRemain()
- :GCD()
- :CDs()
- :CritPct()
- :TTM()
- :AutoTarget(Yards, Facing)
- :GetEnemies(Yards)
- :GetAttackable(Yards)
- :GetEnemiesRect(Length, Width, TTD)
- :GetEnemiesCone(Length, Angle, TTD)
- :GetFriends(Yards, HP)
- :GetFriendsCone(Length, Angle, HP)

## Tables
- Buffs
- Debuffs
- Equipment
- Items
- LastCast
- Spells
- Talents

# Buff/Debuff
## Constants
- .Ranks[]
- .SpellID
- .SpellName
- .BaseDuration

## Functions
- :Exist(Unit, OnlyPlayer)
- :Remain(Unit, OnlyPlayer)
- :Duration(Unit, OnlyPlayer)
- :Elapsed(Unit, OnlyPlayer)
- :Refresh(Unit, OnlyPlayer)
- :Stacks(Unit, OnlyPlayer)
- :Rank(Unit, OnlyPlayer)
- :Count(Table)
- :Lowest(Table)
- :Query(Unit, OnlyPlayer)

# Spell
## Constants
- .Ranks[]
- .SpellID
- .SpellName
- .BaseCD
- .BaseGCD
- .MinRange
- .MaxRange
- .CastType
- .IsHarmful
- .IsHelpful

## Functions
- :Cost(Rank)
- :CD(Rank)
- :IsReady(Rank)
- :Charges()
- :ChargesFrac()
- :RechargeTime()
- :FullRechargeTime()
- :CastTime(Rank)
- :LastCast(Index)
- :Cast(Unit, Rank)
- :CastPool(Unit, Extra, Rank)
- :CastGround(X, Y, Z, Rank)

# Item
## Constants
- .ItemID
- .ItemName
- .SpellName
- .SpellID

## Functions
- :Equipped()
- :CD(Rank)
- :IsReady(Rank)
- :Use(Unit)