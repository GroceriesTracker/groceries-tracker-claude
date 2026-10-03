---
name: household-brief
description: Use when someone asks about grocery spending, receipts, categories, items, stores, what changed, a budget, or how to spend less, and Groceries Tracker is connected. Call get_household_brief once. It is read only.
version: 1.1.0
allowed-tools: mcp__plugin_groceries-tracker_groceries-tracker__get_household_brief
---

# Groceries Tracker

Groceries Tracker is a grocery receipt app for a household. People in the same house scan receipts. The app keeps categories, items, stores, and a monthly total.

You already know this product. Use the connected Groceries Tracker tool. Do not ask the person to paste receipts, export a file, or grant any other permission.

## The only tool

Call `get_household_brief`. The full name on this plugin is `mcp__plugin_groceries-tracker_groceries-tracker__get_household_brief`.

It is read only. It cannot add, edit, or delete receipts.

- `month`: `YYYY-MM`. Leave it empty for the current month. Pass the previous month when they ask about last month.
- `saveTarget`: amount to cut next month. Leave it empty to use 100. Pass a number only when they name one.

Call it once for the question. Reuse that result. Call it again only when they ask about a different month or a different cut.

## What the result means

The result is a summary for the whole household, not one shopper. The month they ask about has the spending: category totals, top items, store totals, usual spending, what changed, products that cost more, a save plan, and a suggested budget. Usual spending uses the three months before that month.

Grocery names are a separate list from the past 7 days, up to 40 names. That week is not the limit of the history. Do not tell the person their data only covers the past week. The name list is counted from today, even when the question is about another month.

Do not invent aisle numbers. Do not add store names that are not in the result. Skip a blank name. The summary does not include receipt images, and it does not include database ids.

## If the tool is missing

Say the Groceries Tracker connection is not on. They can search for Groceries Tracker in Claude's connectors and sign in with their Groceries Tracker account.

A paid household can connect. Someone on the free plan needs to upgrade. A member who is not the owner needs the household owner to be on a paid plan.

Do not ask them to paste a server address. Do not ask to read their other chats, files, or accounts.

## How to answer

Lead with the number they asked for. Then name the few categories or items that explain it. Bring up the save plan when they ask how to spend less, or when spending is above usual.

If that month has no receipts, say so in one sentence.
