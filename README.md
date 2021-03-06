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

### Connect to O365 PowerShell using MFA

To connect with the Microsoft Azure Active Directory Module for Windows PowerShell with MFA, run the below cmdlet. 

```powershell
./ConnectO365Services.ps1 -Services MSOnline -MFA
```

**_Note:_** Above cmdlet will install MSOnline module if it is not installed already. 

### Connect to Azure Active Directory PowerShell

To connect with the Microsoft Azure Active Directory PowerShell for Graph module, run the below cmdlet. 

```powershell
./ConnectO365Services.ps1 -Services AzureAD
```

**_Note:_** Above cmdlet will install AzureAD module if it is not installed already. 

### Connect to Azure Active Directory PowerShell using MFA

To connect with the Microsoft Azure Active Directory PowerShell with MFA, run the below cmdlet. 

```powershell
./ConnectO365Services.ps1 -Services AzureAD -MFA
```

**_Note:_** Above cmdlet will install AzureAD module if it is not installed already. 

### Connect to SharePoint Online PowerShell 

To connect SharePoint Online using PowerShell, SharePoint Online Management Module is required. When you run a below cmdlet, it will ask for installing that module if it is not already installed.  

```powershell
./ConnectO365Services.ps1 -Services SharePoint -SharePointHostName <Organization Name>
```
SharePointHostName used to connect SharePoint Online Administration Center. For admin@Contoso.onmicrosoft.com, organization name is Contoso. 

### Connect to SharePoint Online PowerShell with MFA 

To connect SharePoint Online PowerShell with MFA enabled account, run the below cmdlet. 

```powershell
./ConnectO365Services.ps1 -Services SharePoint -SharePointHostName <Organization Name> -MFA
```

SharePointHostName used to connect SharePoint Online Administration Center. For admin@Contoso.onmicrosoft.com, organization name is Contoso. 

### Connect to SharePoint PnP PowerShell

SharePoint Patterns and Practices (PnP) allows you to perform complex provisioning and artifact management actions in the SharePoint.

To connect SharePoint PnP using PowerShell, run a below cmdlet. It will ask for installing that module if it is not already installed.  

```powershell
./ConnectO365Services.ps1 -Services SharePointPnP -SharePointHostName <Organization Name>
```

SharePointHostName used to connect SharePoint Online Administration Center. For admin@Contoso.onmicrosoft.com, organization name is Contoso. 

### Connect to SharePoint PnP PowerShell with MFA

To connect SharePoint PnP PowerShell with MFA enabled account, run a below cmdlet.

```powershell
./ConnectO365Services.ps1 -Services SharePointPnP -SharePointHostName <Organization Name> -MFA
```

SharePointHostName used to connect SharePoint Online Administration Center. For admin@Contoso.onmicrosoft.com, organization name is Contoso. 

### Connect to Skype for Business Online PowerShell

To connect Skype for Business Online PowerShell, you can use the below cmdlet.

```powershell
./ConnectO365Services.ps1 -Services Skype
```

Above cmdlet will install Teams PowerShell which has Skype for Business Online Connector integration. So, you can use New-CSOnlineSession cmdlet with the Teams PowerShell itself.

**_Note:_** Since Skype for Business Online Connector module is under deprecation, we have used Teams PowerShell to connect Skype for Business Online PowerShell. If you want to install Skype for Business Online Connector module, you can use below link to download the Module.
[Skype for Business Online Connector Module](https://download.microsoft.com/download/2/0/5/2050B39B-4DA5-48E0-B768-583533B42C3B/SkypeOnlinePowerShell.Exe)

### Connect to Skype for Business Online PowerShell with MFA

To connect Skype for Business Online PowerShell with MFA, you can use the below cmdlet.

```powershell
./ConnectO365Services.ps1 -Services Skype -MFA
```

Above cmdlet will install the Teams PowerShell which has the Skype for Business Online Connector integration. So, you can use `New-CSOnlineSession` cmdlet with the Teams PowerShell itself.

### Connect to Teams PowerShell

To connect Teams PowerShell, it requires Microsoft Teams Module. When you run the below cmdlet, it will install Microsoft’s Team PowerShell module and then connects to Teams. 

```powershell
./ConnectO365Services.ps1 -Services Teams
```

### Connect to Teams PowerShell with MFA

To connect Teams PowerShell with MFA, run the below cmdlet. 

```powershell
./ConnectO365Services.ps1 -Services Teams -MFA
```

### Connect to Office 365 Security & Compliance Center PowerShell

To manage Office 365 Security and Compliance Center from the PowerShell, run the below cmdlet 

```powershell
./ConnectO365Services.ps1 -Services SecAndCompCenter
```

### Connect to Office 365 Security & Compliance Center PowerShell with MFA

To connect Office 365 Security & Compliance Center with MFA, you need Microsoft’s “Exchange Online Remote PowerShell Module”. Our script will install Exchange Online MFA module (After getting confirmation from you) when you execute a script with `-MFA` param and then connects Security & Compliance Center. 

```powershell
./ConnectO365Services.ps1 -Services SecAndCompCenter -MFA
```

If you want to install module manually, you can refer Install Exchange Online Remote PowerShell Module blog. 

### Connect Multiple Office 365 Services Using PowerShell

If you want to connect multiple services, mention the required services by using -Services param.

```powershell
./ConnectO365Services.ps1 -Services AzureAD,ExchangeOnline
```

If you want to connect multiple Office 365 services with MFA, mention the required services with `-MFA` switch.

```powershell
./ConnectO365Services.ps1 -Services AzureAD,ExchangeOnline,Skype -MFA
```

### Disconnect Office 365 Services

Make sure to disconnect the remote PowerShell session when you’re finished. Else you would end up using all remote PowerShell sessions available to you and you will get the following error. 

```powershell
`New-PSSession :` "outlook.office365. com Processing data from remote server outlook.office365. com failed with the following error message: Fail to create a runspace because you have exceeded the maximum number of connections allowed: 10 for the policy party: MaxConcurrency. Please close existing runspace and try again."
```

To disconnect all the Office 365 PowerShell session in the current window, run the below command. 

```powershell
./ConnectO365Services.ps1 –Disconnect
``` 