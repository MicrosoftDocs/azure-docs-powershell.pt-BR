---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428286"
---
# Get-AzureRmBackupRecoveryPoint

## Sinopse
Obtém os pontos de recuperação para um item de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBackupRecoveryPoint** Obtém os pontos de recuperação para um item do Azure backup em backup.
Após o backup de um item, o backup armazena um ou mais pontos de recuperação.

## EXEMPLOS

### Exemplo 1: obter pontos de recuperação para um item
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.
O comando armazena esse objeto na variável $Vault.

O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet **Get-AzureRmBackupContainer** .
O comando armazena esse objeto na variável $Container.

O terceiro comando obtém o item de backup no contêiner no $Container usando o cmdlet **Get-AzureRmBackupItem** .
O comando armazena esse objeto na variável $BackupItem.

O comando final Obtém pontos de recuperação para o item em $BackupItem.

## OS

### -Item
Especifica o item para o qual esse cmdlet recebe pontos de recuperação.
Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPointId
Especifica a ID de um ponto de recuperação que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

### AzureRmBackupItem

## EXIBE

### AzureRmBackupRecoveryPoint

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


