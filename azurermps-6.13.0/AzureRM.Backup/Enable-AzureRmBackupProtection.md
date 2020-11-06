---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c66eda488b0b7876317b02db279202a88bbcc3d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431436"
---
# Enable-AzureRmBackupProtection

## Sinopse
Associa um item a uma política de proteção de backup do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzureRmBackupProtection** associa um item a uma política de proteção de backup do Azure.
Para habilitar uma política de proteção, você deve primeiro ter um item de backup existente e uma política existente.
Ambas devem pertencer ao mesmo cofre de backup.
O agendamento de backup faz a cópia inicial completa para o item e a cópia incremental dos backups subsequentes.

## EXEMPLOS

### Exemplo 1: habilitar a proteção em uma máquina virtual do Azure
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .
O comando armazena esse objeto na variável $Vault.
O segundo comando obtém a política de proteção de backup chamada DefaultPolicy para o cofre em $Vault.
O comando armazena esse objeto na variável $Policy.
O comando final usa o operador pipeline para passar valores de um cmdlet para o seguinte.
Ele obtém um contêiner, usando o cmdlet Get-AzureRmBackupContainer.
O comando obtém o item de backup desse contêiner usando o cmdlet Get-AzureRmBackupItem.
O cmdlet atual habilita a política armazenada em $Policy para o item que o comando passa para esse cmdlet.

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

### -Item
Especifica o item de backup para o qual esse cmdlet habilita a proteção.
Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Política
Especifica a política de proteção que este cmdlet associa a um item.
Para obter um objeto **AzureRmBackupProtectionPolicy** , use o cmdlet Get-AzureRmBackupProtectionPolicy.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainerContextObject
Parâmetros: Item (ByValue)

## EXIBE

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## INFORMA

## LINKS RELACIONADOS

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


