---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427917"
---
# Get-AzureRmKeyVault

## Sinopse
Obtém cofres de chave.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### GetVaultByName
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllVaultsInSubscription
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmKeyVault** Obtém informações sobre os cofres de chaves em uma assinatura. Você pode exibir todas as instâncias de cofre de chaves em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um cofre de chaves específico.

Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet quando você obtém um único cofre de chaves, você deve fazê-lo para obter melhor desempenho.

## EXEMPLOS

### Exemplo 1: obter todos os cofres de chaves na sua assinatura atual
```
PS C:\>Get-AzureRMKeyVault
```

Este comando obtém todos os cofres de chaves na sua assinatura atual.

### Exemplo 2: obter um cofre de chaves específico
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

Esse comando obtém o cofre de chaves chamado Contoso03Vault na sua assinatura atual e, em seguida, armazena-o na variável $MyVault. Você pode inspecionar as propriedades de $MyVault para obter detalhes sobre o cofre de chaves.

### Exemplo 3: obter cofres de chaves em um grupo de recursos
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Esse comando obtém todos os cofres de chaves do grupo de recursos chamado ContosoPayRollResourceGroup.

### Exemplo 4: obter todos os cofres de chaves excluídos na sua assinatura atual
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

Este comando obtém todos os cofres de chaves excluídos na sua assinatura atual.

### Exemplo 5: obter um cofre de chaves excluído
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Este comando obtém as informações de cofre de chave excluídas chamadas Contoso03Vault na sua assinatura atual e na região do eastus2.

## OS

### -Inremovestate
Especifica se os cofres excluídos anteriormente devem ser mostrados na saída.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local do cofre excluído.

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos associado ao cofre de chaves ou a cofres de chaves sendo consultados.

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cofrename
Especifica o nome do cofre de chaves.

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## EXIBE

### Microsoft. Azure. Commands. keyvault. Models. PSVault

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSVaultIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault

### System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmKeyVault](./New-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
