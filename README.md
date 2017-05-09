# Satellite 6 Registration

A basic playbook for registering clients to a Satellite 6 host.

## Installation

This playbook uses the bootstrap.py script shipped with Satellite 6.

## Usage

`ansible-playbook -i hosts sat_bootstrap.yml -e @extra_vars.yml`

The hosts file provided is basic.  Modify as needed.
The extra_vars file should be populated as needed, and a sample file is provided here.

This playbook adds the host to Autosign in the Satellite configuration.  Currently you need to change a setting in Satellite.
Navigate to Administer-->Settings-->Provisioning-->Manage PuppetCA and set this to `false`
Without changing this setting you will need to manually sign the certificate request in Satellite, as boostrap creates the host record
after the autosign config has taken place, which removes the entry.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Credits

Author - Tim Fairweather, Arctiq

## License

GNU GENERAL PUBLIC LICENSE
see LICENSE.md