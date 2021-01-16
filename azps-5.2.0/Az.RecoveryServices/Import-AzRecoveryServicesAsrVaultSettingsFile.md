---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262138"
---
# Import-AzRecoveryServicesAsrVaultSettingsFile

## Sinopse
Importa o arquivo de configurações do cofre ASR especificado para definir o contexto do cofre (contexto da sessão do PowerShell) para operações ASR subsequentes na sessão do PowerShell. 

## SYNTAX

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importa o arquivo de configurações do cofre do Azure site Recovery. O arquivo de configurações de cofre é usado para definir o contexto do cofre para operações subsequentes de recuperação de site do Azure na sessão atual.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

Importa o arquivo de configurações do cofre de serviços de recuperação especificado e retorna as configurações do cofre importado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings

## INFORMA

## LINKS RELACIONADOS

[Get-AzRecoveryServicesAsrVaultSettingsFile](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
