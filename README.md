### Connect to all Office 365 Services (Without MFA)

Using below cmdlet, you can connect to Office 365 services like Exchange Online, Azure Active Directory, MSOnline, SharePoint Online, SharePoint PnP, Skype for Business Online, Teams, and Security & Compliance center.

``` powershell
./ConnectO365Services.ps1
```

You can also pass the credential as a parameter:

```powershell
./ConnectO365Services.ps1 -UserName Admin@Contoso.com -Password "XXX"
```

**_Note:_** *You can also give script’s absolute path if it’s not in the current directory.*

### Connect to all Office 365 Services (With MFA)

Using below cmdlet, you can connect to Office 365 services like Exchange Online, Azure Active Directory, SharePoint Online, Skype for Business Online, Teams, and Security & Compliance center with MFA:

```powershell
./ConnectO365Services.ps1 -MFA
```

### Connect to Exchange Online PowerShell

To connect Exchange Online, run the below cmdlet:

```powershell
./ConnectO365Services.ps1 -Services ExchangeOnline
```

If you want to know detailed explanation about cmdlet, refer to [connect to Exchange Online PowerShell](https://o365reports.com/2019/08/22/connect-exchange-online-powershell/) blog.

### Connect to Exchange Online PowerShell with MFA

To connect Exchange Online PowerShell with MFA, you need Microsoft’s “Exchange Online Remote PowerShell Module”. Our script will install Exchange Online MFA module (after your confirmation), when you execute a script with `-MFA` switch and then connect to Exchange Online using MFA:

```powershell
./ConnectO365Services.ps1 -Services ExchangeOnline -MFA
```

If you want to know detailed explanation about cmdlet, refer to [connect to Exchange Online PowerShell](https://o365reports.com/2019/08/22/connect-exchange-online-powershell/) blog.

### Connect to Office 365 PowerShell

To connect with the Microsoft Azure Active Directory Module for Windows PowerShell, run the below cmdlet:

```powershell
./ConnectO365Services.ps1 -Services MSOnline
```

**_Note:_** *Above cmdlet will install MSOnline module if it is not installed already.*
