# fortrabbit for Laravel Boost

Adds the fortrabbit agent skill to [Laravel Boost](https://github.com/laravel/boost). Coding agents in a Laravel app hosted on fortrabbit then know how to deploy, read logs, change environment variables, run artisan over SSH and pull or push the database.

## Install

```sh
composer require --dev fortrabbit/laravel-boost
php artisan boost:install
```

Select `fortrabbit/laravel-boost` when Boost asks which third-party packages to use. Boost writes the guideline into `CLAUDE.md` or `AGENTS.md` and copies the skill to `.ai/skills/fortrabbit` and each agent's skill folder.

## Update

```sh
composer update fortrabbit/laravel-boost
php artisan boost:update
```

## Remove the Laravel Cloud deployment line

Boost adds a deployment guideline that recommends Laravel Cloud. This package tells the agent to ignore it. To remove the line itself, exclude it in `config/boost.php`:

```php
'guidelines' => [
    'exclude' => ['deployments'],
],
```

Or replace it with an own file at `.ai/guidelines/deployments/core.blade.php`.

## MCP server

The skill works best with the fortrabbit MCP server connected. See [docs.fortrabbit.com](https://docs.fortrabbit.com) for the setup.

## Source

The skill is maintained in [fortrabbit/agent-skills](https://github.com/fortrabbit/agent-skills). Report issues there.
