---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281607"
---
# <span data-ttu-id="9be25-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9be25-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="9be25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9be25-102">SYNOPSIS</span></span>
<span data-ttu-id="9be25-103">Cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="9be25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9be25-104">SYNTAX</span></span>

### <span data-ttu-id="9be25-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9be25-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9be25-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9be25-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9be25-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9be25-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9be25-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9be25-108">DESCRIPTION</span></span>
<span data-ttu-id="9be25-109">O cmdlet **New-AzPolicySetDefinition** cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="9be25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9be25-110">EXAMPLES</span></span>

### <span data-ttu-id="9be25-111">Exemplo 1: criar uma definição de conjunto de políticas com metadados usando um arquivo de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="9be25-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="9be25-112">Esse comando cria uma definição de conjunto de políticas denominada VMPolicySetDefinition com metadados indicando que sua categoria é "máquina virtual" que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="9be25-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9be25-113">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="9be25-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="9be25-114">Exemplo 2: criar uma definição de conjunto de políticas com parâmetros</span><span class="sxs-lookup"><span data-stu-id="9be25-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="9be25-115">Esse comando cria uma definição de conjunto de políticas parametrizada chamada VMPolicySetDefinition que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="9be25-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9be25-116">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="9be25-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="9be25-117">Exemplo 3: criar uma definição de conjunto de políticas com grupos de definições de política</span><span class="sxs-lookup"><span data-stu-id="9be25-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="9be25-118">Esse comando cria uma definição de conjunto de políticas chamada VMPolicySetDefinition com o agrupamento de definições de política especificado em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="9be25-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="9be25-119">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="9be25-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="9be25-120">OS</span><span class="sxs-lookup"><span data-stu-id="9be25-120">PARAMETERS</span></span>

### <span data-ttu-id="9be25-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9be25-121">-ApiVersion</span></span>
<span data-ttu-id="9be25-122">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9be25-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9be25-123">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9be25-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9be25-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be25-124">-DefaultProfile</span></span>
<span data-ttu-id="9be25-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9be25-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9be25-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9be25-126">-Description</span></span>
<span data-ttu-id="9be25-127">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="9be25-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9be25-128">-DisplayName</span></span>
<span data-ttu-id="9be25-129">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="9be25-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="9be25-130">-GroupDefinition</span></span>
<span data-ttu-id="9be25-131">Os grupos de definições de política para a nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="9be25-132">Isso pode ser um caminho para um arquivo que contém os grupos ou os grupos como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="9be25-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="9be25-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9be25-133">-ManagementGroupName</span></span>
<span data-ttu-id="9be25-134">O nome do grupo de gerenciamento da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="9be25-135">-Metadados</span><span class="sxs-lookup"><span data-stu-id="9be25-135">-Metadata</span></span>
<span data-ttu-id="9be25-136">Os metadados da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-136">The metadata for policy set definition.</span></span> <span data-ttu-id="9be25-137">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="9be25-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="9be25-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="9be25-138">-Name</span></span>
<span data-ttu-id="9be25-139">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="9be25-140">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9be25-140">-Parameter</span></span>
<span data-ttu-id="9be25-141">A declaração Parameters para a definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="9be25-142">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="9be25-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="9be25-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9be25-143">-PolicyDefinition</span></span>
<span data-ttu-id="9be25-144">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="9be25-144">The policy definitions.</span></span> <span data-ttu-id="9be25-145">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou as definições da política como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="9be25-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="9be25-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="9be25-146">-Pre</span></span>
<span data-ttu-id="9be25-147">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9be25-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9be25-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9be25-148">-SubscriptionId</span></span>
<span data-ttu-id="9be25-149">A ID da assinatura da nova definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9be25-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="9be25-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9be25-150">-Confirm</span></span>
<span data-ttu-id="9be25-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9be25-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9be25-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9be25-152">-WhatIf</span></span>
<span data-ttu-id="9be25-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9be25-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9be25-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9be25-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9be25-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be25-155">CommonParameters</span></span>
<span data-ttu-id="9be25-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be25-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be25-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9be25-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be25-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9be25-158">INPUTS</span></span>

### <span data-ttu-id="9be25-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9be25-159">System.String</span></span>

### <span data-ttu-id="9be25-160">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9be25-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9be25-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9be25-161">OUTPUTS</span></span>

### <span data-ttu-id="9be25-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9be25-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9be25-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9be25-163">NOTES</span></span>

## <span data-ttu-id="9be25-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9be25-164">RELATED LINKS</span></span>
