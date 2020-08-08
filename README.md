# Netbox Device Template and Device Component Template Generator Playbook

This playbook takes the YAML devicetype-libraries style YAML files and leverages the netbox-community ansible_modules to provision them into Netbox

## Prerequisites

This playbook requires the netbox.netbox collection from ansible-galaxy. To install:\
`ansible-galaxy collection install netbox.netbox`

YAML models of devices using the format found in the devicetype-library [found here](https://github.com/netbox-community/devicetype-library)

## Usage

Place YAML files in the `device_type_templates` directory at the root of this package. The playbook will search recursively one directory deep, so you can nest the template files in a subdirectory of that root. Alternatively, you can use the `--extra-vars` when you run the playbook and specify the parameter `rootdir` to an absolute path of the directory that you place your templates.

## License

[MIT License](https://choosealicense.com/licenses/mit/)