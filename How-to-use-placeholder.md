**You might want to use dynamic values in your newsletter. That's what placeholder are used for !**

For every custom strings you can modify in the configuration file (`config.yml`), you can insert placeholders that will be replaced in the final email. 
### Available placeholders 
Currently, the following placeholders are available : 
| Placeholder | Description | Example | Version | 
|---|---|---|---|
|`{date}` | Date of the day. Format `Y-m-d`. | `2025-06-19` | `>= v0.5.0` |
|`{day_name}` | Today's day name, localized. | `Monday` | `>= v0.5.0` |
|`{day_number}` | Today's day number of the month. | `19` | `>= v0.5.0` |
|`{month_name}` | Current month name, localized. | `June` | `>= v0.5.0` |
|`{month_number}` | Current month number. | `06` | `>= v0.5.0` |
|`{year}` | Current year. | `2025` | `>= v0.5.0` |
|`{start_date}` | First date new addition are taken into account. Depends on `observed_period_days` config parameter.  Format `Y-m-d`. | `2025-05-18` | `>= v0.5.0` |
|`{start_day_name}` | Day name of the first observed date. | `Sunday` | `>= v0.5.0` |
|`{start_day_number}` | Day number of the first observed date. | `19` | `>= v0.5.0` |
|`{start_month_name}` | Month name of the first observed date. | `May` | `>= v0.5.0` |
|`{start_month_number}` | Month number of the first observed date. | `05` | `>= v0.5.0` |
|`{start_year}` | Year the first observed date. | `2025` | `>= v0.5.0` |

> [!Note]
> You don't see what you are looking for below ? [Open an issue](https://github.com/SeaweedbrainCY/jellyfin-newsletter/issues) to add support of your custom value !

> [!Warnin]
> If you try using a placeholder that doesn't exist, the placeholder key `{example_placeholder}` will not be replaced in the final email.

### Example 
Let's customize the email subject. 

In the `config.yml` file : 
```yml
[...]
email_template:
  language: "en"
  subject: "New addition of {month_name}"
[...]
```
Result : 

<img width="261" alt="Capture d’écran 2025-06-19 à 11 51 55" src="https://github.com/user-attachments/assets/33a8909d-fd00-4a6f-8292-89f3a7618da5" />

> [!Note]
> Change the `language` field with one of the supported language to get localized date name !
