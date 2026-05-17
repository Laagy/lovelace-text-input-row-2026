# Lovelace Text Input Row (HA 2026 Compatible)

A modernized fork of the original `lovelace-text-input-row` custom row for Home Assistant.

This version has been updated to work with modern Home Assistant releases including HA 2026.5.

Supports `input_text` entities inside Lovelace entities cards.

---

## Installation

### HACS (Recommended)

1. Open HACS
2. Go to **Frontend**
3. Click the three dots in the top right corner
4. Select **Custom repositories**
5. Add your repository URL:

```text
https://github.com/Laagy/lovelace-text-input-row-2026
```

Category:

```text
Dashboard
```

6. Install the card
7. Restart Home Assistant

---

## Manual Installation

Download:

```text
lovelace-text-input-row.js
```

Copy the file into:

```text
/config/www/
```

Add the resource to your dashboard:

```yaml
resources:
  - url: /local/lovelace-text-input-row.js
    type: module
```

Restart Home Assistant.

---

## Example Configuration

```yaml
type: entities
entities:
  - entity: input_text.announcement_text
    type: custom:text-input-row

  - type: call-service
    name: Announce
    icon: mdi:bullhorn
    action_name: Send
    service: script.send_announcement
```

---

## Notes

* Only works with `input_text` entities
* Updated for modern Home Assistant frontend APIs
* Original project was abandoned for several years, this fork restores compatibility with current HA versions

---

## Credits

Original project:
gadgetchnnel

HA 2026 compatibility fork:
Laagy
