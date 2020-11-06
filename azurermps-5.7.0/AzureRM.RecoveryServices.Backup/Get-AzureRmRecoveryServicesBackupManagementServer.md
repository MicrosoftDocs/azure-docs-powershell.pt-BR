---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 0dac27b7e17a9336db198906cdfb60fb15738795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427497"
---
# Get-AzureRmRecoveryServicesBackupManagementServer

## Sinopse
Obtém servidores de gerenciamento de backup do SCDPM e do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesBackupManagementServer** Obtém uma lista de servidores de gerenciamento de backup que são registrados em um cofre.

Há dois tipos de servidores de gerenciamento de backup: o System Center Data Protection Manager (SCDPM) e os servidores de gerenciamento de backup do Azure.
Os servidores de gerenciamento de backup são instalados separadamente para gerenciar a orquestração de backup.

Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.

## EXEMPLOS

### Exemplo 1: obter todos os servidores de gerenciamento de backup
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

Esse comando obtém todos os servidores de gerenciamento de backup registrados no cofre.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do servidor de gerenciamento de backup a ser obtido.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. BackupEngineBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. BackupEngineBase]

## INFORMA

## LINKS RELACIONADOS

[Cancelar registro-AzureRmRecoveryServicesBackupManagementServer](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


