# Dconf Settings

This role handles configuring the specified dconf settings.

## Requirements

The hosts you are targeting should have the following packages:

- python >= 2.6
- python-dnf

## Role Variables

| Variable       | Required | Default | Description                                                                                                          |
| -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------- |
| dconf_settings | &#9989;  | `[]`    | A list of dconf settings to set.<br><br>Each item in the list should be a dictionary containing a `key` and `value`. |

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: jaredhocutt.vscode
      vars:
        dconf_settings:
          - key: /org/gnome/desktop/interface/clock-show-date
            value: "true"
          - key: /org/gnome/desktop/interface/clock-format
            value: "'12h'"
          - key: /org/gnome/desktop/interface/show-battery-percentage
            value: "true"
```

## License

MIT

## Author Information

Jared Hocutt (@jaredhocutt)
