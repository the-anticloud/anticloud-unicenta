# UNICENTA

> Anticloud offline package — upstream: herbiehp/unicenta @ `master`.

## What This Project Does

uniCenta oPos repository

## Upstream README

Reference: uniCenta.com
Author: Jack Gerrard

v3.81 Is a direct replacement for v3.80 - Apache Derby database driver rolled-back to 10.10

v3.80 Is a deprecated release. No source code available.
Apache Derby 10.11 caused known issue (Apache Derby forums) with Auto-Increment fields

********************************************************************************

v3.90 SOURCE CODE IS NOT AVAILABLE! 

Use v3.81 if you do not need digital receipt functionality.

posApps Digital Receipt plugin app' is totally independent of uniCenta oPOS and exists as a separate jar file. No uniCenta oPOS source code has been changed or  affected.

THE ONLY DIFFERENCE BETWEEN V3.90 AND v3.81 IS THAT v3.90 IS DELIVERED WITH OUR posApps Digital Receipt plugin library jar and change to Ticket.Close script - which is available from http://www.posapps.io 


Please see - http://www.posapps.io for more information

********************************************************************************

3.81
1.  Bug: Ticket and Pickup auto-numbering incrementing +100 on each restart 
    Fix: Revert Apache Derby 10.11 derby.jar to version 10.10.2

3.80
1.  Bug: Customer Find - Telephone SQL field criteria incorrect - returning PHONE2
    Fix: Correct SQL statement to return PHONE
2.  Bug: Categories Display Name in panel checkbox ineffective
    Fix: Change getRootCategories SQL to only include CATSHOWNAME=1
3.  Bug: Show Category in Panel check/un-check ineffective
    Fix: Amend RootCategory method
4.  Bug: script.linediscount rounding error
    Fix: Remove Math(Rounding()) and replace with revised formula on LineTotal value
5.  Bug: Free Sale line product add fails after upgrade
    Fix: Change Installer SQL statement + supporting in-line code
6.  Bug: Close Cash - Drawer Openings in MySQL not resetting
    Fix: Change code to allow for TIMESTAMP differentails between DB's
7.  Bug: JPanelTicket SouthComponent refresh error
    Fix: Now conditional - John L
8.  Bug: rpt:productsalesprofit - incompatible/incorrect SQL syntax causes report fail
    Fix: redesign and replace complete report productsalesreport
9.  Bug: Authorize.net Payment Gateway - attempt to get past intermittent submission fails.
    Fix: Per latest Authorize.net //github repository + addition of messages (success/fails/refusals & etc).
	 IMPORTANT: Only tested in developer Authorizenet Sandbox mode
10. Bug: Customer Current Debt value not updating after ticket Payment form by Debt
    Fix: PaymentInfo get and sets amended to fetch, display and write latest CurrentDebt value
11. Bug: Customer Current Debt Date not updating after ticket Payment form by Debt
    Fix: PaymentInfo get and sets amended to fetch, display and write latest CurrentDate value
12. Bug: EAN-8/UPC-8 Barcode input not checked
    Fix: Barcode checks for EAN-8/UPC-8 construct

13. Change: Payment form: Given and Change background/text contrast poor. Now uses skin settings
14. Change: Sales screen Product button default background image reduced

## License

Upstream terms preserved in `THIRD_PARTY_LICENSES/`. Overlay licensed under Anticommons 0.1.0.

## Verification

Recompute the SHA3-256 of `BENCH.json` and compare to this package’s register. Any drift = invalid package.
