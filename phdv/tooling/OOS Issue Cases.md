# OOS Issue Cases

## Case #1: Add/Remove one or more product-variant(s) of `Classic Crust` 

1. Remove `hawaiian` pizza that associates to `Classic Crust` 
2. Trigger the import with `--reset` flag
3. Re-add `hawaiian` pizza that associates to `Classic Crust`
4. Trigger the import without `--reset` flag (Note: make sure `producType` value = `side,dip,dessert,drink,pizza` - the Feature Flag for `TO-1FusionOutofStock`  )

## Case #2: The initial OOS price entries are not enough after launching new campaign

1. Search `Classic Crust` and set OOS in Fusion UI
2. Add some price entries with `price=0` in Menu Sheet
3. Execute the import (Note: Make `productType` flag empty in Unleashed )
4. Verify the OOS `Classic Crust in Fusion UI

## Case 1+2: The export

1. Remove `veg-supreme`  in Price Sheet
2. Trigger Import process with `--reset` flag
3. Search `Classic Crust` and set OOS in Fusion UI
4. Export OOS from Fusion UI
5. Re-add `veg-supreme` in Price Sheet for New Campaign
6. Copy & Paste the Exported OOS to Price Sheet
7. Re-import with `--reset` flag (New Campaign)
8. Verify ---> OOS Products not shown in Fusion
9. Add OOS for `veg-supreme` in Price sheet
10. Re-import without `--reset` flag 
11. Verify Fusion Again -> OOS shown.



