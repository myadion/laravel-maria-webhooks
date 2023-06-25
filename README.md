# Adion's Laravel-Maria-Webhooks

Adion's `laravel-maria-webhooks` is a powerful package designed to seamlessly integrate your Laravel application with Adion's Artificial Intelligence service, Maria. With real-time responsiveness to Maria-triggered events, this package is essential for boosting automation and enhancing interaction within your application.

## Features

- Real-time reaction to events triggered by Maria.
- Customizable instruction sets for handling a variety of actions.
- Smooth integration with Laravel applications.
- Leverages Maria's capabilities to automate processes and manage client requests.

## Installation

Before you start, ensure you have [Composer](https://getcomposer.org/) installed.

To install `laravel-maria-webhooks`, run the following command in your project directory:

```bash
composer require adion/laravel-maria-webhooks
```

## Usage
After the package has been installed, your application can start receiving webhooks from Maria. Commands such as '/maria_please>' are declared in the Maria's recipe book on the Adion client space, not within the Laravel application itself. Once these commands are declared in the recipe book, the application can receive these webhooks.

For instance, to handle a pizza order, you might define the following in Maria's recipe book:

```
The pizza ordering procedure involves collecting the client's name, phone number, and order details including the type and quantity of pizzas.
To place the order:
/maria_please>post_new_order(String {_phone_number}, String $name, String $firstname, Json data).
```
This will generate a webhook to the `/adion/maria/post/new_order` endpoint of your Laravel application. Your application can then handle this webhook as required, such as by placing a pizza order.

Refer to our [official documentation](link-soon) for more information on how to setup these commands in Maria's recipe book and properly use the package.

## Configuration

After setting up the '/maria_please>' commands in Maria's recipe book, you may need to configure your server to properly receive webhooks from Maria. This could involve configuring firewalls, adjusting server settings, etc. The exact details will depend on your specific server setup.

Refer to our [official documentation](link-soon) for a detailed guide on how to configure `laravel-maria-webhooks` for your application.

## Contributing

We welcome contributions from the community. If you wish to contribute, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## Testing

`laravel-maria-webhooks` includes a suite of tests to ensure its functionality. To run the tests, use PHPUnit:

```bash
vendor/bin/phpunit
```

## License

This project is licensed under the [GNU General Public License v3.0](link-soon).

## Support

If you encounter any problems or have any questions about `laravel-maria-webhooks`, please open an issue on our GitHub repository or contact our support team at hello@myadion.com.

