# xDiff change history: 

## 2020-10-06
* Only latest 100 reports are shown. Improved performance. Older reports are still available on demand.
* Non-admin users can only see reports they have created or for containers and languages their VegaSuite credentials have assigned.
* The Settings tab is gone, since one option there had and might never been implemented, and the other one does not really make sense.

## 2020-11-15

### On main page:
* Corrupted OMT packages failed silently and gave a report with no differences -> no report is created now
* Delete button in report list deleted report even if confirmation was cancelled -> cancel button stops the action now
* Table styles, search box, and sorting were gone -> restored now
* Drop area did not show file dragged -> restored now

### On report page:
* Arabic/Hebrew text had wrong left-to-right direction -> correct RTL direction now
* Font used (Rockwell) in cells did not display all languages clearly -> changed to Segoe UI
* Clean-up button had an unclear name -> renamed as to reflect what it actually does
