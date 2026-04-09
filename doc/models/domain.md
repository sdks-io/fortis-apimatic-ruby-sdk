
# Domain

Domain Information on `expand`

## Structure

`Domain`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `String` | Optional | URL<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+([\-\.]{1}[a-zA-Z0-9]+)*\.[a-zA-Z]{2,5}$` |
| `title` | `String` | Optional | Domain Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `logo` | `String` | Optional | Logo<br><br>**Constraints**: *Maximum Length*: `64` |
| `support_email` | `String` | Optional | Support Email<br><br>**Constraints**: *Maximum Length*: `64` |
| `allow_contact_signup` | `TrueClass \| FalseClass` | Optional | Allow Contact Signup. |
| `allow_contact_registration` | `TrueClass \| FalseClass` | Optional | Allow Contact Registration. |
| `allow_contact_login` | `TrueClass \| FalseClass` | Optional | Allow Contact Login. |
| `registration_fields` | [`Array[RegistrationFieldEnum]`](../../doc/models/registration-field-enum.md) | Optional | Registration Fields |
| `company_name` | `String` | Optional | Company Name.<br><br>**Constraints**: *Maximum Length*: `32` |
| `nav_color` | `String` | Optional | Nav Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `button_primary_color` | `String` | Optional | Button Primary Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `logo_background_color` | `String` | Optional | Logo Background Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `icon_background_color` | `String` | Optional | Icon Background Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `menu_text_background_color` | `String` | Optional | Menu Text Background Color<br><br>**Constraints**: *Maximum Length*: `7` |
| `menu_text_color` | `String` | Optional | Menu Text Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `right_menu_background_color` | `String` | Optional | Right Menu Background Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `right_menu_text_color` | `String` | Optional | Right Menu Text Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `button_primary_text_color` | `String` | Optional | Button Primary Text Color.<br><br>**Constraints**: *Maximum Length*: `7` |
| `nav_logo` | `String` | Optional | Nav Logo.<br><br>**Constraints**: *Maximum Length*: `256` |
| `fav_icon` | `String` | Optional | Fav Icon.<br><br>**Constraints**: *Maximum Length*: `256` |
| `aes_key` | `String` | Optional | Aes Key.<br><br>**Constraints**: *Maximum Length*: `255` |
| `help_text` | `String` | Optional | Help Text. |
| `email_reply_to` | `String` | Optional | Email Reply To. |
| `email` | `String` | Optional | Email. |
| `custom_javascript` | `String` | Optional | Custom Javascript.<br><br>**Constraints**: *Maximum Length*: `2048`, *Pattern*: `^<script\b[^>]*>([\s\S]*?)<\/script>$` |
| `custom_theme` | `String` | Optional | Custom Theme<br><br>**Constraints**: *Maximum Length*: `48` |
| `custom_css` | `String` | Optional | Custom CSS<br><br>**Constraints**: *Maximum Length*: `2048` |
| `contact_user_default_entry_page` | [`ContactUserDefaultEntryPageEnum`](../../doc/models/contact-user-default-entry-page-enum.md) | Optional | Contact User Default Entry Page |
| `contact_user_default_auth_roles` | `Array[Object]` | Optional | Contact User Default Auth Role |
| `custom_stylesheet_url` | `String` | Optional | Custom Stylesheet URL<br><br>**Constraints**: *Maximum Length*: `256` |
| `id` | `String` | Optional | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |

## Example (as JSON)

```json
{
  "url": "fortispayrbyn9y.sandbox.zeamster.com",
  "title": "Test Brand Domain Title 2",
  "support_email": "email@domain.com",
  "allow_contact_signup": true,
  "allow_contact_registration": true,
  "allow_contact_login": true,
  "registration_fields": [
    "id",
    "email"
  ],
  "email_reply_to": "email@domain.com",
  "email": "email@domain.com",
  "contact_user_default_entry_page": "dashboard",
  "custom_stylesheet_url": "https://127.0.0.1/receiver",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "logo": "logo0"
}
```

