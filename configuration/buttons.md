---
icon: circle-dot
description: >-
  Buttons are the interactive elements within a menu that players can click to
  trigger various actions. Each button can be customized to display specific
  menus, run commands, send messages, and more.
---

# Buttons

Buttons component of a menu is a list of buttons, which has the following properties:

## Button Display

### Slot

**Description:** Defines the position of the button in the menu. Slot numbers start from 0 and go up to the size of the menu.

**Type:** `Integer`

**Optional:** `false`

**Example:**

```yaml
slot: 10
```

### Amount

**Description:** Specifies how many of the item should be displayed in the button slot.

**Type:** `Integer`

**Optional:** `true`

**Example:**

```yaml
amount: 1
```

### Material

**Description:** The Minecraft material for the button. This is the actual item that players will see in the slot.

**Type:** [**Material**](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html)

**Optional:** `false`

**Example:**

```yaml
material: DIAMOND_SWORD
```

### Image

**Description:**&#x20;

URL or Material for displaying custom icons  for image (primarily used for Bedrock users).

**Type: URL or** [**Material**](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html)

**Optional:** `true`

**Example:**

<pre class="language-yaml"><code class="lang-yaml"><strong># Example 1
</strong><strong>image: https://example.com/image.png
</strong><strong>
</strong><strong># Example 2
</strong><strong>image: PAPER
</strong></code></pre>

### Path

**Description:**&#x20;

Texture path for image, can override image

**Type: URL or** [**Material**](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html)

**Optional:** `true`

**Example:**

<pre class="language-yaml"><code class="lang-yaml"><strong>path: textures/i/glyph_world_template.png
</strong></code></pre>

### Name

**Description:** The display name of the button item. Supports color codes and placeholders.

**Type:** `String`

**Optional:** `false`

**Example:**

```yaml
name: "&cCommand Action"
```

### Lore

**Description:** Descriptive text that appears when players hover over the button. Supports multiple lines, color codes, and placeholders.

**Type:** `List of Strings`

**Optional:** `false`

**Example:**

```yaml
lore: 
    - "&7Click to execute a command"
    - "<black>Line 2 of lore"
```

### Bedrock Lore

**Description:** Specific lore for bedrock button

**Type:** `String`

**Optional:** `true`

**Example:**

```yaml
bedrock_lore: "&7Click to execute a command"
```

### Enchantments

**Description:** A list of enchantments applied to the button item, such as `SHARPNESS`, `UNBREAKING`, etc.

**Type: List of** [**Enchantments**](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/enchantments/Enchantment.html)

**Optional:** `true`

**Example:**

<pre class="language-yaml"><code class="lang-yaml">enchantments:
<strong>    - SHARPNESS: 5
</strong>    - UNBREAKING: 5
</code></pre>

### Custom Model data

**Description:** The Minecraft custom model data for the item

**Type:** `Integer`

**Optional:** `true`

**Example:**

```yaml
custom_model_data: 12131
```

## Button Conditions

### Items

**Description:** Required items that are required to click the button, They will be taken to performs the actions

**Type: List of Items**

**Optional:** `true`

**Example:**

```yaml
items:
  - material: DIAMOND
    amount: 1
    name: "name of the item if wanted, can be removed"
    lore: "lore of the item if wanted, can be removed"
# enchantments can also be added like in the main button
```

### Price

**Description:** Defines the in-game cost (e.g., currency) required to click this button. Useful in shops or trade menus. requires Vault

**Type:** `Float`

**Optional:** `true`

**Example:**

```yaml
price: 200.99
```

### Permission

**Description:** A permission string required to click this button

**Type:** `String`

**Optional:** `true`

**Example:**

```yaml
permission: "toclick.this.button"
```

### Actions

**Description:** Defines the actions triggered when the button is clicked. Multiple actions can be linked to a single button.

**Type:  List of actions**

**Optional:** `false`

**Example:**

```yaml
actions:
      - console: "give %player% diamond_sword" # Command ran a the console
      - message: "You have received an epic sword!" # message sent to the player
      - sound: "ITEM_PICKUP" # Sound played
      - player: "say hi" # command ran by player (can also be command:)
      - sound: "ENTITY_EXPERIENCE_ORB_PICKUP"
      - menu: "anothermenu" # Open another menu
      - close # Close the menu
```

### Requirements

**Description:** Conditions that must be met for the button to be visible or clickable. These can include permissions or placeholders.

Checkout Requirements for the requirements

**Type: Map of view and click**

**Both view and click take a List of Requirements**

**Optional:** `true`

**Example:**

```yaml
requirements:
    view:
        - 
    click:
        -
```

Checkout next page to create Requirements
