# SYN Discord Admin - Commands Reference

## 🎮 Commands

All commands use the prefix: `?command`

### 👤 Character Management

#### Height Management
```
?command height check <CHARACTER_ID>
?command height change <CHARACTER_ID> <NEW_HEIGHT>
```
- **Examples**: 
  - `?command height check 123`
  - `?command height change 123 1.05`
- **Note**: Player must be offline for height changes

#### Name Change
```
?command namechange <CHAR_ID> <OLD_FIRST> <OLD_LAST> <NEW_FIRST> <NEW_LAST>
```
- **Example**: `?command namechange 123 Jack Smith John Snow`
- **Note**: Player must be offline and old name must match exactly

#### Location Change
```
?command locationchange <CHARACTER_ID> <NEW_LOCATION>
```
- **Example**: `?command locationchange 123 valentine`

#### Date of Birth Change
```
?command dobchange <CHARACTER_ID> <NEW_DOB>
```
- **Example**: `?command dobchange 123 1885-01-01`

### 🚀 Teleportation

#### Teleport by Player ID
```
?command tp <PLAYER_ID> <LOCATION>
```
- **Examples**: 
  - `?command tp 5 valentine`
  - `?command tp 12 blackwater`
  - `?command tp 3 sd` (using alias)

#### Teleport by Character ID
```
?command tpchar <CHARACTER_ID> <LOCATION>
```
- **Examples**: 
  - `?command tpchar 123 valentine`
  - `?command tpchar 456 armadillo`
  - `?command tpchar 789 col` (using alias)

#### Set Custom Location
```
?command setloc <CHARACTER_ID> <LOCATION>
```
- **Examples**: 
  - `?command setloc 123 valentine`
  - `?command setloc 456 rhodes`
  - `?command setloc 789 tw` (using alias)

### 💰 Economy Management

#### Cash Operations
```
?command cash give <CHARACTER_ID> <AMOUNT>
?command cash take <CHARACTER_ID> <AMOUNT>
```
- **Examples**: 
  - `?command cash give 123 500`
  - `?command cash give 456 1500`
  - `?command cash take 123 200`
  - `?command cash take 789 750`

#### Legacy Cash Commands
```
?command givecash <PLAYER_ID> <AMOUNT>
?command takecash <PLAYER_ID> <AMOUNT>
```
- **Examples**: 
  - `?command givecash 5 300`
  - `?command takecash 8 150`

### 🎒 Inventory Management

#### Give Items
```
?command giveitem <CHARACTER_ID> <ITEM_NAME> <AMOUNT>
```
- **Examples**: 
  - `?command giveitem 123 bread 10`
  - `?command giveitem 456 water 5`
  - `?command giveitem 789 money 1000`

#### Give Weapons
```
?command givewep <PLAYER_ID> <WEAPON_NAME>
```
- **Examples**: 
  - `?command givewep 5 weapon_rifle_carbine`
  - `?command givewep 8 weapon_pistol_volcanic`
  - `?command givewep 12 weapon_shotgun_pump`

#### Society Inventory Upgrade
```
?command invup <JOB_NAME> <INCREASE_AMOUNT>
```
- **Examples**: 
  - `?command invup blacksmith 10`
  - `?command invup doctor 15`
  - `?command invup gunsmith 20`

### 🏠 Property Management

#### Ranch Management
```
?command delranch <RANCH_ID>
?command nameranch <RANCH_ID> <NEW_NAME>
?command moveranch <RANCH_ID> <CHARACTER_ID>
```
- **Examples**: 
  - `?command delranch 15`
  - `?command nameranch 10 "Johnson Ranch"`
  - `?command moveranch 5 123`

#### Shop Management
```
?command delshop <SHOP_ID>
?command moveshop <SHOP_ID> <CHARACTER_ID>
```
- **Examples**: 
  - `?command delshop 8`
  - `?command moveshop 12 456`

### 📋 Auditing & Information

#### Character Information
```
?command getcharacters <STEAM_ID>
?command charaudit <CHARACTER_ID>
```
- **Examples**: 
  - `?command getcharacters steam:110000100075a4f`
  - `?command charaudit 123`

#### Housing Audit
```
?command housingaudit <CHARACTER_ID>
?command multiplehouses <CHARACTER_ID>
```
- **Examples**: 
  - `?command housingaudit 123`
  - `?command multiplehouses 456`

#### Storage Management
```
?command storages check <STORAGE_ID>                 -- View storage details, shared access, and contents
?command storages contents <STORAGE_ID>              -- View storage contents only
?command storages delete <STORAGE_ID>                -- Delete a storage unit
?command storages owned <CHARACTER_ID>               -- View all storages owned by a character
?command multiplestorages <CHARACTER_ID>             -- Check multiple storage ownership
?command checkmultiaccess <STORAGE_ID>               -- Check shared access for a storage
```
- **Examples**: 
  - `?command storages check 45`
  - `?command storages contents 67`
  - `?command storages delete 23`
  - `?command storages owned 123`
  - `?command multiplestorages 456`
  - `?command checkmultiaccess 89`

#### Inventory Search
```
?command searchinventory <ITEM_NAME>
?command searchserial <SERIAL_NUMBER>
```
- **Examples**: 
  - `?command searchinventory bread`
  - `?command searchinventory weapon_rifle_carbine`
  - `?command searchserial WS123456789`

#### Banking
```
?command auditbank <CHARACTER_ID>
```
- **Examples**: 
  - `?command auditbank 123`
  - `?command auditbank 456`

### 🚢 Vehicle Management

#### Boat Manifest
```
?command boatmanifest <CHARACTER_ID>
```
- **Examples**: 
  - `?command boatmanifest 123`
  - `?command boatmanifest 789`

#### Stable Manifest
```
?command stablemanifest <CHARACTER_ID>
```
- **Examples**: 
  - `?command stablemanifest 123`
  - `?command stablemanifest 456`

#### Fix Horse
```
?command fixhorse coat <HORSE_ID_1> <HORSE_ID_2>     -- Copy coat & model from Horse2 to Horse1
?command fixhorse breeding <HORSE_ID>                -- Enable breeding for a horse
?command fixhorse age <HORSE_ID> <NEW_AGE>           -- Change horse age
?command fixhorse exp <HORSE_ID> <NEW_EXP>           -- Change horse EXP
?command fixhorse model <HORSE_ID> <NEW_MODEL>       -- Manually update model
?command fixhorse components <HORSE_ID> <COMPONENTS> -- Manually update components
```
- **Examples**: 
  - `?command fixhorse coat 42 56` (copy from horse 56 to horse 42)
  - `?command fixhorse breeding 42`
  - `?command fixhorse age 42 5`
  - `?command fixhorse exp 42 1500`
  - `?command fixhorse model 42 A_C_Horse_MissouriFoxTrotter_SilverDapplePinto`
  - `?command fixhorse components 42 []`

### 👔 Job Management

#### Job Operations
```
?command jobs list <CHARACTER_ID>                    -- View all jobs & multi-jobs
?command jobs set <CHARACTER_ID> <JOB> <GRADE>       -- Set primary job
?command jobs add <CHARACTER_ID> <JOB> <GRADE>       -- Add multi-job
?command jobs remove <CHARACTER_ID> <JOB>            -- Remove multi-job
?command jobs clear <CHARACTER_ID>                   -- Remove all jobs & set to unemployed
```
- **Examples**: 
  - `?command jobs list 123`
  - `?command jobs set 123 blacksmith 3`
  - `?command jobs add 123 doctor 2`
  - `?command jobs remove 123 doctor`
  - `?command jobs clear 123`

#### Group Management
```
?command group add <CHARACTER_ID> <GROUP>            -- Set character's group
?command group reset <CHARACTER_ID>                  -- Reset character's group to user
?command group purge <STEAM_ID>                      -- Reset all characters for Steam ID to user
```
- **Examples**: 
  - `?command group add 123 admin`
  - `?command group add 456 moderator`
  - `?command group reset 123`
  - `?command group purge steam:110000100075a4f`

#### Hideouts
```
?command hideouts check <HIDEOUT_ID>                 -- View hideout details
?command hideouts contents <HIDEOUT_ID>              -- View hideout inventory
?command hideouts setowner <HIDEOUT_ID> <CHAR_ID>    -- Transfer ownership
?command hideouts addcoowner <HIDEOUT_ID> <CHAR_ID>  -- Add co-owner
?command hideouts removecoowner <HIDEOUT_ID> <CHAR_ID> -- Remove co-owner
?command hideouts clearcoowners <HIDEOUT_ID>         -- Clear all co-owners
```
- **Examples**: 
  - `?command hideouts check 7`
  - `?command hideouts contents 7`
  - `?command hideouts setowner 7 123`
  - `?command hideouts addcoowner 7 456`
  - `?command hideouts removecoowner 7 456`
  - `?command hideouts clearcoowners 7`

### 💬 Communication

#### Telegram Management
```
?command telegram check <TELEGRAM_ID>                -- Check who owns a telegram ID
?command telegram change <OLD_TELEGRAM> <NEW_TELEGRAM> -- Change telegram ID
```
- **Examples**: 
  - `?command telegram check 555123`
  - `?command telegram change 555123 555999`

### 🛠️ Utility Commands

#### Player Management
```
?command res <PLAYER_ID>              -- Resurrect player
?command checkactive                  -- Check active players
?command clearall                     -- Clear chat
```
- **Examples**: 
  - `?command res 5`
  - `?command checkactive`
  - `?command clearall`

#### Society Management
```
?command viewsociety                  -- View all societies
```
- **Examples**: 
  - `?command viewsociety`

#### General Audit
```
?command audit <CHARACTER_ID>         -- General character audit
```
- **Examples**: 
  - `?command audit 123`
  - `?command audit 456`

## 🗺️ Teleport Locations & Aliases

| Location | Aliases |
|----------|---------|
| **valentine** | valentine, val, schmud |
| **saintdenis** | saintdenis, sd, dennis |
| **strawberry** | strawberry, sb, straw, berry |
| **annesburg** | annesburg, ab, annes |
| **chuparosa** | chuparosa, chu, chupa |
| **escalera** | escalera, esc |
| **guarma** | guarma, gua |
| **armadillo** | armadillo, arm, arma |
| **tumbleweed** | tumbleweed, tw |
| **blackwater** | blackwater, bw, backwater |
| **rhodes** | rhodes, rh |
| **colter** | colter, col, snow |
| **sisika** | sisika, prison | 