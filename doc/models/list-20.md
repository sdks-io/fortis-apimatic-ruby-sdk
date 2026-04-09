
# List 20

## Structure

`List20`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_number` | `String` | Optional | Account Number |
| `branding_domain_url` | `String` | Optional | Branding Domain Url<br><br>**Constraints**: *Maximum Length*: `64` |
| `cell_phone` | `String` | Optional | Cell Phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `company_name` | `String` | Optional | Company Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `contact_id` | `String` | Optional | Contact Id Information on `expand` |
| `date_of_birth` | `String` | Optional | Date Of Birth<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `domain_id` | `String` | Optional | Domain<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `email` | `String` | Optional | Email<br><br>**Constraints**: *Maximum Length*: `128` |
| `email_trx_receipt` | `TrueClass \| FalseClass` | Optional | Email Trx Receipt |
| `home_phone` | `String` | Optional | Home Phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `first_name` | `String` | Optional | First Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `last_name` | `String` | Optional | Last Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `locale` | `String` | Optional | Locale<br><br>**Constraints**: *Maximum Length*: `8` |
| `office_phone` | `String` | Optional | Office Phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `office_ext_phone` | `String` | Optional | Office Ext Phone<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^\d{1,10}$` |
| `primary_location_id` | `String` | Optional | Primary Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `requires_new_password` | `String` | Optional | Requires New Password<br><br>**Constraints**: *Maximum Length*: `1` |
| `terms_condition_code` | `String` | Optional | Terms Condition (This field is required when updating your own password). |
| `tz` | `String` | Optional | Time zone<br><br>**Constraints**: *Maximum Length*: `30` |
| `ui_prefs` | [`UiPrefs`](../../doc/models/ui-prefs.md) | Optional | Ui Prefs |
| `username` | `String` | Optional | Username<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `64` |
| `user_api_key` | `String` | Optional | User Api Key<br><br>**Constraints**: *Minimum Length*: `16`, *Maximum Length*: `64` |
| `user_hash_key` | `String` | Optional | User Hash Key<br><br>**Constraints**: *Minimum Length*: `24`, *Maximum Length*: `36` |
| `user_type_code` | [`UserTypeCodeEnum`](../../doc/models/user-type-code-enum.md) | Optional | User Type |
| `password` | `String` | Optional | Password<br><br>**Constraints**: *Minimum Length*: `8`, *Maximum Length*: `128`, *Pattern*: ``^(?=.*[`!@#$%^&*()_+\-=\[\]{};':"\\\|,.<>\/?~])(?=.*[0-9])(?=.*[a-zA-Z]).*$`` |
| `zip` | `String` | Optional | Zip<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_api_id` | `String` | Optional | ContactApi Id |
| `primary_location_api_id` | `String` | Optional | Primary LocationApi ID |
| `status_code` | [`StatusCodeEnum`](../../doc/models/status-code-enum.md) | Optional | Status Code |
| `api_only` | `TrueClass \| FalseClass` | Optional | API Only |
| `is_invitation` | `TrueClass \| FalseClass` | Optional | Is Invitation |
| `address` | [`Address2`](../../doc/models/address-2.md) | Optional | Address |
| `id` | `String` | Optional | User ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `status` | `TrueClass \| FalseClass` | Optional | Status |
| `login_attempts` | `Integer` | Optional | Login Attempts |
| `last_login_ts` | `Integer` | Optional | Last Login |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | Created User<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `terms_accepted_ts` | `Integer` | Optional | Terms Accepted |
| `terms_agree_ip` | `String` | Optional | Terms Agree Ip<br><br>**Constraints**: *Maximum Length*: `16` |
| `current_date_time` | `String` | Optional | Current Date Time<br><br>**Constraints**: *Maximum Length*: `24` |
| `current_login_ip` | `String` | Optional | Current Login Ip |
| `current_login` | `Integer` | Optional | Current Login Timestamp |
| `sftp_access` | `TrueClass \| FalseClass` | Optional | SFTP Access |
| `log_api_response_body_ts` | `Integer` | Optional | Log Api Response Body |
| `locations` | [`Array[Location18]`](../../doc/models/location-18.md) | Optional | Location Information on `expand` |
| `primary_location` | [`PrimaryLocation`](../../doc/models/primary-location.md) | Optional | Primary Location Information on `expand` |
| `received_emails` | [`Array[ReceivedEmail]`](../../doc/models/received-email.md) | Optional | Received Email Information on `expand` |
| `contact` | [`Contact1`](../../doc/models/contact-1.md) | Optional | Contact Information on `expand` |
| `is_deletable` | `TrueClass \| FalseClass` | Optional | Is Deletable Information on `expand` |
| `active_notification_alerts` | [`Array[ActiveNotificationAlert]`](../../doc/models/active-notification-alert.md) | Optional | Active Notification Alert Information on `expand` |
| `location_users` | [`Array[LocationUser]`](../../doc/models/location-user.md) | Optional | Location User Information on `expand` |
| `auth_roles` | [`Array[AuthRole]`](../../doc/models/auth-role.md) | Optional | Auth Role Information on `expand` |
| `changelogs` | [`Array[Changelog]`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `resources` | [`Resources`](../../doc/models/resources.md) | Optional | Resource Information on `expand` |
| `domain` | [`Domain`](../../doc/models/domain.md) | Optional | Domain Information on `expand` |
| `created_user` | [`CreatedUser`](../../doc/models/created-user.md) | Optional | User Information on `expand` |
| `location_marketplaces` | [`Array[Locationmarketplace]`](../../doc/models/locationmarketplace.md) | Optional | Locationmarketplaces Information on `expand` |
| `email_blacklist` | [`EmailBlacklist`](../../doc/models/email-blacklist.md) | Optional | Email Blacklist Information on `expand` |
| `helppage` | [`Helppage2`](../../doc/models/helppage-2.md) | Optional | Helppage Information on `expand` |

## Example (as JSON)

```json
{
  "account_number": "5454545454545454",
  "branding_domain_url": "{branding_domain_url}",
  "cell_phone": "3339998822",
  "company_name": "Fortis Payment Systems, LLC",
  "contact_id": "Sample contact ID",
  "date_of_birth": "2021-12-01",
  "domain_id": "11e95f8ec39de8fbdb0a4f1a",
  "email": "email@domain.com",
  "email_trx_receipt": true,
  "home_phone": "3339998822",
  "first_name": "John",
  "last_name": "Smith",
  "locale": "en-US",
  "office_phone": "3339998822",
  "office_ext_phone": "5",
  "primary_location_id": "11e95f8ec39de8fbdb0a4f1a",
  "terms_condition_code": "20220308",
  "tz": "America/New_York",
  "username": "{user_name}",
  "user_api_key": "234bas8dfn8238f923w2",
  "user_type_code": 100,
  "zip": "48375",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "status_code": 1,
  "api_only": false,
  "is_invitation": false,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "status": true,
  "login_attempts": 0,
  "last_login_ts": 1422040992,
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "terms_accepted_ts": 1422040992,
  "terms_agree_ip": "192.168.0.10",
  "current_login": 1422040992,
  "log_api_response_body_ts": 1422040992,
  "isDeletable": true
}
```

