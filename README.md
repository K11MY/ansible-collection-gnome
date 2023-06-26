# Gnome Workstation Collection for Ansible

This collection includes Ansible roles aims to help customise Gnome Workstations.

Roles included in this collection:
- `gnome.setup.terminal`

## Installation

Install via Ansible Galaxy:

```bash
ansible-galaxy collection install gnome.setup
```

Or include this collection in your playbook's `requirements.yml` file:

```yaml
---
collections:
  - name: gnome.setup
```

### Role Requirements
- `community.general.dconf`

## Usage
Below is an example playbook that customises the gnome terminal

```yaml
---
- name: Customise gnome terminal
  hosts: local
  gather_facts: true
  vars: 
    # terminal vars
    create_new_profile: true
    profile_id:
    visible_name: Cat
    background_transparency_percent: 10
    use_transparent_background: true
    background_color: "#1E1E2E"
    # tweaks vars
    icon_theme: ePapirus-Dark
    user_theme_name: Catppuccin-Frappe-Standard-Rosewater-Dark
    font_name: Cantarell 11
    action_double_click_titlebar: toggle-maximize
    # background vars
    user_home: chai
    bg_default_img_name: background1.jpg
    bg_default_img_path: "/home/{{ user_home }}/Downloads/{{ bg_default_img_name }}"
  roles:
    - gnome.setup.terminal
    - gnome.setup.tweaks
    - gnome.setup.background
```
## License

TBC 

## Author
Kim Pham