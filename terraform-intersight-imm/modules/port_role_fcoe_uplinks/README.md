# port_role_fcoe_uplinks - Intersight Port Policy - Port Role - FCoE Uplink Terraform Module

## Usage

```hcl
module "port_role_fcoe_uplinks" {

  source = "terraform-cisco-modules/imm/intersight//modules/port_role_fcoe_uplinks"

  # omitted...
}
```

This module will Configure FCoE Uplink Port Roles in a Port Policy.

These resources are consumed

* [FCoE Uplinks](https://registry.terraform.io/providers/CiscoDevNet/intersight/latest/docs/resources/fabric_fcoe_uplink_role)

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_intersight"></a> [intersight](#provider\_intersight) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [intersight_fabric_fcoe_uplink_role.port_role](https://registry.terraform.io/providers/CiscoDevNet/intersight/latest/docs/resources/fabric_fcoe_uplink_role) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_admin_speed"></a> [admin\_speed](#input\_admin\_speed) | Admin configured speed for the port.<br>* Auto - Admin configurable speed AUTO ( default ).<br>* 1Gbps - Admin configurable speed 1Gbps.<br>* 10Gbps - Admin configurable speed 10Gbps.<br>* 25Gbps - Admin configurable speed 25Gbps.<br>* 40Gbps - Admin configurable speed 40Gbps.<br>* 100Gbps - Admin configurable speed 100Gbps. | `string` | `"Auto"` | no |
| <a name="input_breakout_port_id"></a> [breakout\_port\_id](#input\_breakout\_port\_id) | Breakout port Identifier of the Switch Interface.  When a port is not configured as a breakout port, the aggregatePortId is set to 0, and unused.  When a port is configured as a breakout port, the 'aggregatePortId' port number as labeled on the equipment, e.g. the id of the port on the switch. | `number` | `0` | no |
| <a name="input_fec"></a> [fec](#input\_fec) | Forward error correction configuration for the port.<br>* Auto - Forward error correction option 'Auto'.<br>* Cl91 - Forward error correction option 'cl91'.<br>* Cl74 - Forward error correction option 'cl74'. | `string` | `"Auto"` | no |
| <a name="input_link_control_policy_moid"></a> [link\_control\_policy\_moid](#input\_link\_control\_policy\_moid) | A reference to a fabricLinkControlPolicy resource. | `set(string)` | `[]` | no |
| <a name="input_port_list"></a> [port\_list](#input\_port\_list) | String of Ports to assign to the Port Policy. | `string` | `""` | no |
| <a name="input_port_policy_moid"></a> [port\_policy\_moid](#input\_port\_policy\_moid) | A reference to a fabricPortPolicy resource. | `string` | n/a | yes |
| <a name="input_slot_id"></a> [slot\_id](#input\_slot\_id) | Slot Identifier of the Switch/FEX/Chassis Interface. | `number` | `1` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | List of Tag Attributes to Assign to the Policy. | `list(map(string))` | `[]` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_moid"></a> [moid](#output\_moid) | Port Role - FCoE Uplink Managed Object ID (moid). |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
