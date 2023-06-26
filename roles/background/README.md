Gnome Background
=========

This role will use community.general.dconf to customise your gnome background

Requirements
------------

`community.general.dconf`

Role Variables
--------------

| Name           | Default Value | Type  | Options  | Description                       |
| -------------- | ------------- | ----- | -------- |-----------------------------------|
| `user_home` | marryjane | string | | user home directory name |
| `bg_default_img_name` | bg_light.jpg | string | | name of image including extension |
| `bg_default_img_path` | "file:///home/{{ user_home }}/{{ bg_default_img_name }}" | string | | path where the image is stored |
| `bg_dark_img_name` | bg_dark.jpg | string | | name of image including extension |
| `bg_dark_img_path` | "file:///home/{{ user_home }}/{{ bg_dark_img_name }}" | string | | path where the image is stored |

Example Playbook
----------------

Example playbook to configure gnome-tweaks

```yaml
- name: Configure gnome terminal
  hosts: servers
  vars:
    user_home: marry
  roles:
    - background
```

License
-------

#TBC

Author Information
------------------

K11MY