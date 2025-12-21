# 🎮 EssentialsX Skript Recreation
# NOT AFFILIATED WITH ESSENTIALSX
A comprehensive Minecraft server management Skript that recreates the functionality of the popular EssentialsX plugin using native Skript syntax with skbee and skcrew support.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Minecraft](https://img.shields.io/badge/minecraft-1.16+-green)
![Skript](https://img.shields.io/badge/skript-2.6+-orange)

---

## ✨ Features

### 🏠 **Teleportation System**
- Home management (set, teleport, delete, list)
- Warp system with admin controls
- Spawn point management
- TPA/TPAHere request system
- Back to last location/death point
- World teleportation

### 💬 **Communication**
- Private messaging (msg/tell/whisper)
- Reply to last message
- Message toggling (DND mode)
- Broadcast system
- Nickname support

### 👤 **Player Management**
- God mode (invincibility)
- Fly mode toggle
- Speed adjustment (walk/fly)
- Vanish mode
- Player information display (whois)
- Inventory viewing (invsee)
- Enderchest access

### 🎮 **Gamemode & Utilities**
- Quick gamemode switches (gmc, gms, gma, gmsp)
- Heal and feed commands
- Repair items (hand or all)
- Clear inventory
- Workbench/Anvil/Grindstone access anywhere

### ⚡ **Server Administration**
- Kick/Kickall players
- Sudo command execution
- Give items to players
- Time and weather control
- Server performance info (TPS, memory, uptime)
- List online players

### 💰 **Economy System**
- Balance checking
- Player-to-player payments
- Admin economy management (give/take/set/reset)

### 🎨 **Fun Features**
- Wear items as hats
- Player skull collection
- Burn/Extinguish players
- Suicide command
- More (max stack items)

### 🔒 **Safety Features**
- AFK kick system
- God mode damage prevention
- Permission-based command access
- Teleport request acceptance/denial

---

## 📦 Requirements

### **Essential**
- **Minecraft Server**:  1.16+ (recommended 1.19+)
- **Skript**: Version 2.6 or higher
- **Server Software**: Paper, Spigot, or Purpur

### **Dependencies**
- **[skbee](https://github.com/ShaneBeee/SkBee)**:  For advanced NBT, inventory, and entity management

---

## 🚀 Installation

### **Step 1: Install Dependencies**
1. Download and install [Skript](https://github.com/SkriptLang/Skript/releases)
2. Download and install [skbee](https://github.com/ShaneBeee/SkBee/releases)
4. Restart your server

### **Step 2: Install the Skript**
1. Download `essentialsx-skript.sk` from this repository
2. Place the file in `/plugins/Skript/scripts/`
3. Run `/sk reload essentialsx-skript` or restart the server

### **Step 3: Verify Installation**
1. Type `/essentials version` in-game
2. You should see: `[Essentials] EssentialsX Skript Version:  1.0.0`

### **Step 4: Configure Permissions**
Add permissions to your permissions plugin (LuckPerms, PermissionsEx, etc.)

---

## 📜 Commands

### **General Commands**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/help [search] [page]` | `/ehelp` | View available commands | - |
| `/list` | `/online`, `/who` | List online players | `essentials.list` |
| `/whois <player>` | `/ewhois` | View player information | `essentials.whois` |
| `/essentials [reload/version]` | `/ess`, `/eess` | Plugin management | `essentials.essentials` |

### **Teleportation Commands**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/spawn` | `/espawn` | Teleport to spawn | `essentials.spawn` |
| `/setspawn` | `/esetspawn` | Set spawn point | `essentials.setspawn` |
| `/home [name]` | `/ehome` | Teleport to home | `essentials.home` |
| `/sethome [name]` | `/esethome` | Set home location | `essentials.sethome` |
| `/delhome [name]` | `/edelhome`, `/remhome` | Delete a home | `essentials.delhome` |
| `/homes` | `/ehomes` | List your homes | `essentials.homes` |
| `/warp [name]` | `/ewarp`, `/warps` | Teleport to warp | `essentials.warp` |
| `/setwarp <name>` | `/esetwarp` | Create a warp | `essentials.setwarp` |
| `/delwarp <name>` | `/edelwarp` | Delete a warp | `essentials.delwarp` |
| `/tpa <player>` | `/etpa`, `/call` | Request teleport | `essentials.tpa` |
| `/tpahere <player>` | `/etpahere` | Request player teleport to you | `essentials.tpahere` |
| `/tpaccept` | `/etpaccept` | Accept teleport request | `essentials.tpaccept` |
| `/tpdeny` | `/etpdeny` | Deny teleport request | `essentials.tpdeny` |
| `/back` | `/eback`, `/return` | Return to last location | `essentials.back` |
| `/tp <player> [player]` | `/etp` | Teleport to player | `essentials.tp` |
| `/tphere <player>` | `/etphere` | Teleport player to you | `essentials.tphere` |
| `/tpall [player]` | `/etpall` | Teleport all players | `essentials.tpall` |
| `/world <world>` | `/eworld` | Teleport to world | `essentials.world` |

### **Player Management**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/heal [player]` | `/eheal` | Heal yourself or others | `essentials.heal` |
| `/feed [player]` | `/efeed`, `/eat` | Feed yourself or others | `essentials.feed` |
| `/fly [player]` | `/efly` | Toggle flight mode | `essentials.fly` |
| `/god [player]` | `/egod`, `/godmode` | Toggle god mode | `essentials.god` |
| `/speed [type] <speed>` | `/espeed` | Change walk/fly speed | `essentials.speed` |
| `/vanish [player]` | `/evanish`, `/v` | Toggle visibility | `essentials.vanish` |
| `/nick [nickname]` | `/enick` | Change nickname | `essentials.nick` |
| `/suicide` | `/esuicide` | Kill yourself | - |

### **Gamemode Commands**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/gmc [player]` | `/creative` | Creative mode | `essentials.gamemode.creative` |
| `/gms [player]` | `/survival` | Survival mode | `essentials.gamemode.survival` |
| `/gma [player]` | `/adventure` | Adventure mode | `essentials.gamemode.adventure` |
| `/gmsp [player]` | `/spectator` | Spectator mode | `essentials.gamemode.spectator` |

### **Item & Inventory**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/give <player> <item> [amount]` | `/egive` | Give items to player | `essentials.give` |
| `/repair [hand/all]` | `/fix`, `/erepair` | Repair items | `essentials.repair` |
| `/more` | `/emore` | Max stack item in hand | `essentials.more` |
| `/hat` | `/ehat` | Wear item as hat | `essentials.hat` |
| `/skull [player]` | `/head` | Get player skull | `essentials.skull` |
| `/invsee <player>` | `/einvsee` | View player inventory | `essentials.invsee` |
| `/enderchest [player]` | `/echest`, `/ec` | View enderchest | `essentials.enderchest` |
| `/clearinventory [player]` | `/ci`, `/clear` | Clear inventory | `essentials.clearinventory` |
| `/workbench` | `/wb`, `/craft` | Open crafting table | `essentials.workbench` |
| `/anvil` | `/eanvil` | Open anvil | `essentials.anvil` |
| `/grindstone` | `/egrindstone` | Open grindstone | `essentials.grindstone` |

### **Communication**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/msg <player> <message>` | `/tell`, `/whisper`, `/m` | Private message | `essentials.msg` |
| `/reply <message>` | `/r` | Reply to last message | `essentials.msg` |
| `/msgtoggle` | `/emsgtoggle` | Toggle private messages | `essentials.msgtoggle` |
| `/broadcast <message>` | `/bc`, `/bcast` | Broadcast message | `essentials.broadcast` |

### **Server Management**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/kick <player> [reason]` | `/ekick` | Kick player | `essentials.kick` |
| `/kickall [reason]` | `/ekickall` | Kick all players | `essentials.kickall` |
| `/sudo <player> <command>` | `/esudo` | Force player command | `essentials.sudo` |
| `/burn <player>` | `/eburn` | Set player on fire | `essentials.burn` |
| `/ext [player]` | `/extinguish` | Extinguish fire | `essentials.ext` |
| `/time [set/add] [value]` | `/etime` | Change world time | `essentials.time` |
| `/weather <type>` | `/sun`, `/rain`, `/storm` | Change weather | `essentials.weather` |
| `/gc` | `/lag`, `/tps`, `/mem` | Server performance info | `essentials.gc` |

### **Economy**

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/balance [player]` | `/bal`, `/money` | Check balance | `essentials.balance` |
| `/pay <player> <amount>` | `/epay` | Pay player | `essentials.pay` |
| `/eco <give/take/set> <player> <amount>` | `/economy` | Manage economy | `essentials.eco` |

---

## 🔐 Permissions

### **Permission Structure**
All permissions follow the format: `essentials.<command>[. modifier]`

### **Permission Modifiers**

| Modifier | Description | Example |
|----------|-------------|---------|
| `.others` | Use command on other players | `essentials.heal.others` |
| `.all` | Access all sub-features | `essentials.repair.all` |
| `.kickexempt` | Exempt from AFK kick | `essentials.afk.kickexempt` |

### **Wildcard Permissions**

```yaml
# Grant all essentials permissions
permissions:
  essentials.*:  true

# Grant all teleport permissions
permissions:
  essentials.tp.*: true
  essentials.tpa.*: true
  essentials.home.*: true
```

### **Example LuckPerms Setup**

```bash
# Admin group - all permissions
/lp group admin permission set essentials. * true

# Moderator group - moderation commands
/lp group mod permission set essentials.kick true
/lp group mod permission set essentials.heal. others true
/lp group mod permission set essentials.invsee true

# VIP group - quality of life
/lp group vip permission set essentials.fly true
/lp group vip permission set essentials.speed true
/lp group vip permission set essentials.hat true

# Default group - basic commands
/lp group default permission set essentials.home true
/lp group default permission set essentials.sethome true
/lp group default permission set essentials.tpa true
/lp group default permission set essentials.msg true
```

---

## ⚙️ Configuration

### **Customizing Messages**

Edit the `options` section at the top of the script: 

```skript
options:
    prefix: &6[&bEssentials&6]&r  # Change message prefix
```

### **Economy Starting Balance**

The default starting balance is `0`. To change this, modify the balance commands:

```skript
if {balance.%player%} is not set:
    set {balance.%player%} to 1000  # Change starting balance
```

### **AFK Kick Timer**

Change the AFK kick duration (default is 5 minutes):

```skript
every 1 minute:
    loop all players:
        if difference between {afk.lastmove.%loop-player%} and now is more than 10 minutes:  # Change duration
            kick loop-player due to "AFK for too long"
```

### **Speed Limits**

Default speed range is 0-10.  Adjust in the `/speed` command:

```skript
if {_speed} is between 0 and 20:  # Change max speed
```

---

## 🛠️ Troubleshooting

### **Common Issues**

#### ❌ **"Unknown command" error**
**Solution**: Ensure the script is loaded with `/sk reload essentialsx-skript`

#### ❌ **"You don't have permission"**
**Solution**: Grant the appropriate permission node (see [Permissions](#permissions))

#### ❌ **Teleport commands not working**
**Solution**: 
1. Check if spawn/homes are set
2. Verify player is online for TPA requests
3. Ensure world exists for `/world` command

#### ❌ **Economy not working**
**Solution**: Balance variables initialize on first use.  Run `/balance` once to create your account.

#### ❌ **Variables not saving on restart**
**Solution**:  Ensure Skript's `variables. csv` has write permissions

### **Debug Mode**

Enable Skript debug mode to see detailed error messages:

```bash
/skript reload essentialsx-skript. sk
# Watch console for errors
```

---

## 🔄 Updates & Roadmap

### **Version 1.0.0** ✅
- Core teleportation system
- Basic economy
- Player management commands
- Communication system

### **Planned for 1.1.0** 🚧
- Kits system with cooldowns
- Jail/Ban system with time support
- Sign editing commands
- Spawner manipulation
- PowerTools system
- Custom join/quit messages
- MOTD system
- Worth/Sell system

### **Planned for 1.2.0** 📋
- GUI-based management
- MySQL/SQLite database support
- Multi-language support
- Advanced warp categories
- Custom commands framework

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### **Reporting Bugs**
1. Check existing [Issues](../../issues)
2. Create a new issue with: 
   - Minecraft version
   - Skript version
   - Detailed description
   - Steps to reproduce
   - Error messages (if any)

### **Suggesting Features**
1. Open a [Feature Request](../../issues/new)
2. Describe the feature and use case
3. Explain how it benefits users

### **Code Contributions**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### **Code Style Guidelines**
- Use descriptive variable names
- Comment complex logic
- Follow existing formatting
- Test thoroughly before submitting

---

## 🙏 Credits

### **Inspired By**
- [EssentialsX](https://github.com/EssentialsX/Essentials) - The original Essentials plugin

### **Built With**
- [Skript](https://github.com/SkriptLang/Skript) - Event-driven scripting for Minecraft
- [skbee](https://github.com/ShaneBeee/SkBee) - Advanced Skript addon

### **Special Thanks**
- EssentialsX team for the original plugin
- Skript community for documentation and support
- All contributors and testers

---

## 🌟 Show Your Support

If this project helped you, please consider: 
- ⭐ Starring this repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 🤝 Contributing code

---

<div align="center">

[⬆ Back to Top](#-essentialsx-skript-recreation)

</div>
