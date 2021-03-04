---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: ae1cc96cd617ec74a69fc2c95ec50973e688ebe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890983"
---
# <span data-ttu-id="7813a-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="7813a-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="7813a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7813a-102">SYNOPSIS</span></span>
<span data-ttu-id="7813a-103">Cria uma definição de conjunto de política.</span><span class="sxs-lookup"><span data-stu-id="7813a-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="7813a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7813a-104">SYNTAX</span></span>

### <span data-ttu-id="7813a-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7813a-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7813a-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7813a-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7813a-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7813a-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7813a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7813a-108">DESCRIPTION</span></span>
<span data-ttu-id="7813a-109">O cmdlet **New-AzPolicySetDefinition** cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="7813a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7813a-110">EXAMPLES</span></span>

### <span data-ttu-id="7813a-111">Exemplo 1: Criar uma definição de conjunto de política com metadados usando um arquivo de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="7813a-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="7813a-112">Este comando cria uma definição de conjunto de políticas chamada VMPolicySetDefinition com metadados indicando que sua categoria é "Máquina Virtual" que contém as definições de política especificadas no C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="7813a-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="7813a-113">O conteúdo de exemplo do VMPolicy.json é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="7813a-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="7813a-114">Exemplo 2: Criar uma definição de conjunto de políticas parametrizado</span><span class="sxs-lookup"><span data-stu-id="7813a-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="7813a-115">Este comando cria uma definição de conjunto de diretivas parametrizada chamada VMPolicySetDefinition que contém as definições de política especificadas no C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="7813a-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="7813a-116">O conteúdo de exemplo do VMPolicy.json é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="7813a-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="7813a-117">Exemplo 3: Criar uma definição de conjunto de políticas com grupos de definição de política</span><span class="sxs-lookup"><span data-stu-id="7813a-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="7813a-118">Este comando cria uma definição de conjunto de políticas chamada VMPolicySetDefinition com o agrupamento de definições de política especificadas em C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="7813a-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="7813a-119">O conteúdo de exemplo do VMPolicy.json é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="7813a-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="7813a-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7813a-120">PARAMETERS</span></span>

### <span data-ttu-id="7813a-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7813a-121">-ApiVersion</span></span>
<span data-ttu-id="7813a-122">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7813a-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7813a-123">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="7813a-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7813a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7813a-124">-DefaultProfile</span></span>
<span data-ttu-id="7813a-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7813a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7813a-126">-Description</span><span class="sxs-lookup"><span data-stu-id="7813a-126">-Description</span></span>
<span data-ttu-id="7813a-127">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="7813a-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7813a-128">-DisplayName</span></span>
<span data-ttu-id="7813a-129">O nome de exibição para definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="7813a-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="7813a-130">-GroupDefinition</span></span>
<span data-ttu-id="7813a-131">Os grupos de definição de política para a nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="7813a-132">Isso pode ser um caminho para um arquivo que contém os grupos ou os grupos como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="7813a-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="7813a-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7813a-133">-ManagementGroupName</span></span>
<span data-ttu-id="7813a-134">O nome do grupo de gerenciamento da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="7813a-135">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7813a-135">-Metadata</span></span>
<span data-ttu-id="7813a-136">Os metadados para definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-136">The metadata for policy set definition.</span></span> <span data-ttu-id="7813a-137">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="7813a-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="7813a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="7813a-138">-Name</span></span>
<span data-ttu-id="7813a-139">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7813a-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7813a-140">-Parameter</span></span>
<span data-ttu-id="7813a-141">A declaração de parâmetros para definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="7813a-142">Isso pode ser um caminho para um nome de arquivo que contém a declaração de parâmetros ou a declaração de parâmetros como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="7813a-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="7813a-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7813a-143">-PolicyDefinition</span></span>
<span data-ttu-id="7813a-144">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="7813a-144">The policy definitions.</span></span> <span data-ttu-id="7813a-145">Isso pode ser um caminho para um nome de arquivo que contém as definições de política ou as definições de política como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="7813a-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7813a-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="7813a-146">-Pre</span></span>
<span data-ttu-id="7813a-147">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7813a-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7813a-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7813a-148">-SubscriptionId</span></span>
<span data-ttu-id="7813a-149">A ID da assinatura da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7813a-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="7813a-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7813a-150">-Confirm</span></span>
<span data-ttu-id="7813a-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7813a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7813a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7813a-152">-WhatIf</span></span>
<span data-ttu-id="7813a-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7813a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7813a-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7813a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7813a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7813a-155">CommonParameters</span></span>
<span data-ttu-id="7813a-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7813a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7813a-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7813a-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7813a-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7813a-158">INPUTS</span></span>

### <span data-ttu-id="7813a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="7813a-159">System.String</span></span>

### <span data-ttu-id="7813a-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7813a-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7813a-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7813a-161">OUTPUTS</span></span>

### <span data-ttu-id="7813a-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="7813a-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7813a-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="7813a-163">NOTES</span></span>

## <span data-ttu-id="7813a-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7813a-164">RELATED LINKS</span></span>
