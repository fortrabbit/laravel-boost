# fortrabbit/laravel-boost

Composer package that ships the fortrabbit agent skill and a short guideline to Laravel Boost apps.

- `resources/boost/skills/fortrabbit/` is a copy of `plugins/fortrabbit/skills/fortrabbit` in `fortrabbit/agent-skills`. Never edit it here: change it there, the release copies it over.
- `resources/boost/guidelines/core.blade.php` is the only file maintained in this repo. Boost loads it into every agent session, so keep it to a few lines.
- Versions follow `VERSION` in agent-skills.
