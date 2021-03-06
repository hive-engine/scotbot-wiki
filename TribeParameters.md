```
{
    "$schema": "http://json-schema.org/draft-07/schema",
    "$id": "http://example.com/example.json",
    "type": "object",
    "title": "The root schema",
    "description": "The root schema comprises the entire JSON document.",
    "default": {},
    "examples": [
        {
            "author_curve_exponent": 1.0,
            "author_reward_percentage": 50.0,
            "beneficiaries_account": "h@leoburn",
            "beneficiaries_reward_percentage": 20.0,
            "cashout_window_days": 7.0,
            "curation_curve_exponent": 1.0,
            "disable_downvoting": false,
            "downvote_power_consumption": 2000,
            "downvote_regeneration_seconds": 432000,
            "downvote_window_days": -1,
            "enable_account_muting": true,
            "enable_comment_beneficiaries": true,
            "exclude_apps": null,
            "exclude_apps_from_token_beneficiary": "leofinance",
            "exclude_beneficiaries_accounts": "likwid,finex,sct.krwp,h@likwid,h@finex,h@sct.krwp,rewarding.app,h@rewarding.app",
            "exclude_tags": "actifit,steemhunt,appics,dlike,share2steem",
            "fee_post_account": null,
            "fee_post_amount": 0,
            "fee_post_exempt_beneficiary_account": null,
            "fee_post_exempt_beneficiary_weight": 0,
            "hive_community": "hive-167922",
            "hive_enabled": true,
            "hive_engine_enabled": true,
            "issue_token": true,
            "json_metadata_app_value": null,
            "json_metadata_key": "tags",
            "json_metadata_value": "leofinance,leo",
            "miner_tokens": "{\"LEOM\": 1, \"LEOMM\": 4}",
            "mining_pool_claim_number": 30,
            "mining_pool_claims_per_year": 8760,
            "muting_account": "noleo4u",
            "n_daily_posts_muted_accounts": 0,
            "other_pool_accounts": "{\"wleo.pool\": 15}",
            "other_pool_percentage": 15.0,
            "other_pool_send_token_per_year": 365,
            "pob_comment_pool_percentage": -1.0,
            "pob_pool_percentage": 70.0,
            "posm_pool_percentage": 15.0,
            "post_reward_curve": "default",
            "post_reward_curve_parameter": null,
            "promoted_post_account": "null",
            "reduction_every_n_block": 10512000,
            "reduction_percentage": 7.0,
            "rewards_token": 19.0,
            "rewards_token_every_n_block": 100,
            "staked_reward_percentage": 0.0,
            "staking_pool_claim_number": 0,
            "staking_pool_claims_per_year": 0,
            "staking_pool_percentage": 0.0,
            "steem_enabled": false,
            "steem_engine_enabled": false,
            "tag_adding_window_hours": 1.0,
            "token": "LEO",
            "token_account": "khaleelkazi",
            "use_staking_circulating_quotent": false,
            "vote_power_consumption": 200,
            "vote_regeneration_seconds": 432000,
            "vote_window_days": -1
        }
    ],
    "required": [
        "author_curve_exponent",
        "author_reward_percentage",
        "beneficiaries_account",
        "beneficiaries_reward_percentage",
        "cashout_window_days",
        "curation_curve_exponent",
        "disable_downvoting",
        "downvote_power_consumption",
        "downvote_regeneration_seconds",
        "downvote_window_days",
        "enable_account_muting",
        "enable_comment_beneficiaries",
        "exclude_apps",
        "exclude_apps_from_token_beneficiary",
        "exclude_beneficiaries_accounts",
        "exclude_tags",
        "fee_post_account",
        "fee_post_amount",
        "fee_post_exempt_beneficiary_account",
        "fee_post_exempt_beneficiary_weight",
        "hive_community",
        "hive_enabled",
        "hive_engine_enabled",
        "issue_token",
        "json_metadata_app_value",
        "json_metadata_key",
        "json_metadata_value",
        "miner_tokens",
        "mining_pool_claim_number",
        "mining_pool_claims_per_year",
        "muting_account",
        "n_daily_posts_muted_accounts",
        "other_pool_accounts",
        "other_pool_percentage",
        "other_pool_send_token_per_year",
        "pob_comment_pool_percentage",
        "pob_pool_percentage",
        "posm_pool_percentage",
        "post_reward_curve",
        "post_reward_curve_parameter",
        "promoted_post_account",
        "reduction_every_n_block",
        "reduction_percentage",
        "rewards_token",
        "rewards_token_every_n_block",
        "staked_reward_percentage",
        "staking_pool_claim_number",
        "staking_pool_claims_per_year",
        "staking_pool_percentage",
        "steem_enabled",
        "steem_engine_enabled",
        "tag_adding_window_hours",
        "token",
        "token_account",
        "use_staking_circulating_quotent",
        "vote_power_consumption",
        "vote_regeneration_seconds",
        "vote_window_days"
    ],
    "properties": {
        "author_curve_exponent": {
            "$id": "#/properties/author_curve_exponent",
            "type": "number",
            "title": "The author_curve_exponent schema",
            "description": "Value can be 1 to 2. This corresponds to linear or expontial rewards. In linear rewards the Rshares benefits linearly with how much Token power you have. In exponential rewards you square your Token Power when calculating rewards. It means that whales are a lot more powerful. That may encourage hodling and potentially discourage new users. Too many variables to say exactly what any one change does.",
            "default": 1.0,
            "examples": [
                1.0
            ]
        },
        "author_reward_percentage": {
            "$id": "#/properties/author_reward_percentage",
            "type": "number",
            "title": "The author_reward_percentage schema",
            "description": "value can be 0.0 to 100.0. This is how much of the rewards go to the author as opposed to the curator. There's a lot of debate of what's best. As of 5/3/19 Steem is 75% author and 25% curator. There's a lot of discussion of switching to 50:50. I've even heard talk of zero author rewards and it's all curation. Are you trying to incentivize authoring, sharing, curating, and/or something else?",
            "default": 0.0,
            "examples": [
                50.0
            ]
        },
        "beneficiaries_account": {
            "$id": "#/properties/beneficiaries_account",
            "type": "string",
            "title": "The beneficiaries_account schema",
            "description": "Account to receive a portion of post rewards, if allocating a percentage of rewards to a beneficiary. Needs chain prefix (h@ for hive, empty for steem).",
            "default": "",
            "examples": [
                "h@leoburn"
            ]
        },
        "beneficiaries_reward_percentage": {
            "$id": "#/properties/beneficiaries_reward_percentage",
            "type": "number",
            "title": "The beneficiaries_reward_percentage schema",
            "description": "Percentage of post rewards that will go to a beneficiary. Note that curator rewards are subtracted first, and the beneficiary percentage denotes the percentage of the remaining author rewards to give to the beneficiary.",
            "default": 0.0,
            "examples": [
                20.0
            ]
        },
        "cashout_window_days": {
            "$id": "#/properties/cashout_window_days",
            "type": "number",
            "title": "The cashout_window_days schema",
            "description": "a value with 1 decimal precision. This determines how many days before you can collect rewards for a post in the system. When it reaches the cashout_window_days you can claim the rewards. Steem is set to 7 days.",
            "default": 0.0,
            "examples": [
                7.0
            ]
        },
        "curation_curve_exponent": {
            "$id": "#/properties/curation_curve_exponent",
            "type": "number",
            "title": "The curation_curve_exponent schema",
            "description": "Steem sets this value to 0.5 when the author rewards are linear, the curation rewards follow then a square root function (as on steem at the current HF). It can set to 1 if you want curation rewards should be linear or it can be set between 1-2 when the rewards should be super linear.",
            "default": 0.0,
            "examples": [
                1.0
            ]
        },
        "disable_downvoting": {
            "$id": "#/properties/disable_downvoting",
            "type": "boolean",
            "title": "The disable_downvoting schema",
            "description": "disable the ability to downvote",
            "default": false,
            "examples": [
                false
            ]
        },
        "downvote_power_consumption": {
            "$id": "#/properties/downvote_power_consumption",
            "type": "integer",
            "title": "The downvote_power_consumption schema",
            "description": "this is a number that says how much of your down vote pool is eaten each time you down vote. Steem doesn't have a down vote pool, so there isn't something to compare it to, but if you want the upvote and downvotes to work the same way make sure your downvote_power_consuption and your vote_power_consumption are the same number. If you want your community to be able to down vote more frequently try a downvote number that's smaller than the vote_power number and if you want to have less downvoting than make sure the downvote number is larger than your vote_power number,",
            "default": 0,
            "examples": [
                2000
            ]
        },
        "downvote_regeneration_seconds": {
            "$id": "#/properties/downvote_regeneration_seconds",
            "type": "integer",
            "title": "The downvote_regeneration_seconds schema",
            "description": "If you want it to work like steem would (if it had a downvote pool) choose 432000 because that's exactly 5 days. If you would like the downvote pool to recharge faster choose a smaller number and if you want the downvote pool to recharge slower choose a larger number. If you don't want a downvote pool at all set the value to -1.",
            "default": 0,
            "examples": [
                432000
            ]
        },
        "downvote_window_days": {
            "$id": "#/properties/downvote_window_days",
            "type": "integer",
            "title": "The downvote_window_days schema",
            "description": "how many days should each user wait between each downvote?",
            "default": 0,
            "examples": [
                -1
            ]
        },
        "enable_account_muting": {
            "$id": "#/properties/enable_account_muting",
            "type": "boolean",
            "title": "The enable_account_muting schema",
            "description": "If enabled, allows muting accounts that a designated muting account mutes. Muting prevents posts and votes from paying rewards to the muted account. It will also prevent further posts from the muted user from being indexed (and consequently comments on such posts) ",
            "default": false,
            "examples": [
                true
            ]
        },
        "enable_comment_beneficiaries": {
            "$id": "#/properties/enable_comment_beneficiaries",
            "type": "boolean",
            "title": "The enable_comment_beneficiaries schema",
            "description": "If enabled, Scotbot will respect the comment beneficiaries in the comment options of the post and will allocate the designated percentage of author's rewards to the benficiary account (after curation, beneficiary account cuts) ",
            "default": false,
            "examples": [
                true
            ]
        },
        "exclude_apps": {
            "$id": "#/properties/exclude_apps",
            "type": "null",
            "title": "The exclude_apps schema",
            "description": "Comma separated list of apps to prevent Scotbot from indexing (and giving rewards to). The app is in the post's json metadata on creation and remains stable (edits are ignored)",
            "default": null,
            "examples": [
                null
            ]
        },
        "exclude_apps_from_token_beneficiary": {
            "$id": "#/properties/exclude_apps_from_token_beneficiary",
            "type": "string",
            "title": "The exclude_apps_from_token_beneficiary schema",
            "description": "If a post is created from the designated app, the beneficiaries_reward_percentage is ignored, and that portion will be allocated to the author (and any comment beneficiaries)",
            "default": "",
            "examples": [
                "leofinance"
            ]
        },
        "exclude_beneficiaries_accounts": {
            "$id": "#/properties/exclude_beneficiaries_accounts",
            "type": "string",
            "title": "The exclude_beneficiaries_accounts schema",
            "description": "Comma separated list of accounts that will be excluded from receiving beneficiary rewards. Instead it will go to the author. Needs chain prefix (h@ for hive, empty for steem)",
            "default": "",
            "examples": [
                "likwid,finex,sct.krwp,h@likwid,h@finex,h@sct.krwp,rewarding.app,h@rewarding.app"
            ]
        },
        "exclude_tags": {
            "$id": "#/properties/exclude_tags",
            "type": "string",
            "title": "The exclude_tags schema",
            "description": "Comma separated list of tags that should not be indexed by Scotbot for this tribe.",
            "default": "",
            "examples": [
                "actifit,steemhunt,appics,dlike,share2steem"
            ]
        },
        "fee_post_account": {
            "$id": "#/properties/fee_post_account",
            "type": "integer",
            "title": "The fee_post_account schema",
            "description": "[Not tested for hive] Account to receive fees for posting. Posts without fees paid will remain muted and will not pay out. ",
            "default": null,
            "examples": [
                null
            ]
        },
        "fee_post_amount": {
            "$id": "#/properties/fee_post_amount",
            "type": "integer",
            "title": "The fee_post_amount schema",
            "description": "[Not tested for hive] Amount for posting fee, which should be specified as an integer, and the actual fee will be the amount divided by 10^precision",
            "default": 0,
            "examples": [
                0
            ]
        },
        "fee_post_exempt_beneficiary_account": {
            "$id": "#/properties/fee_post_exempt_beneficiary_account",
            "type": "null",
            "title": "The fee_post_exempt_beneficiary_account schema",
            "description": "[Not tested for hive] If specified, allows for posts to specify a beneficiary with the given weight and account to be exempt from posting fee.",
            "default": null,
            "examples": [
                null
            ]
        },
        "fee_post_exempt_beneficiary_weight": {
            "$id": "#/properties/fee_post_exempt_beneficiary_weight",
            "type": "integer",
            "title": "The fee_post_exempt_beneficiary_weight schema",
            "description": "[Not tested for hive] If specified, allows for posts to specify a beneficiary with the given weight and account to be exempt from posting fee. The weight is an integer between 0 and 10000 corresponding to the beneficiary option on the post",
            "default": 0,
            "examples": [
                0
            ]
        },
        "hive_community": {
            "$id": "#/properties/hive_community",
            "type": "string",
            "title": "The hive_community schema",
            "description": "Allows for specifying a community to be indexed in addition to the specified tags. Hive refers to hivemind, not the hive blockchain, which is in both Steem and Hive.",
            "default": "",
            "examples": [
                "hive-167922"
            ]
        },
        "hive_enabled": {
            "$id": "#/properties/hive_enabled",
            "type": "boolean",
            "title": "The hive_enabled schema",
            "description": "Whether to allow indexing for posts on Hive.",
            "default": false,
            "examples": [
                true
            ]
        },
        "hive_engine_enabled": {
            "$id": "#/properties/hive_engine_enabled",
            "type": "boolean",
            "title": "The hive_engine_enabled schema",
            "description": "Whether to base Hive voting stake on balances from hive engine.",
            "default": false,
            "examples": [
                true
            ]
        },
        "issue_token": {
            "$id": "#/properties/issue_token",
            "type": "boolean",
            "title": "The issue_token schema",
            "description": "Options are true or false. If you want Scotbot to be able to issue tokens then you'll set this to True. If you try to do proof of brain distribution and you run out of tokens it'll cease to operate if it can't issue more or there are no more to issue. If the answer is false you'll have to transfer tokens from an account if it runs out or issue them manually.",
            "default": false,
            "examples": [
                true
            ]
        },
        "json_metadata_app_value": {
            "$id": "#/properties/json_metadata_app_value",
            "type": "null",
            "title": "The json_metadata_app_value schema",
            "description": "If specified, only index posts that have this app. This is in conjunction with the specified tags.",
            "default": null,
            "examples": [
                null
            ]
        },
        "json_metadata_key": {
            "$id": "#/properties/json_metadata_key",
            "type": "string",
            "title": "The json_metadata_key schema",
            "description": "For now the only option here is \"tags\", It means that the bot is searching tags to find out which posts to apply proof of brain token distribution onto. In the future I hope to add \"url\" and it'll explore only specific URLs to to see if a post should be tokens rewarded to it.",
            "default": "",
            "examples": [
                "tags"
            ]
        },
        "json_metadata_value": {
            "$id": "#/properties/json_metadata_value",
            "type": "string",
            "title": "The json_metadata_value schema",
            "description": "\"scottest\", it's the name of the tag that the bot looks for when distributing tokens.",
            "default": "",
            "examples": [
                "leofinance,leo"
            ]
        },
        "miner_tokens": {
            "$id": "#/properties/miner_tokens",
            "type": "string",
            "title": "The miner_tokens schema",
            "description": "If proof of staked mining is enabled (posm_pool_percentage), this specifies which tokens are used for mining. Deprecated for hive-- use the mining contract instead.",
            "default": "",
            "examples": [
                "{\"LEOM\": 1, \"LEOMM\": 4}"
            ]
        },
        "mining_pool_claim_number": {
            "$id": "#/properties/mining_pool_claim_number",
            "type": "integer",
            "title": "The mining_pool_claim_number schema",
            "description": "For proof of staked mining, the number of winners per staked mining lottery.",
            "default": 0,
            "examples": [
                30
            ]
        },
        "mining_pool_claims_per_year": {
            "$id": "#/properties/mining_pool_claims_per_year",
            "type": "integer",
            "title": "The mining_pool_claims_per_year schema",
            "description": "For proof of staked mining, the number of lotteries run per year. 8760 corresponds to once per hour.",
            "default": 0,
            "examples": [
                8760
            ]
        },
        "muting_account": {
            "$id": "#/properties/muting_account",
            "type": "string",
            "title": "The muting_account schema",
            "description": "If muting is enabled, the designated account to track for muting accounts. If this account mutes another account, that account is then muted for the tribe.",
            "default": "",
            "examples": [
                "noleo4u"
            ]
        },
        "n_daily_posts_muted_accounts": {
            "$id": "#/properties/n_daily_posts_muted_accounts",
            "type": "integer",
            "title": "The n_daily_posts_muted_accounts schema",
            "description": "If specified, specifies a maximum number of posts that will be muted per day. 0 means no limit.",
            "default": 0,
            "examples": [
                0
            ]
        },
        "other_pool_accounts": {
            "$id": "#/properties/other_pool_accounts",
            "type": "string",
            "title": "The other_pool_accounts schema",
            "description": "Accounts and percentages (between 1 and 100) that will receive inflation from the other_pool_percentage of inflation. Values in map should add up to other_pool_percentage",
            "default": "",
            "examples": [
                "{\"wleo.pool\": 15}"
            ]
        },
        "other_pool_percentage": {
            "$id": "#/properties/other_pool_percentage",
            "type": "number",
            "title": "The other_pool_percentage schema",
            "description": "Percentage of inflation to direct to other pools specified in other_pool_accounts",
            "default": 0.0,
            "examples": [
                15.0
            ]
        },
        "other_pool_send_token_per_year": {
            "$id": "#/properties/other_pool_send_token_per_year",
            "type": "integer",
            "title": "The other_pool_send_token_per_year schema",
            "description": "Number of times per year to send tokens from the other pool to the other pool accounts.",
            "default": 0,
            "examples": [
                365
            ]
        },
        "pob_comment_pool_percentage": {
            "$id": "#/properties/pob_comment_pool_percentage",
            "type": "number",
            "title": "The pob_comment_pool_percentage schema",
            "description": "Percentage of inflation that will be directed to the reward pool for comments. If specified, posts and comments will have separate pools. Otherwise, comments and posts are counted together.",
            "default": -1.0,
            "examples": [
                -1.0
            ]
        },
        "pob_pool_percentage": {
            "$id": "#/properties/pob_pool_percentage",
            "type": "number",
            "title": "The pob_pool_percentage schema",
            "description": "Percentage of inflation that will be directed to the reward pool for posts.",
            "default": 0.0,
            "examples": [
                70.0
            ]
        },
        "posm_pool_percentage": {
            "$id": "#/properties/posm_pool_percentage",
            "type": "number",
            "title": "The posm_pool_percentage schema",
            "description": "Percentage of inflation that will be directed to the staked mining pool. Staked mining works by lottery, where the chances of winning are proportional to your mining power (determined by the mining tokens and multiplier). Deprecated for hive-- use the mining contract instead.",
            "default": 0.0,
            "examples": [
                15.0
            ]
        },
        "post_reward_curve": {
            "$id": "#/properties/post_reward_curve",
            "type": "string",
            "title": "The post_reward_curve schema",
            "description": "Default for n^a author, n^b curation parameters. 'convergent_linear' for the newer scheme used in Steem/Hive.",
            "default": "",
            "examples": [
                "default"
            ]
        },
        "post_reward_curve_parameter": {
            "$id": "#/properties/post_reward_curve_parameter",
            "type": "null",
            "title": "The post_reward_curve_parameter schema",
            "description": "n^a reward curve. Specifies weight of a post for payout. e.g. if 1, it is linear,  2 is quadratic (means rewards will be proportional to n^2 where n is the amount of rshares on the post)",
            "default": 1,
            "examples": [
                1
            ]
        },
        "promoted_post_account": {
            "$id": "#/properties/promoted_post_account",
            "type": "string",
            "title": "The promoted_post_account schema",
            "description": "Post to collect fee for post promotion. When a memo is sent to this account with the permlink to the post, that post will be promoted, and the promoted feed for a given tag will be ordered by promotion amount, descending.",
            "default": "",
            "examples": [
                "null"
            ]
        },
        "reduction_every_n_block": {
            "$id": "#/properties/reduction_every_n_block",
            "type": "integer",
            "title": "The reduction_every_n_block schema",
            "description": "10512000, 1051200 is 1 year's worth. So, this is saying \"After one year reduce the amount of inflation by the \"reduction_percentage\". If you want it to reduce faster than you'll put in a smaller number. If you want inflation to reduce over time more slowly put in a larger number.",
            "default": 0,
            "examples": [
                10512000
            ]
        },
        "reduction_percentage": {
            "$id": "#/properties/reduction_percentage",
            "type": "number",
            "title": "The reduction_percentage schema",
            "description": "this is how much the inflation percent will reduce every time reduction_every_n_block cycles. Steem uses 0.5. If you'd like to keep inflation up then you'll want this smaller. If you want to drastically cut how much inflation you use over time you'll want this number to be high.",
            "default": 0.0,
            "examples": [
                7.0
            ]
        },
        "rewards_token": {
            "$id": "#/properties/rewards_token",
            "type": "number",
            "title": "The rewards_token schema",
            "description": "This is how many tokens are released into the rewards pool every time that rewards_token_every_n_block is hit. So, if this is 10 and that's 3 then every 3 blocks 10 tokens will be added to the pool.",
            "default": 0.0,
            "examples": [
                8.0
            ]
        },
        "rewards_token_every_n_block": {
            "$id": "#/properties/rewards_token_every_n_block",
            "type": "integer",
            "title": "The rewards_token_every_n_block schema",
            "description": "this is what determines the size of the rewards pool. This is an interger value. This is really determining how quickly you're distributing new tokens.",
            "default": 0,
            "examples": [
                100
            ]
        },
        "staked_reward_percentage": {
            "$id": "#/properties/staked_reward_percentage",
            "type": "number",
            "title": "The staked_reward_percentage schema",
            "description": "When paying out rewards via auto claim (about once a day), specifies what percentage of the reward to distribute as staked vs liquid.",
            "default": 0.0,
            "examples": [
                0.0
            ]
        },
        "staking_pool_claim_number": {
            "$id": "#/properties/staking_pool_claim_number",
            "type": "integer",
            "title": "The staking_pool_claim_number schema",
            "description": "If proof of staked mining is enabled (staking_pool_percentage), this specifies the number of winners for each staking lottery.",
            "default": 0,
            "examples": [
                0
            ]
        },
        "staking_pool_claims_per_year": {
            "$id": "#/properties/staking_pool_claims_per_year",
            "type": "integer",
            "title": "The staking_pool_claims_per_year schema",
            "description": "If proof of staked mining is enabled (staking_pool_percentage), this specifies the number of lotteries per year.",
            "default": 0,
            "examples": [
                0
            ]
        },
        "staking_pool_percentage": {
            "$id": "#/properties/staking_pool_percentage",
            "type": "number",
            "title": "The staking_pool_percentage schema",
            "description": "Percentage of inflation to allocate to proof of stake mining. This works by a lottery where your chances are winning are proportional to your stake.",
            "default": 0.0,
            "examples": [
                0.0
            ]
        },
        "steem_enabled": {
            "$id": "#/properties/steem_enabled",
            "type": "boolean",
            "title": "The steem_enabled schema",
            "description": "Is Steem Enabled?",
            "default": false,
            "examples": [
                false
            ]
        },
        "steem_engine_enabled": {
            "$id": "#/properties/steem_engine_enabled",
            "type": "boolean",
            "title": "The steem_engine_enabled schema",
            "description": "Is Steem Engine enabled?",
            "default": false,
            "examples": [
                false
            ]
        },
        "tag_adding_window_hours": {
            "$id": "#/properties/tag_adding_window_hours",
            "type": "number",
            "title": "The tag_adding_window_hours schema",
            "description": "How many hours after a post is added, can tags be added to the post?",
            "default": 0.0,
            "examples": [
                1.0
            ]
        },
        "token": {
            "$id": "#/properties/token",
            "type": "string",
            "title": "The token schema",
            "description": "what's the name of the token that's being distributed?",
            "default": "",
            "examples": [
                "SCOTT"
            ]
        },
        "token_account": {
            "$id": "#/properties/token_account",
            "type": "string",
            "title": "The token_account schema",
            "description": "which account is the one distributing the tokens?",
            "default": "",
            "examples": [
                "scottest"
            ]
        },
        "use_staking_circulating_quotent": {
            "$id": "#/properties/use_staking_circulating_quotent",
            "type": "boolean",
            "title": "The use_staking_circulating_quotent schema",
            "description": "Deprecated.",
            "default": false,
            "examples": [
                false
            ]
        },
        "vote_power_consumption": {
            "$id": "#/properties/vote_power_consumption",
            "type": "integer",
            "title": "The vote_power_consumption schema",
            "description": "2,this is how much of your voting power is consumed every time you do a full vote. Steem has it so that every 5 days you can use 100% of your power. So, a value of 2 gives you 10 votes a day which comes to a value of 20%/day and in 5 days you have used full power. If you think users should vote more frequently (spread votes out) then you'll want a smaller number. If you think they should be casting fewer mega votes then go for a number bigger than 2.",
            "default": 0,
            "examples": [
                2
            ]
        },
        "vote_regeneration_seconds": {
            "$id": "#/properties/vote_regeneration_seconds",
            "type": "integer",
            "title": "The vote_regeneration_seconds schema",
            "description": "the value for 5 days. This number is how many seconds are required to recharge your VP from 0 to full. If you want a faster recharge use a smaller number. If you want a slower recharge choose a bigger number.",
            "default": 0,
            "examples": [
                432000
            ]
        },
        "vote_window_days": {
            "$id": "#/properties/vote_window_days",
            "type": "integer",
            "title": "The vote_window_days schema",
            "description": "How long a post is active, able to receive votes for, before it is ready for payout.",
            "default": 7,
            "examples": [
                -1
            ]
        }
    },
    "additionalProperties": true
}
```
