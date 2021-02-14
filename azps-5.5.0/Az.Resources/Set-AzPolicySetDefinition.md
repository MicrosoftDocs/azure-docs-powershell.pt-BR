---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117170"
---
# <span data-ttu-id="e0491-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e0491-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="e0491-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0491-102">SYNOPSIS</span></span>
<span data-ttu-id="e0491-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="e0491-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="e0491-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0491-104">SYNTAX</span></span>

### <span data-ttu-id="e0491-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0491-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0491-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0491-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0491-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0491-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0491-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0491-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0491-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0491-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0491-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0491-110">DESCRIPTION</span></span>
<span data-ttu-id="e0491-111">O cmdlet **Set-AzPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="e0491-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="e0491-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0491-112">EXAMPLES</span></span>

### <span data-ttu-id="e0491-113">Exemplo 1: Atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="e0491-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="e0491-114">O primeiro comando obtém uma definição de conjunto de políticas usando Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0491-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="e0491-115">O comando armazena esse objeto na variável $PolicySetDefinition dados.</span><span class="sxs-lookup"><span data-stu-id="e0491-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="e0491-116">O segundo comando atualiza a descrição da definição de conjunto de políticas identificada pela propriedade **ResourceId** da $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e0491-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="e0491-117">Exemplo 2: Atualizar os metadados de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="e0491-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="e0491-118">Esse comando atualiza os metadados de uma definição de conjunto de políticas chamada VMPolicySetDefinition para indicar que sua categoria é "Máquina Virtual".</span><span class="sxs-lookup"><span data-stu-id="e0491-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="e0491-119">Exemplo 3: Atualizar os grupos de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="e0491-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="e0491-120">Esse comando atualiza os grupos de uma definição de conjunto de políticas chamada VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e0491-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="e0491-121">Exemplo 4: Atualizar os grupos de uma definição de conjunto de políticas usando uma tabela hash</span><span class="sxs-lookup"><span data-stu-id="e0491-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="e0491-122">Esse comando atualiza os grupos de uma definição de conjunto de políticas chamada VMPolicySetDefinition usando uma tabela hash para construir os grupos.</span><span class="sxs-lookup"><span data-stu-id="e0491-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="e0491-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0491-123">PARAMETERS</span></span>

### <span data-ttu-id="e0491-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e0491-124">-ApiVersion</span></span>
<span data-ttu-id="e0491-125">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e0491-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e0491-126">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e0491-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e0491-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0491-127">-DefaultProfile</span></span>
<span data-ttu-id="e0491-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e0491-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0491-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e0491-129">-Description</span></span>
<span data-ttu-id="e0491-130">A descrição para definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e0491-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="e0491-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e0491-131">-DisplayName</span></span>
<span data-ttu-id="e0491-132">O nome de exibição para definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e0491-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="e0491-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="e0491-133">-GroupDefinition</span></span>
<span data-ttu-id="e0491-134">Os grupos de definição de política da definição de conjunto de políticas atualizada.</span><span class="sxs-lookup"><span data-stu-id="e0491-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="e0491-135">Isso pode ser um caminho para um arquivo que contém os grupos ou os grupos como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="e0491-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="e0491-136">-ID</span><span class="sxs-lookup"><span data-stu-id="e0491-136">-Id</span></span>
<span data-ttu-id="e0491-137">A ID de definição de política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0491-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="e0491-138">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e0491-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e0491-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0491-139">-InputObject</span></span>
<span data-ttu-id="e0491-140">O objeto de definição de conjunto de políticas para atualizar que foi saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0491-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="e0491-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e0491-141">-ManagementGroupName</span></span>
<span data-ttu-id="e0491-142">O nome do grupo de gerenciamento da definição de conjunto de políticas a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e0491-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="e0491-143">-Metadados</span><span class="sxs-lookup"><span data-stu-id="e0491-143">-Metadata</span></span>
<span data-ttu-id="e0491-144">Os metadados da definição de conjunto de políticas atualizados.</span><span class="sxs-lookup"><span data-stu-id="e0491-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="e0491-145">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="e0491-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="e0491-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0491-146">-Name</span></span>
<span data-ttu-id="e0491-147">O nome de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e0491-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="e0491-148">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0491-148">-Parameter</span></span>
<span data-ttu-id="e0491-149">A declaração de parâmetros da definição de conjunto de políticas atualizada.</span><span class="sxs-lookup"><span data-stu-id="e0491-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="e0491-150">Isso pode ser um caminho para um nome de arquivo ou uri que contém a declaração de parâmetros ou a declaração de parâmetros como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="e0491-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="e0491-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e0491-151">-PolicyDefinition</span></span>
<span data-ttu-id="e0491-152">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="e0491-152">The policy definitions.</span></span> <span data-ttu-id="e0491-153">Isso pode ser um caminho para um nome de arquivo que contém as definições de política ou as definições de política como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="e0491-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="e0491-154">-Pré-</span><span class="sxs-lookup"><span data-stu-id="e0491-154">-Pre</span></span>
<span data-ttu-id="e0491-155">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e0491-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e0491-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0491-156">-SubscriptionId</span></span>
<span data-ttu-id="e0491-157">A ID da assinatura da definição de conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e0491-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="e0491-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0491-158">-Confirm</span></span>
<span data-ttu-id="e0491-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0491-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0491-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0491-160">-WhatIf</span></span>
<span data-ttu-id="e0491-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0491-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0491-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0491-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0491-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0491-163">CommonParameters</span></span>
<span data-ttu-id="e0491-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0491-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0491-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0491-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0491-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0491-166">INPUTS</span></span>

### <span data-ttu-id="e0491-167">System.String</span><span class="sxs-lookup"><span data-stu-id="e0491-167">System.String</span></span>

### <span data-ttu-id="e0491-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e0491-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e0491-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0491-169">OUTPUTS</span></span>

### <span data-ttu-id="e0491-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e0491-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e0491-171">Notas</span><span class="sxs-lookup"><span data-stu-id="e0491-171">NOTES</span></span>

## <span data-ttu-id="e0491-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0491-172">RELATED LINKS</span></span>
