## How to import

### Sheets
- C5: https://docs.google.com/spreadsheets/d/1KRdKFhQk2wtO1HM_L_M620uLuBZUEYQAqqFQ7dkML88/edit#gid=315762446
- C6: https://docs.google.com/spreadsheets/d/1Z_TImbOIvWFGY0_WOPGLeBKXTQi3rYQhlbkap-PHdjo/edit#gid=0

### Steps

Login as google account
```
aws-google-auth --username phuhao.nguyen@pizzahut.io -d 43200 -I C03x308ch -S 176561460548 -p phdvuk -R eu-west-1export NODE_ENV=development
export AWS_PROFILE=phdvuk
export AWS_REGION=eu-west-1
```

Trigger the import process
```
NODE_ENV=development MENU_API_KEY=local scripts/run.sh to-1 "TO-1 21C6" "1KRdKFhQk2wtO1HM_L_M620uLuBZUEYQAqqFQ7dkML88"
NODE_ENV=development MENU_API_KEY=local scripts/run.sh to-1 "TO-1 21C7" "1Z_TImbOIvWFGY0_WOPGLeBKXTQi3rYQhlbkap-PHdjo"
```

In case of running in PRODUCTION
```
NODE_ENV=production  scripts/run.sh to-1 "TO-1 21C5" "13QgucL1C3r5qh5XGr-KXfq9oLZbMBTrU8y9aR0YwTOM"
```

