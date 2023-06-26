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
| `icon_theme` | ePapirus-Dark | string | | icon theme name |
| `user_theme_name` | Catppuccin-Frappe-Standard-Rosewater-Dark | string | | user theme |
| `gtk_theme` | Catppuccin-Frappe-Standard-Rosewater-Dark | string | | gtk them |
| `monospace_font_name` | Source Code Pro Medium 12| string | | monospace font name |
| `font_name` | Cantarell 11| string | | system font |
| `document_font_name` | Cantarell 11| string | | document font |
| `action_double_click_titlebar` | toggle-maximize | string | `lower` `menu` `minimize` `none` `toggle-maximize` `toggle-maximize-horizontally` `toggle-maximize-vertically` `toggle-shade` | double click title bar action|
| `action_middle_click_titlebar` | toggle-maximize | string | `lower` `menu` `minimize` `none` `toggle-maximize` `toggle-maximize-horizontally` `toggle-maximize-vertically` `toggle-shade` | middle click title bar action|
| `action_right_click_titlebar` | toggle-maximize | string | `lower` `menu` `minimize` `none` `toggle-maximize` `toggle-maximize-horizontally` `toggle-maximize-vertically` `toggle-shade` | right click title bar action|

Example Playbook
----------------

Example playbook to configure gnome-tweaks

```yaml
- name: Configure gnome terminal
  hosts: servers
  roles:
      - tweaks
```

License
-------

#TBC

Author Information
------------------

K11MY