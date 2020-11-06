---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: 3bbddc217bd33e303b998bfb816c9c0c65e96ce6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428604"
---
# Restore-AzureRmBackupItem

## Sinopse
Restaura os dados e a configuração de um item de backup para um ponto de recuperação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Restore-AzureRmBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.
Esse cmdlet inicia a restauração do cofre de backup para a sua conta.
A operação de restauração não restaura a máquina virtual completa.
Ele restaura os dados de disco e as informações de configuração.
Após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.

## EXEMPLOS

### Exemplo 1: restaurar uma máquina virtual para um ponto de recuperação
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.
O comando armazena esse objeto na variável $Vault.
O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet **Get-AzureRmBackupContainer** .
O comando armazena esse objeto na variável $Container.
O terceiro comando obtém o item de backup no contêiner no $Container usando o cmdlet **Get-AzureRmBackupItem** .
O comando armazena esse objeto na variável $BackupItem.
O quarto comando obtém o ponto de recuperação do item em $BackupItem.
O comando armazena esse objeto na variável $RecoveryPoint.
O comando final restaura o ponto de recuperação no $RecoveryPoint para a conta chamada DestinationAccount.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -RecoveryPoint
Especifica o ponto de recuperação no qual restaurar a máquina virtual.
Para obter um **AzureRmBackupRecoveryPoint** , use o cmdlet Get-AzureRmBackupRecoveryPoint.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento de destino na sua assinatura.
Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRecoveryPoint
Parâmetros: RecoveryPoint (ByValue)

## EXIBE

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## INFORMA

## LINKS RELACIONADOS

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupRecoveryPoint](./Get-AzureRmBackupRecoveryPoint.md)


