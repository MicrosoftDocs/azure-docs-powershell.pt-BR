---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: fab07b94c565a37d2884c5074de9f23692878df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893119"
---
# Set-AzPolicySetDefinition

## SYNOPSIS
Modifica uma definição de conjunto de políticas

## SINTAXE

### NameParameterSet (Padrão)
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagementGroupNameParameterSet
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SubscriptionIdParameterSet
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### IdParameterSet
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectParameterSet
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzPolicySetDefinition** modifica uma definição de política.

## EXEMPLOS

### Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzPolicySetDefinition de segurança.
O comando armazena esse objeto na variável $PolicySetDefinition.
O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela **propriedade ResourceId** do $PolicySetDefinition.

### Exemplo 2: atualizar os metadados de uma definição de conjunto de políticas
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

Este comando atualiza os metadados de uma definição de conjunto de políticas chamada VMPolicySetDefinition para indicar que sua categoria é "Máquina Virtual".

### Exemplo 3: atualizar os grupos de uma definição de conjunto de políticas
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

Este comando atualiza os grupos de uma definição de conjunto de políticas chamada VMPolicySetDefinition.

### Exemplo 4: atualizar os grupos de uma definição de conjunto de políticas usando uma tabela de hash
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

Este comando atualiza os grupos de uma definição de conjunto de políticas chamada VMPolicySetDefinition usando uma tabela de hash para construir os grupos.

## PARÂMETROS

### -ApiVersion
Quando definido, indica a versão da API do provedor de recursos a ser usada.
Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Description
A descrição da definição do conjunto de políticas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
O nome de exibição para definição do conjunto de políticas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupDefinition
Os grupos de definição de política da definição de conjunto de políticas atualizada. Isso pode ser um caminho para um arquivo que contém os grupos ou os grupos como uma cadeia de caracteres JSON.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
A ID de definição de política totalmente qualificada, incluindo a assinatura.
por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
O objeto de definição de conjunto de políticas para atualizar que foi saída de outro cmdlet.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ManagementGroupName
O nome do grupo de gerenciamento da definição de conjunto de políticas a ser atualizada.

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Metadados
Os metadados da definição de conjunto de políticas atualizada. Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres JSON.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
O nome da definição do conjunto de políticas.

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parameter
A declaração de parâmetros da definição de conjunto de políticas atualizada. Isso pode ser um caminho para um nome de arquivo ou uri contendo a declaração de parâmetros ou a declaração de parâmetros como uma cadeia de caracteres JSON.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinition
As definições de política. Isso pode ser um caminho para um nome de arquivo que contém as definições de política ou as definições de política como uma cadeia de caracteres JSON.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura da definição de conjunto de políticas a ser atualizada.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## SAÍDAS

### System.Management.Automation.PSObject

## NOTES

## LINKS RELACIONADOS
