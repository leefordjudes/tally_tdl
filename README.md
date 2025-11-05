# Import Auditplus Vouchers To Tally Using TDL

* Configure
* Login
* Download Masters (Group, Voucher Type)
* Mapping Masters (Group, Voucher Type) 
* Transaction Download
* Delete imported vouchers based on date, voucher type

# Steps

* 1. Create Company
    ![create company](docs/create-company.png)
* 2. Load TDL auditplus.txt
    * F1: Help => O: TDLs & AddOns => F4: Manage Local TDLs 
    * Select Tdl from local path, and End of List
    * Ctrl+Q : Quit
* 3. Now Menu "Auditplus Integration" added in Menu "Gateway of Tally"
* 4. Configure
    * Host          : http://192.168.1.31:3000 or https://ap1.auditplusdb.com
    * Organization  : someorg
    * BookBegin:    : 1-Apr-24
    ![configure](docs/auditplus-configuration.png)
* 5. Login
    * Username      : someuser with "tally export" permission
    * Password      : somepassword
    ![login](docs/login.png)
* 6. GoTo "Masters" => Select "Download"
* 7. GoTo "Group" => Map tally group against auditplus account type 
    ![group mapping](docs/group-mapping.png)
* 8. GoTo "Voucher Type" => Map tally voucher type against auditplus voucher type 
    ![voucher type mapping](docs/vouchertype-mapping.png)
* 9. Make sure
    * "Method of Voucher Numbering"             : Automatic (Manual Override)
    * Prevent creating duplicate Voucher Nos.   : Yes
    ![alter master](docs/alter-master.png)
    ![alter master voucher type](docs/alter-master-vouchertype.png)
    ![select default voucher type](docs/select-default-vouchertype.png)
    ![alter default voucher type](docs/alter-default-voucher-type.png)
* 10. If you need any new voucher type, then create it
    ![select custom voucher type](docs/select-custom-vouchertype.png)
    ![alter custom voucher type](docs/alter-custom-voucher-type.png)
* 11. GoTo "Transactions" to download vouchers from auditplus
    ![transaction configuration](docs/transaction-configuration.png)
* 12. GoTo "Delete Imported Vouchers" 
    ![delete imported vouchers](docs/delete-configuration.png)