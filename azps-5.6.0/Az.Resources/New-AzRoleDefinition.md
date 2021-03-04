---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888193"
---
# New-AzRoleDefinition

## SYNOPSIS
Cria uma função personalizada no Azure RBAC.
Forneça um arquivo de definição de função JSON ou um objeto PSRoleDefinition como entrada.
Primeiro, use o comando Get-AzRoleDefinition para gerar um objeto de definição de função de linha de base.
Em seguida, modifique suas propriedades conforme necessário.
Por fim, use este comando para criar uma função personalizada usando a definição de função.

## SINTAXE

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O New-AzRoleDefinition cmdlet cria uma função personalizada no Azure Role-Based Access Control.
Forneça uma definição de função como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.
A definição da função de entrada DEVE conter as seguintes propriedades:
1) DisplayName: o nome da função personalizada
2) Descrição: uma breve descrição da função que resume o acesso que a função concede.
3) Ações: o conjunto de operações às quais a função personalizada concede acesso.
Use Get-AzProviderOperation para obter a operação para provedores de recursos do Azure que podem ser protegidos usando o Azure RBAC.
A seguir estão algumas cadeias de caracteres de operação válidas:
 - "*/leitura" concede acesso a operações de leitura de todos os provedores de recursos do Azure.
 - "Microsoft.Network/*/read" concede acesso a operações de leitura para todos os tipos de recursos no provedor de recursos Microsoft.Network do Azure.
 - "Microsoft.Compute/virtualMachines/*" concede acesso a todas as operações de máquinas virtuais e seus tipos de recursos filho.
4) AssignableScopes: o conjunto de escopos (assinaturas do Azure ou grupos de recursos) nos quais a função personalizada estará disponível para atribuição.
Usando AssignableScopes, você pode disponibilizar a função personalizada para atribuição apenas nas assinaturas ou grupos de recursos que precisam dela e não atrapalhar a experiência do usuário para o restante das assinaturas ou grupos de recursos.
A seguir estão alguns escopos atribuíveis válidos:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": disponibiliza a função para atribuição em duas assinaturas.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": disponibiliza a função para atribuição em uma única assinatura.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": disponibiliza a função para atribuição somente no grupo de recursos rede.
A definição da função de entrada PODE conter as seguintes propriedades:
1) NotActions: o conjunto de operações que deve ser excluído das Ações para determinar as ações efetivas para a função personalizada.
Se houver uma operação específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar NotActions para exclui-la, em vez de especificar todas as operações que não a operação específica em Actions.
2) DataActions: o conjunto de operações de dados às quais a função personalizada concede acesso.
3) NotDataActions: o conjunto de operações que deve ser excluído dos DataActions para determinar as ações de dados efetivas para a função personalizada.
Se houver uma operação de dados específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar NotDataActions para exclui-la, em vez de especificar todas as operações que não a operação específica em Actions.
OBSERVAÇÃO: Se um usuário receber uma função que especifique uma operação em NotActions e também atribuída outra função concederá acesso à mesma operação - o usuário poderá executar essa operação.
NotActions não é uma regra de negação - é simplesmente uma maneira conveniente de criar um conjunto de operações permitidas quando operações específicas precisam ser excluídas.
A seguir está uma definição de função json de exemplo que pode ser fornecida como entrada { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## EXEMPLOS

### Exemplo 1: Criar usando PSRoleDefinitionObject
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### Exemplo 2: Criar usando o arquivo JSON
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -InputFile
Nome do arquivo que contém uma única definição de função json.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Objeto de definição de função.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## NOTES
Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS RELACIONADOS

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

