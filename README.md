# Netbox Device Template and Device Component Template Generator Playbook

This playbook takes the YAML devicetype-libraries style YAML files and leverages the netbox-community ansible_modules to provision them into Netbox

## Prerequisites

This playbook requires the netbox.netbox collection from ansible-galaxy. To install:\
`ansible-galaxy collection install netbox.netbox`

YAML models of devices using the format found in the devicetype-library [found here](https://github.com/netbox-community/devicetype-library)

## Usage

Place YAML files in the `devicetype-library/device-types/` directory from the root of this package. The playbook will search recursively one directory deep, so you can nest the template files in a subdirectory of that root. Alternatively, you can use the `--extra-vars` when you run the playbook and specify the parameter `template_dir` to an absolute path of the directory that you place your templates, as well as `nb_url` and `nb_token` to set your netbox variables. Otherwise, these will be taken from environment vars with the same name.

From the root of this package, run `ansible-playbook playbooks/00_create_device_type_templates.yaml`

## License

[MIT License](https://choosealicense.com/licenses/mit/)
