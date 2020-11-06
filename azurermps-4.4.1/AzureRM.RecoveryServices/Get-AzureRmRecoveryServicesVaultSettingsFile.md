---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433027"
---
# Get-AzureRmRecoveryServicesVaultSettingsFile

## Sinopse
Obtém o arquivo de configurações do cofre do Azure site Recovery.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ForSite
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefault
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultType
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** Obtém o arquivo de configurações para um cofre do Azure site Recovery.

## EXEMPLOS

### Exemplo 1: registrar um servidor Windows ou um computador do DPM para backup do Azure
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

O primeiro comando obtém o cofre chamado TestVault e, em seguida, armazena-o na variável $Vault 01.

O segundo comando define a variável $CredsPath como C:\Downloads.

O último comando obtém o arquivo de credenciais do cofre para $Vault 01 usando as credenciais do $CredsPath para o backup do Azure.

## OS

### -Backup
Indica que o arquivo de credenciais do cofre se aplica ao Azure backup.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho para o arquivo de configurações do cofre do Azure site Recovery.
Você pode baixar esse arquivo do portal de cofre do Azure site Recovery e armazená-lo localmente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Especifica o nome amigável do site.
Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
Especifica o identificador do site.
Use esse parâmetro se você estiver baixando as credenciais do cofre para um site do Hyper-V.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
Indica que o arquivo de credenciais do cofre se aplica ao Azure site Recovery.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cofre
Especifica o objeto do cofre do Azure site Recovery.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### ARSVault
O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. VaultSettingsFilePath

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesVault](./Get-AzureRmRecoveryServicesVault.md)

[New-AzureRmRecoveryServicesVault](./New-AzureRmRecoveryServicesVault.md)

[Remove-AzureRmRecoveryServicesVault](./Remove-AzureRmRecoveryServicesVault.md)


