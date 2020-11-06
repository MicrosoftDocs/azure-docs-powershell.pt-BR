---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428596"
---
# Set-AzureRmBackupVault

## Sinopse
Altera o tipo de armazenamento de um cofre de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmBackupVault** altera o tipo de armazenamento de um cofre de backup do Azure.
Não é possível modificar outras propriedades de um cofre.

## EXEMPLOS

### Exemplo 1: alterar o armazenamento de um cofre existente
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

Esse comando obtém o cofre de backup do Azure chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .
O comando passa o cofre para o cmdlet atual usando o operador pipeline.
O cmdlet atual altera o tipo de armazenamento para LocallyRedundant.

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

### -Armazenamento
Especifica o tipo de armazenamento dos dados de backup.
Os valores aceitáveis para esse parâmetro são: LocallyRedundant e georedundantes.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cofre
Especifica um cofre de backup que é modificado por esse cmdlet.
Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Parâmetros: cofre (ByValue)

## EXIBE

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault

## INFORMA
* Quando você registra o primeiro servidor ou máquina virtual para um cofre, o tipo de armazenamento fica bloqueado. Em seguida, você não pode alterar o tipo de armazenamento.

## LINKS RELACIONADOS

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)


