# Changelog

All notable changes to Vagou are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2026-09-25

### Changed
- Found slots now come with a reminder to confirm the times in the Humana app before booking.

## [0.3.0] - 2026-09-24

### Added
- "Todas as unidades": a doctor-name watch can now search every unit of the specialty, like the official app's name search, instead of only the units you picked. The editor shows where a matching doctor works.
- A watch can combine doctors you picked with a doctor name: you get slots from the picked doctors and from anyone whose name matches.

### Changed
- Changing the units of a watch keeps the typed doctor name and the picked doctors that still work there.

### Fixed
- Watches by doctor name or for any doctor now see a doctor who just opened an online agenda at the next check, instead of up to 24 hours later.

## [0.2.0] - 2026-09-24

### Added
- A silent persistent notification shows how many watches are running and when the next check is. Its "Desativar" button turns it off until you switch it back on in Ajustes > Notificação fixa.

### Fixed
- Specialties such as Cardiologia no longer fail to list doctors when some of their units have no doctor with an online agenda; those units just show none.
- When a unit's doctor list can't be loaded, the other units still show, and you can still watch any doctor by name.
- A check over several units no longer fails as a whole when one unit answers in an unexpected format; that unit is skipped and the others are checked.

## [0.1.0] - 2026-09-24

First pilot build. Vagou watches your health plan's agenda from your phone and notifies you when a slot opens with the doctor you want. Everything stays on the phone: no server, no account, no telemetry.

### Added
- Humana Saúde Nordeste support: connect with your beneficiary portal login, see the plans and patients (holder and dependents) found on the account, and pick specialties, units and doctors from the portal's own lists.
- Watches: choose the plan, patient, specialty and one or more units, then any doctor, specific doctors, or any doctor whose name contains what you type. Limit them by dates, weekdays and time of day, and set how often to check: as often as every 10 minutes, with a higher minimum for watches that cover many doctors.
- Background checks that keep running with the app closed, and a notification as soon as a new slot appears, with a shortcut to the plan's official app to book it.
- Alerts when an account needs you (wrong password, locked account, new terms to accept on the portal): its checks pause until you resume them, and Vagou never accepts anything for you.
- Notices when the plan portal is down or checks are running late.
- Watch details with the open slots found, grouped by day and by doctor, each doctor in its own color, with a doctor filter. Taken and past slots drop off the list.
- Activity history of what was checked and found.
- Accounts screen with your plan cards (carteirinhas).
- Demo provider ("Demonstração") with fake data, to try every screen without a plan login.
- Settings: light theme by default (dark or follow the system), discreet notifications that only say "Nova vaga encontrada", lock-screen details on or off, pause everything, a diagnostics report without personal data, and "Apagar tudo" to erase everything Vagou stored on the phone.
- Terms of Use and Privacy Policy to accept on first launch, readable any time from Settings.

### Fixed
- Humana login no longer stops at the plan step, blocked by the portal's Cloudflare protection.
- Links to the Privacy Policy inside the Terms of Use now open the policy.
- On accounts with more than one plan, checks for a plan now run in that plan's portal session. Before, they could run in the last plan selected and find nothing, or the wrong slots.
- A slot that drops out of one check and comes back is no longer shown as taken, and editing what a watch searches for starts its results fresh instead of marking the old ones as taken.
- "Verificar agora" says when the next manual check unlocks instead of doing nothing.

### Security
- Passwords, sessions and all app data are encrypted with a key kept in the Android Keystore, and are left out of backups and device transfers.
- Vagou talks only to the plan portal's own addresses, over HTTPS, trusting only the system's certificates. No analytics, crash reporting or ads.
- The login screen can't be captured in screenshots or the recent-apps preview.

