---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 40747a82cab67a61e6a65e9eba4f3ba6ebc66f96
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776382"
---
# New-AzRoleDefinition

## Sinopse
Cria uma função personalizada no Azure RBAC.
Forneça um arquivo de definição de função JSON ou um objeto PSRoleDefinition como entrada.
Primeiro, use o comando Get-AzRoleDefinition para gerar um objeto de definição de função de linha de base.
Em seguida, modifique suas propriedades conforme necessário.
Por fim, use esse comando para criar uma função personalizada usando definição de função.

## SYNTAX

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzRoleDefinition cria uma função personalizada no controle de acesso do Azure Role-Based.
Forneça uma definição de função como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.
A definição da função de entrada deve conter as seguintes propriedades:
1) DisplayName: o nome da função personalizada
2) Descrição: uma breve descrição da função que resume o acesso concedido pela função.
3) Ações: o conjunto de operações às quais a função personalizada concede acesso.
Use Get-AzProviderOperation para obter a operação dos provedores de recursos do Azure que podem ser protegidos usando o Azure RBAC.
Veja a seguir algumas cadeias de caracteres de operação válidas:
 - "*/Read" concede acesso a operações de leitura de todos os provedores de recursos do Azure.
 - "Microsoft. Network/*/Read" concede acesso a operações de leitura para todos os tipos de recursos do provedor de recursos da Microsoft. Network do Azure.
 - "Microsoft. Compute/virtualMachines/*" concede acesso a todas as operações de máquinas virtuais e seus tipos de recursos filhos.
4) AssignableScopes: o conjunto de escopos (assinaturas do Azure ou grupos de recursos) em que a função personalizada estará disponível para a atribuição.
Usando o AssignableScopes, você pode disponibilizar a função personalizada para atribuição somente em assinaturas ou grupos de recursos que precisarem, e não truncar a experiência do usuário para o restante das assinaturas ou grupos de recursos.
Veja a seguir alguns escopos atribuíveis válidos:
 - "/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": torna a função disponível para a atribuição em duas assinaturas.
 - "/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e": torna a função disponível para a atribuição em uma única assinatura.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": torna a função disponível para a atribuição somente no grupo de recursos de rede.
A definição da função de entrada pode conter as seguintes propriedades:
1) Ações: o conjunto de operações que devem ser excluídas das ações para determinar as ações efetivas para a função personalizada.
Se houver uma operação específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar as ações para excluí-lo, em vez de especificar todas as operações que não sejam uma operação específica em ações.
2) Dataactions: o conjunto de operações de dados às quais a função personalizada concede acesso.
3) NotDataActions: o conjunto de operações que devem ser excluídas da dataactions para determinar as ações de dataacção efetivas para a função personalizada.
Se houver uma operação de dados específica para a qual você não deseja conceder acesso em uma função personalizada, é conveniente usar o NotDataActions para excluí-lo, em vez de especificar todas as operações que não sejam uma operação específica em ações.
Observação: se um usuário é atribuído a uma função que especifica uma operação em minhas ações e também uma outra função concede acesso à mesma operação-o usuário poderá executar essa operação.
Não é uma regra de negação-é simplesmente uma maneira conveniente de criar um conjunto de operações permitidas quando operações específicas precisam ser excluídas.
Veja a seguir uma definição de função JSON de exemplo que pode ser fornecida como entrada {"nome": "função Updated", "Descrição": "pode monitorar todos os recursos e iniciar e reiniciar máquinas virtuais", "ações": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/reiniciar/ação", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]

## EXEMPLOS

### Criar usando PSRoleDefinitionObject
```
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

### Criar usando um arquivo JSON
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
Nome do arquivo que contém uma única definição de função JSON.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## INFORMA
Palavras-chave: Azure, AZ, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

