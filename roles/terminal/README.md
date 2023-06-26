Gnome Terminal
=========

This role will use community.general.dconf to customise your gnome terminal

Requirements
------------

`community.general.dconf`

Role Variables
--------------

| Name           | Default Value | Type  | Options  | Description                       |
| -------------- | ------------- | ----- | -------- |-----------------------------------|
| `create_new_profile` | true | boolean | `true` `false` | generate a random uuid using the `create_profile_sh` script and write it to the gnome database|
| `profile_id` | null | string | | uuid of gnome profile |
| `visible_name` | Custom | string | | name of profile |
| `set_terminal_profile` | "true" | string | `"true"` `"false"` | set the profile to uuid being used |
| `background_transparency_percent` | 10 | integer | `0-100` | set the background transparency percentage |
| `use_transparent_background` | "true" | string | `"true"` `"false"` | set the terminal to use transparent background |
| `background_color` | "#1E1E2E" | string | |set the terminal background colour |
| `foreground_color` | "#D7DAE0" | string | |set the terminal foreground colour |
| `palette` | "['rgb(110,108,124)', 'rgb(242,143,173)', 'rgb(171,233,179)', 'rgb(250,227,176)', 'rgb(150,205,251)', 'rgb(221,182,242)', 'rgb(245,194,231)', 'rgb(217,224,238)', 'rgb(152,139,162)', 'rgb(242,143,173)', 'rgb(171,233,179)', 'rgb(250,227,176)', 'rgb(150,205,251)', 'rgb(221,182,242)', 'rgb(245,194,231)', 'rgb(217,224,238)']" | string | |set the terminal pallete |
| `bold_color_same_as_fg` | "true" | string | `"true"` `"false"` | set the bold colour the same as foreground |
| `bold_colors_set` | "false" | string | `"true"` `"false"` | set bold colours |
| `use_theme_colors` | "false" | string | `"true"` `"false"` | set to current gnome theme colours |
| `bold_is_bright` | "false" | string | `"true"` `"false"` | set bold colour to bright |
| `cursor_background_color` | "#F5E0DC" | string | | set cursor background colour |
| `cursor_foreground_color` | "#1E1E2E" | string | | set cursor foreground colour |
| `cursor_colors_set` | "true" | string | `"true"` `"false"` | set cursor colour |
| `highlight_colors_set` | "false" | string | `"true"` `"false"` | set if highlight colours will be used or not |
| `default_size_columns` | 80 | integer |  |set inital terminal default column size |
| `default_size_rows` | 24 | integer |  |set inital terminal default row size |
| `use_system_font` | "true" | string | `"true"` `"false"` | set system font |
| `terminal_font` | Source Code Pro 12 | string | | set custom font |
| `cell_width_scale` | 1.00 | integer | | set cell width |
| `cell_height_scale` | 1.00 | integer | | set cell height |
| `text_blink_mode` | always | string | `never` `focused` `unfocused` `always`| set blink mode |
| `cursor_shape` | block | string | `ibeam` `underline` `block` | set cursor shape |
| `cursor_blink_mode` | system | string | `on` `off` `system` | set cursor blink mode |
| `audible_bell` | "true" | string | `"true"` `"false"`| set cursor blink mode |
| `scrollbar_policy` | always | string | `never` `always`| set scroll bar policy |
| `scroll_on_output` | "false" | string | `"true"` `"false"`| set scroll on output |
| `scroll_on_keystroke` | "true" | string | `"true"` `"false"`| set scroll on keystroke |
| `scroll_on_keystroke` | "true" | string | `"true"` `"false"`| set scroll on output |
| `scrollback_unlimited` | "true" | string | `"true"` `"false"` | set scrollback to unlimited |
| `scrollback_lines` | 10000 | integer | | set scrollback to unlimited |
| `terminal_title` | Terminal | String | | set terminal title |
| `title_mode` | replace | String | `before` `after` `ignore` `replace` | set title mode |
| `login_shell` | "false" | String | `"true"` `"false"` | set title mode |
| `use_custom_command` | "false" | String | `"true"` `"false"` | set terminal to use custom command |
| `custom_command` | null | String | | set custom command |
| `preserve_working_directory` | safe | String | `never` `always` `safe` | set terminal to preserve working directory |
| `exit_action` | close | String | `restart` `hold` `close` | set exit action |
| `backspace_binding` | ascii-delete | String | `auto` `ascii-backspace` `delete-sequence` `tty` `ascii-delete` | set backspace binding |
| `delete_binding` | delete-sequence | String | `auto` `ascii-backspace` `delete-sequence` `tty` `ascii-delete` | set delete binding |
| `encoding` | UTF-8 | String | refer to `encoding.txt` to view the whole list | set exit action |

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Example playbook to create a new gnome terminal profile

```yaml
- name: Configure gnome terminal
  hosts: servers
  vars:
    create_new_profile: true
    profile_id:
  roles:
      - terminal
```

Example playbook to configure a current gnome terminal profile

```yaml
- name: Configure gnome terminal
  hosts: servers
  vars:
    create_new_profile: false
    profile_id: b1cc9dd-5262-4d8d-a863-c897e6d979b9
  roles:
      - terminal
```

License
-------

#TBC

Author Information
------------------

K11MY