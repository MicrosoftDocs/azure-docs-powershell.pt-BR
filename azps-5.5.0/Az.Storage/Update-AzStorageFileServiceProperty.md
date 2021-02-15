---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116084"
---
# Update-AzStorageFileServiceProperty

## Sinopse
Modifica as propriedades de serviço do serviço Arquivo de Armazenamento do Azure.

## Sintaxe

### Nomeda Conta (Padrão)
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FileServicePropertiesResourceId
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Update-AzStorageFileServiceProperty** modifica as propriedades de serviço do serviço Arquivo de Armazenamento do Azure.

## Exemplos

### Exemplo 1: Habilitar o softdelete do compartilhamento de arquivos
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

Este comando permite que o compartilhamento de arquivos exclua softdelete com dias de retenção como 5

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -EnableShareDeleteRetentionPolicy
Habilitar o compartilhamento da Política de Retenção de Exclusão para a conta de armazenamento definida como $true, desabilite o compartilhamento da Política de Retenção de Exclusão definida como $false.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Inserir uma ID de Recurso de conta de armazenamento ou uma ID de Recurso de propriedades do serviço de arquivo.

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShareRetentionDays
Define o número de dias de retenção para o compartilhamento DeleteRetentionPolicy.
O valor só deve ser definido quando habilitar a Política de Retenção de Exclusão de compartilhamento.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
Objeto de conta de armazenamento

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Nome da Conta de Armazenamento.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

### System.String

## Saídas

### Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties

## Notas

## LINKS RELACIONADOS
