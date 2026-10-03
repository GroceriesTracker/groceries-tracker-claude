# Groceries Tracker

Read a household's grocery spending from Groceries Tracker. Claude can see a month: category totals, top items, stores, what changed from the month before, and a save plan. It also includes grocery names from the past week.

The connection is read only. It cannot add or change receipts.

## What this plugin teaches Claude

The skill `household-brief` tells Claude what Groceries Tracker is and to call `get_household_brief` once. The agent `groceries` is the same specialist for Claude Code and Cowork. Chat on claude.ai uses the skill.

Claude should not ask the person to paste receipts, paste a server address, or grant any other permission.

## Who can connect

A paid household. Each person signs in with their own Groceries Tracker account and picks the household at connect. Someone on the free plan is asked to upgrade. A member who is not the owner is told that the household owner needs a paid plan.

## What Claude receives

A summary for the month you ask about. It includes the household name, currency, category totals, top items, store totals, usual spending, what changed, products that cost more, and a save plan. It also includes grocery names from the past week. It does not include receipt images.

## Privacy

Groceries Tracker does not sell this summary. The summary covers the whole household. See the privacy policy at https://groceriestracker.com/privacy.

Support: support@groceriestracker.com
