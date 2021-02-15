---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114903"
---
# <span data-ttu-id="66f20-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="66f20-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="66f20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66f20-102">SYNOPSIS</span></span>
<span data-ttu-id="66f20-103">Cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="66f20-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f20-104">SYNTAX</span></span>

### <span data-ttu-id="66f20-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66f20-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66f20-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f20-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66f20-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f20-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66f20-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="66f20-108">DESCRIPTION</span></span>
<span data-ttu-id="66f20-109">O cmdlet **New-AzPolicySetDefinition** cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="66f20-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66f20-110">EXAMPLES</span></span>

### <span data-ttu-id="66f20-111">Exemplo 1: Criar uma definição de conjunto de política com metadados usando um arquivo de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="66f20-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="66f20-112">Esse comando cria uma definição de conjunto de política chamada VMPolicySetDefinition com metadados indicando que sua categoria é "Máquina Virtual" que contém as definições de política especificadas em C:\VMPolicy.jsem.</span><span class="sxs-lookup"><span data-stu-id="66f20-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="66f20-113">O conteúdo de exemplo do VMPolicy.jsé fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="66f20-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="66f20-114">Exemplo 2: Criar uma definição de conjunto de políticas parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f20-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="66f20-115">Esse comando cria uma definição de conjunto de política parametrizado chamada VMPolicySetDefinition que contém as definições de política especificadas no C:\VMPolicy.jsem.</span><span class="sxs-lookup"><span data-stu-id="66f20-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="66f20-116">O conteúdo de exemplo do VMPolicy.jsé fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="66f20-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="66f20-117">Exemplo 3: Criar uma definição de conjunto de políticas com grupos de definição de política</span><span class="sxs-lookup"><span data-stu-id="66f20-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="66f20-118">Esse comando cria uma definição de conjunto de políticas chamada VMPolicySetDefinition com o grupo de definições de política especificadas no C:\VMPolicy.jsem.</span><span class="sxs-lookup"><span data-stu-id="66f20-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="66f20-119">O conteúdo de exemplo do VMPolicy.jsé fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="66f20-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="66f20-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f20-120">PARAMETERS</span></span>

### <span data-ttu-id="66f20-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66f20-121">-ApiVersion</span></span>
<span data-ttu-id="66f20-122">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="66f20-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="66f20-123">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="66f20-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="66f20-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f20-124">-DefaultProfile</span></span>
<span data-ttu-id="66f20-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="66f20-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66f20-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="66f20-126">-Description</span></span>
<span data-ttu-id="66f20-127">A descrição para definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="66f20-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66f20-128">-DisplayName</span></span>
<span data-ttu-id="66f20-129">O nome de exibição para definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="66f20-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="66f20-130">-GroupDefinition</span></span>
<span data-ttu-id="66f20-131">Os grupos de definição de política para a nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="66f20-132">Isso pode ser um caminho para um arquivo que contém os grupos ou os grupos como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="66f20-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="66f20-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="66f20-133">-ManagementGroupName</span></span>
<span data-ttu-id="66f20-134">O nome do grupo de gerenciamento da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="66f20-135">-Metadados</span><span class="sxs-lookup"><span data-stu-id="66f20-135">-Metadata</span></span>
<span data-ttu-id="66f20-136">Os metadados para definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-136">The metadata for policy set definition.</span></span> <span data-ttu-id="66f20-137">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="66f20-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="66f20-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="66f20-138">-Name</span></span>
<span data-ttu-id="66f20-139">O nome de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="66f20-140">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f20-140">-Parameter</span></span>
<span data-ttu-id="66f20-141">A declaração de parâmetros para definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="66f20-142">Isso pode ser um caminho para um nome de arquivo que contém a declaração de parâmetros ou a declaração de parâmetros como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="66f20-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="66f20-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66f20-143">-PolicyDefinition</span></span>
<span data-ttu-id="66f20-144">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="66f20-144">The policy definitions.</span></span> <span data-ttu-id="66f20-145">Isso pode ser um caminho para um nome de arquivo que contém as definições de política ou as definições de política como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="66f20-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="66f20-146">-Pré-</span><span class="sxs-lookup"><span data-stu-id="66f20-146">-Pre</span></span>
<span data-ttu-id="66f20-147">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="66f20-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66f20-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66f20-148">-SubscriptionId</span></span>
<span data-ttu-id="66f20-149">A ID da assinatura da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="66f20-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="66f20-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66f20-150">-Confirm</span></span>
<span data-ttu-id="66f20-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66f20-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66f20-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f20-152">-WhatIf</span></span>
<span data-ttu-id="66f20-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66f20-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66f20-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66f20-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66f20-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f20-155">CommonParameters</span></span>
<span data-ttu-id="66f20-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f20-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f20-157">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66f20-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f20-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="66f20-158">INPUTS</span></span>

### <span data-ttu-id="66f20-159">System.String</span><span class="sxs-lookup"><span data-stu-id="66f20-159">System.String</span></span>

### <span data-ttu-id="66f20-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66f20-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="66f20-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="66f20-161">OUTPUTS</span></span>

### <span data-ttu-id="66f20-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="66f20-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66f20-163">Notas</span><span class="sxs-lookup"><span data-stu-id="66f20-163">NOTES</span></span>

## <span data-ttu-id="66f20-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66f20-164">RELATED LINKS</span></span>
