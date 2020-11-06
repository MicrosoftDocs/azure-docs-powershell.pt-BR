---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 7bb92a55f366d90eb5993cfe1520d1b516214372
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427219"
---
# Import-AzureRmRecoveryServicesAsrVaultSettingsFile

## Sinopse
Importa o arquivo de configurações do cofre ASR especificado para definir o contexto do cofre (contexto da sessão do PowerShell) para operações ASR subsequentes na sessão do PowerShell. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** importa o arquivo de configurações do cofre do Azure site Recovery. O arquivo de configurações de cofre é usado para definir o contexto do cofre para operações subsequentes de recuperação de site do Azure na sessão atual.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

Importa o arquivo de configurações do cofre de serviços de recuperação especificado e retorna as configurações do cofre importado.

## OS

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

### -Caminho
Especifica o caminho da pasta do arquivo de configurações do cofre ASR.
Esse arquivo pode ser baixado do portal de compartimento de serviços de recuperação e armazenado localmente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesAsrVaultSettingsFile](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
