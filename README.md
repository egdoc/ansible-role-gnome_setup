Ansible role: gnome_setup
=========

Ansible role to setup the GNOME desktop environment

Requirements
------------

dconf must by installed on targets

Role Variables
--------------

```yaml
gnome_power_inactive_ac_type: suspend 
```

The type of sleeping that should be performed when the computer is inactive.

```yaml
gnome_power_inactive_ac_timeout: 900
```

The amount of time in seconds the computer on AC power needs to be inactive before it goes to sleep. A value of 0 means never.

```yaml
gnome_power_inactive_battery_timeout: 900
```

The amount of time in seconds the computer on battery power needs to be inactive before it goes to sleep. A value of 0 means never.

```yaml
gnome_power_idle_dim: true
```

If the screen should be dimmed to save power when the computer is idle.

```yaml
gnome_power_idle_brightness: 30
```

This is the laptop panel screen brightness used when the session is idle.

```yaml
gnome_shell_enabled_extensions: []
```

GNOME Shell extensions have a UUID property; this key lists extensions which should be loaded. Any extension that wants to be loaded needs to be in this list.

```yaml
gnome_shell_favorite_apps:
    - firefox.desktop
    - org.gnome.Calendar.desktop
    - org.gnome.Music.desktop
    - org.gnome.Nautilus.desktop
    - org.gnome.Software.desktop
```

The applications corresponding to these identifiers will be displayed in the favorites area.

```yaml
gnome_media_keys_custom_keybindings: []
```

List of custom keybindings.

```yaml
gnome_nautilus_icon_view_default_zoom_level: medium
```

Default icon view zoom level

```yaml
gnome_nautilus_icon_view_captions: []
```

A list of captions below an icon in the icon view.

```yaml
gnome_nautilus_list_view_zoom_level: medium
```

Default list view zoom level

```yaml
gnome_nautilus_preferences_click_policy: double
```

Possible values are “single” to launch files on a single click, or “double” to launch them on a double click.

```yaml
gnome_nautilus_preferences_show_create_link: false
```

If set to true, then Nautilus will show context menu items to create links from the copied or selected files.

```yaml
gnome_nautilus_preferences_show_delete_permanently: false
```

If set to true, then Nautilus will show a delete permanently context menu item to bypass the Trash.

```yaml
gnome_gtk_sort_directories_first: false
```

If set to true, then folders are shown before files in the list.

```yaml
gnome_gtk_show_hidden: false
```

Controls whether the file chooser shows hidden files or not.

```yaml
gnome_desktop_interface_show_battery_percentage: false
```

If true, display battery percentage in the status menu, in addition to the icon.

```yaml
gnome_desktop_interface_enable_animations: true
```

Whether animations should be displayed

```yaml
gnome_desktop_interface_text_scaling_factor: 1
```

Factor used to enlarge or reduce text display, without changing font size.

```yaml
gnome_desktop_interface_scaling_factor: 1
```

Integer factor used to scale windows by.

```yaml
gnome_desktop_interface_gtk_theme: Adwaita
```

Basename of the default theme used by gtk+.

```yaml
gnome_desktop_interface_icon_theme: Adwaita
```

Icon theme to use for the panel, nautilus etc.

```yaml
gnome_desktop_privacy_remember_recent_files: true
```

Whether to remember recently used files.

```yaml
gnome_desktop_privacy_recent_files_max_age: 1
``` 

Number of days to remember recently used files for.

```yaml
gnome_desktop_privacy_remove_old_trash_files: false
```

Whether to remove old files from the trash automatically

```yaml
gnome_desktop_privacy_remove_old_temp_files: true
```

Whether to remove old temporary files automatically

```yaml
gnome_desktop_privacy_old_files_age: 30
```

Number of days to keep trash and temporary files

```yaml
gnome_desktop_peripherals_touchpad_natural_scroll: true
```

Whether two-finger scrolling is enabled

```yaml
gnome_desktop_peripherals_touchpad_tap_to_click: false
```

Enable mouse clicks with touchpad

```yaml
gnome_desktop_peripherals_touchpad_two_finger_scrolling_enabled: true
```

Whether two-finger scrolling is enabled

```yaml
gnome_desktop_sound_event_sounds: true
```

Sounds for events

```yaml
gnome_desktop_sound_input_feedback_sounds: false
```

Input feedback sound

```yaml
gnome_desktop_background_picture: ''
```

Path of background image.

```yaml
gnome_desktop_background_picture_dark: ''
```

Path of background image in dark mode.

```yaml
gnome_desktop_background_picture_options: zoom
```

Determines how the image set by wallpaper_filename is rendered.

```yaml
gnome_desktop_screensaver_idle_activation_enabled: true
```

Set this to true to activate the screensaver when the session is idle

```yaml
gnome_desktop_screensaver_lock_enabled: true
```

Set this to TRUE to lock the screen when the screensaver goes active

```yaml
gnome_desktop_screensaver_lock_delay: 0
```

The number of seconds after screensaver activation before locking the screen

```yaml
gnome_desktop_screensaver_status_message_enabled: true
```

Allow the session status message to be displayed

```yaml
gnome_mutter_workspaces_only_on_primary: false
```

Determines whether workspace switching should happen for windows on all monitors or only for windows on the primary

```yaml
gnome_mutter_center_new_windows: false
```

When true, the new windows will always be put in the center of the active screen of the monitor


Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
        - role: egdoc.gnome_setup 
          gnome_desktop_peripherals_touchpad_natural_scroll: false
          gnome_desktop_peripherals_touchpad_tap_to_click: true

License
-------

GPLv3

Author Information
------------------

Role created by Egidio Docile in 2023.
