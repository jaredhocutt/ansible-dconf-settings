# Dconf Settings

Sets dconf settings specified by the user.

## Requirements

None

## Role Variables

| Variable         | Required           | Default | Description                                                                                                            |
| ---------------- | ------------------ | ------- | ---------------------------------------------------------------------------------------------------------------------- |
| `dconf-settings` | :heavy_check_mark: | `[]`    | The list of dconf settings to set. Each item in the list should have a `key` and `value` (see example playbook below). |

## Dependencies

None

## Example Playbook

```yaml
- hosts: localhost
  vars:
    dconf_settings:
      - key: /org/gnome/desktop/interface/clock-show-date
        value: "true"
      - key: /org/gnome/desktop/interface/clock-format
        value: "'12h'"
      - key: /org/gnome/desktop/interface/show-battery-percentage
        value: "true"
  roles:
      - jaredhocutt.dconf-settings
```
