# team.prefs.get
This method returns the preferences set for the workspace(team) of the provided token.

## Arguments
This method has the URL `https://slack.com/api/team.prefs.get` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: read, needs client token)

## Response
If successful you will return the preferences set for the current workspace in JSON

```json
{
    "ok": true,
    "prefs": {
        "admin_customized_quick_reactions": [
            "white_check_mark",
            "eyes",
            "raised_hands"
        ],
        "all_users_can_purchase": true,
        "allow_admin_retention_override": 0,
        "allow_calls": true,
        "allow_calls_interactive_screen_sharing": true,
        "allow_retention_override": false,
        "app_management_apps": [
            "A024VLLMF54"
        ],
        "app_whitelist_enabled": true,
        "auth_mode": "normal",
        "billing_wdf_customer_id": null,
        "block_file_download": false,
        "can_receive_shared_channels_invites": true,
        "content_review_enabled": false,
        "custom_status_site": null,
        "disable_file_deleting": false,
        "disable_file_editing": false,
        "display_external_email_addresses": true,
        "display_pronouns": false,
        "dm_retention_duration": 3,
        "dm_retention_type": 2,
        "enable_connect_dm_early_access": false,
        "enable_domain_allowlist_for_cea": false,
        "ent_required_browser": null,
        "enterprise_default_channels": [],
        "enterprise_intune_enabled": false,
        "enterprise_mandatory_channels": [],
        "enterprise_mdm_disable_file_download": false,
        "enterprise_mobile_device_check": false,
        "file_retention_duration": 3,
        "file_retention_type": 1,
        "flagged_content_review_channel": null,
        "group_retention_duration": 3,
        "group_retention_type": 2,
        "has_hipaa_compliance": false,
        "identity_links_prefs": {
            "is_enabled": true,
            "teams_domains_ts": 1624447261
        },
        "invited_user_preset": {
            "enforce_tls": true
        },
        "member_analytics_disabled": false,
        "mobile_force_app_upgrade_min_version": null,
        "mobile_force_app_upgrade_versions_allowed": null,
        "mobile_passcode_timeout_in_seconds": -1,
        "notification_redaction_type": "REDACT_ALL_CONTENT",
        "notify_pending_enabled": true,
        "ntlm_credential_domains": "*",
        "private_channel_membership_limit": 0,
        "required_minimum_mobile_version": null,
        "retention_duration": 3,
        "retention_type": 2,
        "rimeto_org_instance_id": null,
        "signup_domains": null,
        "signup_mode": null,
        "slack_connect_allowed_workspaces": {
            "type": [
                "ALL"
            ]
        },
        "slack_connect_approval_type": null,
        "slack_connect_dm_only_verified_orgs": false,
        "sso_auth_restrictions": null,
        "sso_choose_username": null,
        "who_can_dm_anyone": {
            "type": [
                "EVERYONE"
            ]
        },
        "who_can_manage_guests": {
            "type": [
                "admin"
            ],
            "user": [],
            "subteam": []
        },
        "who_can_manage_private_channels": {
            "type": [
                "ORG_ADMINS_AND_OWNERS"
            ],
            "user": [],
            "subteam": []
        },
        "who_can_manage_private_channels_at_workspace_level": {
            "user": [],
            "type": [
                "NO_ONE"
            ]
        },
        "who_can_manage_public_channels": {
            "user": [],
            "type": []
        },
        "who_can_manage_shared_channels": {
            "type": [
                "admin"
            ]
        },
        "who_can_post_in_shared_channels": {
            "type": [
                "ra"
            ]
        },
        "who_can_review_flagged_content": {
            "type": [
                "ORG_AND_WORKSPACE_ADMINS_OWNERS"
            ]
        },
        "who_can_view_message_activity": {
            "type": [
                "TOPLEVEL_ADMINS_AND_OWNERS"
            ]
        },
        "invites_only_admins": true,
        "show_join_leave": false,
        "discoverable": "invite_only",
        "enterprise_jointeam_requests": {
            "admin_notification_methods": [],
            "admin_notification_channels": []
        },
        "locale": "en-US",
        "invite_requests_enabled": true,
        "default_channels": [
            "C024JHFDDT8",
            "C0253V45NCR"
        ],
        "stats_only_admins": true,
        "disallow_public_file_urls": true,
        "who_can_archive_channels": "admin",
        "who_can_create_channels": "admin",
        "who_can_create_groups": "admin",
        "who_can_kick_channels": "admin",
        "who_can_kick_groups": "admin",
        "who_can_manage_channel_posting_prefs": "ra",
        "allow_huddles": true,
        "allow_message_deletion": true,
        "calls_locations": [],
        "commands_only_regular": null,
        "custom_status_default_emoji": ":speech_balloon:",
        "custom_status_presets": [
            [
                ":spiral_calendar_pad:",
                "In a meeting",
                "In a meeting",
                "1_hour"
            ],
            [
                ":bus:",
                "Commuting",
                "Commuting",
                "30_minutes"
            ],
            [
                ":face_with_thermometer:",
                "Out sick",
                "Out sick",
                "all_day"
            ],
            [
                ":palm_tree:",
                "Vacationing",
                "Vacationing",
                "no_expiration"
            ],
            [
                ":house_with_garden:",
                "Working remotely",
                "Working remotely",
                "all_day"
            ]
        ],
        "default_rxns": [
            "simple_smile",
            "thumbsup",
            "white_check_mark",
            "heart",
            "eyes"
        ],
        "disable_email_ingestion": false,
        "disable_file_uploads": "allow_all",
        "disable_sidebar_connect_prompts": [],
        "disable_sidebar_install_prompts": [],
        "display_email_addresses": true,
        "display_real_names": false,
        "dnd_after_friday": "22:00",
        "dnd_after_monday": "22:00",
        "dnd_after_saturday": "22:00",
        "dnd_after_sunday": "22:00",
        "dnd_after_thursday": "22:00",
        "dnd_after_tuesday": "22:00",
        "dnd_after_wednesday": "22:00",
        "dnd_before_friday": "08:00",
        "dnd_before_monday": "08:00",
        "dnd_before_saturday": "08:00",
        "dnd_before_sunday": "08:00",
        "dnd_before_thursday": "08:00",
        "dnd_before_tuesday": "08:00",
        "dnd_before_wednesday": "08:00",
        "dnd_days": "every_day",
        "dnd_enabled": true,
        "dnd_enabled_friday": "partial",
        "dnd_enabled_monday": "partial",
        "dnd_enabled_saturday": "partial",
        "dnd_enabled_sunday": "partial",
        "dnd_enabled_thursday": "partial",
        "dnd_enabled_tuesday": "partial",
        "dnd_enabled_wednesday": "partial",
        "dnd_end_hour": "08:00",
        "dnd_start_hour": "22:00",
        "dnd_weekdays_off_allday": false,
        "emoji_only_admins": null,
        "enable_shared_channels": 2,
        "hide_gsuite_invite_option": false,
        "hide_referers": true,
        "invite_requests_approval_channel": null,
        "joiner_notifications_enabled": null,
        "loading_only_admins": null,
        "loud_channel_mentions_limit": 10000,
        "msg_edit_window_mins": -1,
        "sign_in_with_slack_disabled": false,
        "slack_connect_file_upload_sharing_enabled": true,
        "slackbot_responses_disabled": false,
        "slackbot_responses_only_admins": null,
        "subteams_auto_create_admin": false,
        "subteams_auto_create_owner": false,
        "use_browser_picker": false,
        "username_policy": null,
        "uses_customized_custom_status_presets": false,
        "warn_before_at_channel": "always",
        "welcome_place_enabled": false,
        "who_can_at_channel": "ra",
        "who_can_at_everyone": "regular",
        "who_can_change_team_profile": "admin",
        "who_can_create_channel_email_addresses": {
            "type": [
                "regular"
            ]
        },
        "who_can_create_delete_user_groups": "admin",
        "who_can_create_shared_channels": "admin",
        "who_can_create_workflows": {
            "type": [
                "regular"
            ]
        },
        "who_can_edit_user_groups": "admin",
        "who_can_manage_integrations": {
            "type": [
                "regular"
            ]
        },
        "who_can_post_general": "ra",
        "who_can_use_hermes": {
            "type": [
                "regular"
            ]
        },
        "workflow_extension_steps_enabled": false,
        "workflows_export_csv_enabled": false,
        "workflows_webhook_trigger_enabled": false,
        "channel_email_addresses_enabled": true,
        "custom_contact_email": null,
        "default_theme": null,
        "dev_company_segment": null,
        "enable_info_barriers": false,
        "enable_mpdm_to_private_channel_conversion": true,
        "enterprise_has_corporate_exports": false,
        "external_shared_channel_requests_approval_channel": null,
        "max_file_upload_size": null,
        "received_esc_route_to_channel_awareness_message": false,
        "single_user_exports": false,
        "who_can_manage_ext_shared_channels": {
            "type": [
                "ORG_ADMINS_AND_OWNERS"
            ]
        },
        "who_can_request_ext_shared_channels": {
            "type": [
                "EVERYONE"
            ]
        },
        "workflow_builder_enabled": true,
        "box_app_installed": false,
        "calls_apps": {
            "video": [
                {
                    "id": "A00",
                    "name": "Slack",
                    "image": "img/slack_hash_128.png"
                }
            ],
            "audio": []
        },
        "compliance_export_start": 0,
        "created_with_google": false,
        "default_channel_creation_enabled": false,
        "dropbox_legacy_picker": false,
        "file_limit_whitelisted": false,
        "filepicker_app_first_install": false,
        "gdrive_enabled_team": false,
        "gg_enabled": false,
        "has_compliance_export": false,
        "has_seen_partner_promo": false,
        "in_shared_channels_day1_creator": null,
        "onedrive_app_installed": false,
        "onedrive_enabled_team": false,
        "self_serve_select": false,
        "show_legacy_paid_benefits_page": false,
        "workflow_extension_steps_beta_opt_in": false,
        "invites_limit": true
    }
}
```
In case of errors you will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics).
## Errors & Warnings
Error|Description
--------|-------
tbd