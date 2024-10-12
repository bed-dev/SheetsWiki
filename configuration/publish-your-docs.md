---
icon: square-plus
description: Once you’ve finished installing sheets, you can create and test menus
---

# Creating & Editing Menus

## Menu Structure

Each menu is defined with a configuration file (`menu_name.yml`)  inside the Sheets/menus folder and follows a structured format in **YAML**. Here's a breakdown of the key components of a menu:

### Title

**Description:** The title displayed at the top of the menu.

**Type:** `String`

**Optional:** `false`

**Example:**

```yaml
title: "Example Menu"
```

### Content

**Description:** The content only bedrock users see below the title

**Type:** `String`

**Optional:** `true`

**Example:**

```yaml
content: "&7Content that only the bedrock players see"
```

### Size

**Description:** The size of the menu (must be a multiple of 9)

**Type:** `Integer`

**Default:** `27`

**Optional:** `false`

**Example:**

```yaml
size: 27
```

### Commands

**Description:** A list of commands that can be executed to open the menu

**Type:** `List of strings`

**Optional:** `true`

**Example:**

```yaml
# Example one
commands:
  - somerandom command
  
# Example two
command: examplecommand
```

### Permission

**Description:** A permission string required to open the menu and execute the menu commands

**Type:** `String`

**Optional:** `true`

**Example:**

```yaml
permission: beds.examplemenu
```

### Filler

**Description:** Items used to fill empty slots in the menu, only for java guis.

**Type:** `Item`

**Optional:** `true`

**Example:**

```yaml
filler:
  material: GRAY_STAINED_GLASS_PANE
  name: "&7"
#  slots:  # Custom slots if needed
#  - 15-17
```

### Buttons

**Description:** Defines clickable items in the menu

**Type:** `List of buttons`

**Optional:** `false`

See individual button properties below here.



## Example Menu

```yaml
# The title of the menu when it is opened
title: "Example Menu"

content: "&7Content that only the bedrock players see"

# The size of the menu (must be a multiple of 9)
size: 27

commands:
  - somerandom command

permission: beds.examplemenu

# Items to be displayed in the menu
buttons: # Check out buttons section

filler: # won't appear on bedrock
  material: GRAY_STAINED_GLASS_PANE
  name: "&7"
#  slots:  # Custom slots if needed
#  - 15-17
```
