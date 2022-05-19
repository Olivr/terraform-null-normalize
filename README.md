# terraform-null-normalize

Normalize strings (replace accents, trim special characters).

## Usage

```sh
terraform plan --var string='Héloïse!'

Changes to Outputs:
  + latinized  = "Heloise!"
  + lower      = "heloise"
  + normalized = "Heloise"
  + title      = "Heloise"
  + upper      = "HELOISE"
```

<!-- BEGIN_TF_DOCS -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_string"></a> [string](#input\_string) | String to normalize. | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_latinized"></a> [latinized](#output\_latinized) | Latinized string (only special letters have been replaced). |
| <a name="output_lower"></a> [lower](#output\_lower) | Normalized string in lower case. |
| <a name="output_normalized"></a> [normalized](#output\_normalized) | Normalized string (special letters replaced and trimmed of other symbold except numbers and '-'). |
| <a name="output_title"></a> [title](#output\_title) | Normalized string in title case. |
| <a name="output_upper"></a> [upper](#output\_upper) | Normalized string in upper case. |
<!-- END_TF_DOCS -->

## Contributing

All contributions are welcome!

Generate documentation with `terraform-docs .`

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details
