**You may want to use dynamic values in your newsletter. That's what these placeholders are used for!**

For every custom string you can modify in the configuration file `config.yml`, you can insert placeholders that will be replaced in the final email. 

### Example 
Let's customize the email subject. 

In `config.yml`: 

```yml
email_template:
  language: "en"
  subject: "New addition of {month_name}"
```

Result: 

<img width="261" alt="Capture d’écran 2025-06-19 à 11 51 55" src="https://github.com/user-attachments/assets/33a8909d-fd00-4a6f-8292-89f3a7618da5" />

> [!Note]
> Change the `language` field to one of the supported languages to get the localized date name!

### Available placeholders 

Currently, the following placeholders are available: 

| Placeholder | Example | Description |
|---|---|---|
| `{date}` | `2025-06-19` | Date of the day. Format `YYYY-MM-DD`. |
| `{day_name}` | `Monday` | Today's day name, localized. |
| `{day_number}` | `19` | Today's day of the month as a number. |
| `{month_name}` | `June` | Current month name, localized. |
| `{month_number}` | `06` | Current month number. |
| `{year}` | `2025` | Current year. |
| `{start_date}` | `2025-05-18` | The first date new additions are taken into account. Depends on `observed_period_days` config parameter. Format `YYYY-MM-DD`. |
| `{start_day_name}` | `Sunday` | Day name of the first observed date. |
| `{start_day_number}` | `19` | Day of the first observed date as a number. |
| `{start_month_name}` | `May` | Month name of the first observed date. |
| `{start_month_number}` | `05` | Month of the first observed date as a number. |
| `{start_year}` | `2025` | Year of the first observed date. |

> [!Note]
> Don't see what you are looking for? [Open an issue](https://github.com/SeaweedbrainCY/jellyfin-newsletter/issues) to request a new custom value!

> [!Warning]
> If you try using a placeholder that doesn't exist, the placeholder key `{example_placeholder}` will not be replaced in the final email.
