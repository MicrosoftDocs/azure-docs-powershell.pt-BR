---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112631"
---
# New-AzRoleDefinition

## Sinopse
Cria uma função personalizada no Azure RBAC.
Forneça um arquivo de definição de função JSON ou um objeto PSRoleDefinition como entrada.
Primeiro, use o comando Get-AzRoleDefinition para gerar um objeto de definição de função de linha de base.
Em seguida, modifique suas propriedades conforme necessário.
Por fim, use esse comando para criar uma função personalizada usando a definição de função.

## Sintaxe

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O New-AzRoleDefinition cmdlet cria uma função personalizada no Azure Role-Based Access Control.
Forneça uma definição de função como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.
A definição da função de entrada DEVE conter as seguintes propriedades:
1) DisplayName: o nome da função personalizada
2) Descrição: uma breve descrição da função que resume o acesso concedido pela função.
3) Ações: o conjunto de operações às quais a função personalizada concede acesso.
Use Get-AzProviderOperation para obter a operação para provedores de recursos do Azure que podem ser protegidos usando o Azure RBAC.
A seguir estão algumas cadeias de caracteres de operação válidas:
 - "*/leitura" concede acesso a operações de leitura de todos os provedores de recursos do Azure.
 - "Microsoft.Network/*/read" concede acesso a operações de leitura para todos os tipos de recursos no provedor de recursos Microsoft.Network do Azure.
 - "Microsoft.Compute/virtualMachines/*" concede acesso a todas as operações de máquinas virtuais e seus tipos de recursos filho.
4) AssignableScopes: o conjunto de escopos (assinaturas ou grupos de recursos do Azure) no qual a função personalizada estará disponível para atribuição.
Usando o AssignableScopes, você pode disponibilizar a função personalizada para atribuição apenas nas assinaturas ou grupos de recursos que precisam dela e não atrapalhar a experiência do usuário para o restante das assinaturas ou grupos de recursos.
A seguir estão alguns escopos atribuíveis válidos:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": disponibiliza a função para atribuição em duas assinaturas.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": disponibiliza a função para atribuição em uma única assinatura.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": disponibiliza a função para atribuição somente no grupo de recursos rede.
A definição da função de entrada PODE conter as seguintes propriedades:
1) NotActions: o conjunto de operações que deve ser excluído das Ações para determinar as ações efetivas para a função personalizada.
Se houver uma operação específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar NotActions para exclui-la, em vez de especificar todas as operações que não a operação específica em Ações.
2) DataActions: o conjunto de operações de dados às quais a função personalizada concede acesso.
3) NotDataActions: o conjunto de operações que deve ser excluído das DataActions para determinar as ações de dados efetivas para a função personalizada.
Se houver uma operação de dados específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar NotDataActions para exclui-la, em vez de especificar todas as operações além dessa operação específica em Ações.
OBSERVAÇÃO: se um usuário receber uma função que especifique uma operação em NotActions e também atribuída outra função concederá acesso à mesma operação, o usuário poderá executar essa operação.
NotActions não é uma regra de negação, é simplesmente uma maneira conveniente de criar um conjunto de operações permitidas quando operações específicas precisam ser excluídas.
Veja a seguir uma definição de função json de exemplo que pode ser fornecida como entrada { "Nome": "Função atualizada", "Descrição": "Pode monitorar todos os recursos e iniciar e reiniciar máquinas virtuais", "Ações": \[ "*/ler", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## Exemplos

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

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
Nome de arquivo que contém uma única definição de função json.

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

### -Função
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## Notas
Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS RELACIONADOS

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

