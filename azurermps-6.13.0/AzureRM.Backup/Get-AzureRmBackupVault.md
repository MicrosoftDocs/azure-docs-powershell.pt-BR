---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609417"
---
# Get-AzureRmBackupVault

## Sinopse
Obtém cofres de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBackupVault** Obtém cofres de backup do Azure.
Esse cmdlet retorna objetos **AzureRmBackupVault** para uso com outros cmdlets.

## EXEMPLOS

### Exemplo 1: exibir todos os cofres de backup
```
PS C:\>Get-AzureRmBackupVault
```

Esse comando obtém todos os cofres de backup do Azure.

### Exemplo 2: exibir todos os cofres criados no oeste dos EUA
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Esse comando obtém todos os cofres de backup.
O comando passa a ele para o cmdlet Where-Object usando o operador pipeline.
Esse cmdlet filtra os resultados com base na propriedade **Region** .
Para obter mais informações, digite `Get-Help Where-Object` .

### Exemplo 3: obter um cofre específico
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Esse comando obtém o cofre chamado Vault03.

### Exemplo 4: contar o número de cofres que têm armazenamento redundante localmente
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Esse comando obtém todos os cofres de backup do Azure.
O comando passa essas pessoas para **Where-Object** , que filtra os resultados com base na propriedade **Storage** .
O comando passa aqueles que têm um valor de LocallyRedundant para o cmdlet Measure-Object, que conta os resultados.
Para obter mais informações, digite `Get-Help Measure-Object` .

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

### -Nome
Especifica o nome do cofre de backup que este cmdlet obtém.
Se mais de um cofre de backup tiver o mesmo nome, esse cmdlet retornará todos eles.
Especifique o parâmetro *ResourceGroupName* para obter um cofre exclusivo.

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

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure em que esse cmdlet obtém um cofre de backup.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


