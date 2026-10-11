# Power BI RLS Starter Kit: Team Hierarchy

Starter kit for the DataSanj YouTube tutorial. You learn how to set up **dynamic row-level security (RLS)** over an organisation hierarchy. Each manager sees only their own team's performance, not other teams or the whole organisation.

▶️ **Video:** <add YouTube link>

## What's inside
One report page, **Team Performance**:
- Manager cards across the top.
- A table of every seller below.
- **No Path column, no Team Key, no RLS role yet.** Everyone sees everything. You add the security while following the video.

## What you'll learn
- Build a **PATH** column with DAX to flatten a parent-child hierarchy.
- Write the RLS role filter with `PATHCONTAINS` and `USERPRINCIPALNAME()`.
- Test the role with **View as**.
- Handle people **moving teams**, so the report always shows the current team.
- Publish and assign users to the role in the Power BI service.

## Requirements
- Power BI Desktop (recent version, with **Developer mode / PBIP** enabled)
- Free **HTML Content** visual (Desktop will prompt you to install it)

## Get started
1. Download or clone this repo.
2. Open `RLS Team Hierarchy - Starter.pbip` in Power BI Desktop.
3. Follow the video, using `TUTORIAL-SNIPPETS.md` for the DAX to copy.

## How teams work
A team is a manager plus everyone who reports to them. A manager sees their team. A team member sees their manager's team.

## Test emails
In **Modeling > View as**, tick **Other user** *and* your role, then enter:

| Email | Should see |
|---|---|
| bob@co.com | 1 card (Bob Chen's team) |
| farid@co.com | Emma's group: Emma, Farid, Grace |
| hannah@co.com | Bob Chen's whole team |
| kate@co.com | 1 card (Kate Nguyen's team) |
| nobody@co.com | nothing |

> Tick the role as well as Other user. If you tick only Other user, no filter is applied.

## Notes
- Sample data only. No real people or company data.
- In the service, RLS applies to **Viewers** only. Admin, Member and Contributor roles bypass it.

---
By [DataSanj](https://datasanj.com). Subscribe for more Power BI and Fabric.
