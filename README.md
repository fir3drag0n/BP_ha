# BP_ha – Home Assistant blueprints

Blueprints used in my Home Assistant setup. Some are my own, some are maintained forks of
community blueprints that are no longer updated upstream.

| Blueprint | Origin | Notes |
|---|---|---|
| `dynamische_abdeckung_v22.yaml` | own | Cover control with priorities, hysteresis, blockers and tilt |
| `weather_notification.yaml` | own | Weather forecast notification for today and tomorrow |
| `actionable-notifications-for-android.yaml` | – | Actionable notifications for Android |
| `notification-if-door-or-window-is-left-open.yaml` | [community thread (2022)](https://community.home-assistant.io/t/notification-if-door-or-window-is-left-open/402851) | v2.0: fixed escaped default values, current syntax, `strftime` time in the default message, optional *clear notification when closed* |
| `cabinet_light.yaml` | [OliverHi/blueprints](https://github.com/OliverHi/blueprints/blob/main/cabinet_light.yaml) (2023) | v2.0: configurable timeout, ignores `unavailable` → `on` after restarts |
| `tts-door-opening.yaml` | [rokam's gist](https://gist.github.com/rokam/22fd6e497fbe61478fda4d0fc8215abf) (2024) | v2.0: optional TTS entity via `tts.speak` (falls back to `tts.google_translate_say`), several persons and media players selectable, current syntax |
| `low_battery_notification.yaml` | based on [sbyx's low battery gist](https://gist.github.com/sbyx/1f6f434f0903b872b84c4302637d0890) | v1.0: one entry per device (merges Battery Notes `battery_plus`/`_low`), exclusions by entity/device/label, device names, battery type, variables `sensors`, `sensors_list`, `sensors_count` |

Related fork: [hassio_appliance-status-monitor](https://github.com/fir3drag0n/hassio_appliance-status-monitor)
(leofabri's appliance status monitor, v3 with fixes).

All forked blueprints keep their existing input names, so automations created from the
original versions keep working after an update.
