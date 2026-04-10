# Polydock amazee.ai Backend PHP Library

The Freedom Tech **amazee.ai Private AI PHP library** provides a simple, object-oriented interface to interact with the amazee.ai backend API.

## Installation

Install the library via [Composer](https://getcomposer.org/):

```bash
composer require freedomtech-hosting/polydock-amazeeai-backend-client-php
```

## Requirements

- PHP 8.2 or higher
- `ext-curl` extension
- `ext-json` extension

## Basic Usage

To get started, instantiate the `Client` with your API base URL and an optional access token.

```php
use FreedomtechHosting\PolydockAmazeeAIBackendClient\Client;

$baseUrl = 'https://api.amazee.ai';
$accessToken = 'your-access-token';

$client = new Client($baseUrl, $accessToken);

// Example: Get current user info
try {
    $me = $client->getMe();
    print_r($me);
} catch (\Exception $e) {
    echo "Error: " . $e->getMessage();
}
```

### Authentication

If you don't have a token yet, you can login to receive one:

```php
$response = $client->login('user@example.com', 'password');
$token = $response['token']; // Depending on API response structure
```

### Working with Teams

```php
// List all teams
$teams = $client->listTeams();

// Create a new team
$newTeam = $client->createTeam('My Team', 'admin@example.com');
```

### Private AI Keys

```php
// List Private AI keys
$keys = $client->listPrivateAIKeys();

// Create a new Private AI key
$client->createPrivateAIKeys($regionId, 'my-key-name');
```

## Features

- **Authentication**: Login, Register, Logout, and Token management.
- **User Management**: Search, Create, Update, and Delete users.
- **Team Management**: Manage teams and user assignments.
- **Private AI Keys**: Manage your private AI keys and tokens.
- **Region Management**: List and manage regions (Admin).
- **Audit Logs**: Access system audit logs.
- **Health Check**: Monitor API health status.

## Debug Mode

Enable debug mode to see detailed request/response information in the console:

```php
$client = new Client($baseUrl, $accessToken, debug: true);
```

## License

This library is licensed under the **MIT License**. See the `LICENSE` file for details.
