# PHPUnit extension for Chassis

Install PHPUnit within your [Chassis](http://chassis.io/) box! The PHPUnit extension automatically sets up your Chassis instance with the `phpunit` executable, for use running PHP unit tests.

## Activation

### Automated Installation

To add the phpunit extension to a Chassis box, include `chassis/phpunit` in the `extensions` list within your `config.local.yaml` file:

```yml
extensions:
    - chassis/phpunit
```

Then run `vagrant provision` to instruct Chassis to download and install the new extension.

### Manual Installation

Ensure you have a Chassis instance set up locally already.

```
#### In your Chassis dir:
cd extensions

#### Grab the extension
git clone --recursive https://github.com/Chassis/phpunit.git phpunit

#### Reprovision
cd ..
vagrant provision
```

## Usage
```
vagrant ssh
cd /vagrant/content/{plugins|themes}/yourdirectory
phpunit
```

You're now ready to run `phpunit` within your Chassis virtual machine!
