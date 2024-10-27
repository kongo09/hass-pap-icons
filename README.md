[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

# hass-pap-icons

Custom icon pack designed for Home Assistant containing icons for Philips Air Purifier.

## Content

| icon                                | name               |
|-------------------------------------|--------------------|
| ![Preview](./svg/power_button.svg)  | power_button       |
| ![Preview](./svg/child_lock_button.svg) | child_lock_button |
| ![Preview](./svg/auto_mode_button.svg) | auto_mode_button |
| ![Preview](./svg/fan_speed_button.svg) | fan_speed_button |
| ![Preview](./svg/humidity_button.svg)  |humidity_button |
| ![Preview](./svg/light_dimming_button.svg) | light_dimming_button |
| ![Preview](./svg/two_in_one_mode_button.svg) | two_in_one_mode_button |
| ![Preview](./svg/timer_reset_button.svg) | timer_reset_button |
| ![Preview](./svg/sleep_mode.svg) | sleep_mode |
| ![Preview](./svg/auto_mode.svg)  | auto_mode |
| ![Preview](./svg/speed_1.svg)    | speed_1 |
| ![Preview](./svg/speed_2.svg)    | speed_2 |
| ![Preview](./svg/speed_3.svg)    | speed_3 |
| ![Preview](./svg/allergen_mode.svg) | allergen_mode |
| ![Preview](./svg/purification_only_mode.svg) | purification_only_mode |
| ![Preview](./svg/two_in_one_mode.svg) | two_in_one_mode |
| ![Preview](./svg/bacteria_virus_mode.svg) | bacteria_virus_mode |
| ![Preview](./svg/pollution_mode.svg)      | pollution_mode |
| ![Preview](./svg/nanoprotect_filter.svg)  | nanoprotect_filter |
| ![Preview](./svg/filter_replacement.svg)  | filter_replacement |
| ![Preview](./svg/water_refill.svg)        | water_refill |
| ![Preview](./svg/prefilter_cleaning.svg)  | prefilter_clearning |
| ![Preview](./svg/prefilter_wick_cleaning.svg) | prefilter_wick_cleaning |
| ![Preview](./svg/pm25.svg) | pm25 |
| ![Preview](./svg/iai.svg)  | iai |
| ![Preview](./svg/wifi.svg) | wifi |
| ![Preview](./svg/reset.svg) | reset |
| ![Preview](./svg/circulate.svg) | circulate |
| ![Preview](./svg/clean.svg) | clean |
| ![Preview](./svg/mode.svg) | mode |
| ![Preview](./svg/pm25b.svg) | pm25b |
| ![Preview](./svg/rotate.svg) | rotate |
| ![Preview](./svg/oscillate.svg) | oscillate |
| ![Preview](./svg/heating.svg)   | heating |
| ![Preview](./svg/gas.svg)       |gas |


## Install

### HACS
Add `https://github.com/kongo09/hass-pap-icons` as custom-repository for a Lovelace plugin in [HACS](https://hacs.xyz/docs/faq/custom_repositories/)

### Manual
Copy the `hass-pap-icons.js` file into `<config>/www/` where `<config>` is your home-assistant config directory (the directory where your `configuration.yaml` resides).

Add the folowing to the `frontend` section of your `configuration.yaml`

```yaml
frontend:
  extra_module_url:
    - /local/hass-pap-icons.js
```

Or add the following to your lovelace configuration using the Raw Config editor under Configure UI or ui-lovelace.yaml if using YAML mode.

```yaml
resources:
  - type: js
    url: /local/hass-pap-icons.js
```

Restart home-assistant.

## Using
The icons use the prefix `pap:`. They are compatible with the icon picker, so you can search for them in the entity configuration UI by typing `pap:` into the box.

Example:

```
type: entity
entity: fan.air_ac2729
icon: 'pap:power_button'
```

## FAQ
Q: The icon ain't showing, it's just white space where it should be. What's up with that?

A: Probably related to cache. Try opening your instance in a incognito/private Window and see if your icon shows then. If yes, it's cache related. If not, spellcheck.

Q: The icons look great, but what Lovelace card would you recommend to make use of them?

A: Great question - I couldn't find one either that takes advantage of the Philips devices. So I used a `lovelace-button-card` to create one. You can find it here: https://community.home-assistant.io/t/lovelace-button-card/65981/4938?u=kongo09

Q: I cannot get my Philips Air Purifier to work with Home Assistant. I know this is off-topic for an icon pack, but how did you do that?

A: The best way is the great integration by @betaboon which can find here: https://github.com/betaboon/philips-airpurifier

## Thanks
Thanks to @hulkhaugen, as I used his hass-bha-icons based on hass-fontawesome from @thomasloven as a template for this pack
