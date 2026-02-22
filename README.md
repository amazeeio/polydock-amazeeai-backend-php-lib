# polydock-amazeeai-backend-php-lib

[![OpenSSF Scorecard](https://api.securityscorecards.dev/projects/github.com/amazeeio/polydock-amazeeai-backend-php-lib/badge)](https://securityscorecards.dev/viewer/?uri=github.com/amazeeio/polydock-amazeeai-backend-php-lib)

The Freedom Tech amazee.ai Private AI PHP library.

## Installation

```bash
composer require freedomtech-hosting/polydock-amazeeai-backend-client-php
```

## Requirements

- PHP 8.2 or higher
- ext-curl

## Usage

```php
use FreedomtechHosting\PolydockAmazeeAIBackendClient\Client;

$client = new Client('https://your-amazeeai-backend-url', 'your-api-token');
```

## Security

For security vulnerabilities, please use [GitHub's private vulnerability reporting](https://github.com/amazeeio/polydock-amazeeai-backend-php-lib/security/advisories/new).

## License

MIT
