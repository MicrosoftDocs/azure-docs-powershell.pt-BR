---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941734"
---
# <span data-ttu-id="5b1e9-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1e9-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="5b1e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1e9-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="5b1e9-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="5b1e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b1e9-104">SYNTAX</span></span>

### <span data-ttu-id="5b1e9-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5b1e9-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b1e9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1e9-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1e9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1e9-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1e9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1e9-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b1e9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b1e9-109">DESCRIPTION</span></span>
<span data-ttu-id="5b1e9-110">O cmdlet **set-AzPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="5b1e9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b1e9-111">EXAMPLES</span></span>

### <span data-ttu-id="5b1e9-112">Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="5b1e9-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="5b1e9-113">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="5b1e9-114">O comando armazena esse objeto na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="5b1e9-115">O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="5b1e9-116">Exemplo 2: atualizar os metadados de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="5b1e9-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="5b1e9-117">Esse comando atualiza os metadados de uma definição de conjunto de políticas chamado VMPolicySetDefinition para indicar que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="5b1e9-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="5b1e9-118">Exemplo 3: atualizar os grupos de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="5b1e9-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="5b1e9-119">Esse comando atualiza os grupos de uma definição de conjunto de políticas chamado VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="5b1e9-120">Exemplo 4: atualizar os grupos de uma definição de conjunto de políticas usando uma tabela de hash</span><span class="sxs-lookup"><span data-stu-id="5b1e9-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="5b1e9-121">Esse comando atualiza os grupos de uma definição de conjunto de políticas chamado VMPolicySetDefinition usando uma tabela de hash para construir os grupos.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="5b1e9-122">OS</span><span class="sxs-lookup"><span data-stu-id="5b1e9-122">PARAMETERS</span></span>

### <span data-ttu-id="5b1e9-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b1e9-123">-ApiVersion</span></span>
<span data-ttu-id="5b1e9-124">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5b1e9-125">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5b1e9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1e9-126">-DefaultProfile</span></span>
<span data-ttu-id="5b1e9-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5b1e9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b1e9-128">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5b1e9-128">-Description</span></span>
<span data-ttu-id="5b1e9-129">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-129">The description for policy set definition.</span></span>

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

### <span data-ttu-id="5b1e9-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5b1e9-130">-DisplayName</span></span>
<span data-ttu-id="5b1e9-131">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-131">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="5b1e9-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1e9-132">-GroupDefinition</span></span>
<span data-ttu-id="5b1e9-133">Os grupos de definição de política da definição de conjunto de políticas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="5b1e9-134">Isso pode ser um caminho para um arquivo que contém os grupos ou os grupos como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="5b1e9-135">-ID</span><span class="sxs-lookup"><span data-stu-id="5b1e9-135">-Id</span></span>
<span data-ttu-id="5b1e9-136">A ID da definição da política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="5b1e9-137">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="5b1e9-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="5b1e9-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1e9-138">-ManagementGroupName</span></span>
<span data-ttu-id="5b1e9-139">O nome do grupo de gerenciamento da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="5b1e9-140">-Metadados</span><span class="sxs-lookup"><span data-stu-id="5b1e9-140">-Metadata</span></span>
<span data-ttu-id="5b1e9-141">Os metadados da definição do conjunto de políticas atualizado.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="5b1e9-142">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="5b1e9-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b1e9-143">-Name</span></span>
<span data-ttu-id="5b1e9-144">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-144">The policy set definition name.</span></span>

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

### <span data-ttu-id="5b1e9-145">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b1e9-145">-Parameter</span></span>
<span data-ttu-id="5b1e9-146">A declaração Parameters da definição de conjunto de políticas atualizada.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="5b1e9-147">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="5b1e9-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1e9-148">-PolicyDefinition</span></span>
<span data-ttu-id="5b1e9-149">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-149">The policy definitions.</span></span> <span data-ttu-id="5b1e9-150">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou as definições da política como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="5b1e9-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="5b1e9-151">-Pre</span></span>
<span data-ttu-id="5b1e9-152">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5b1e9-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b1e9-153">-SubscriptionId</span></span>
<span data-ttu-id="5b1e9-154">A ID da assinatura da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="5b1e9-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b1e9-155">-Confirm</span></span>
<span data-ttu-id="5b1e9-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1e9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1e9-157">-WhatIf</span></span>
<span data-ttu-id="5b1e9-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b1e9-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1e9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1e9-160">CommonParameters</span></span>
<span data-ttu-id="5b1e9-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1e9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1e9-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b1e9-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1e9-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b1e9-163">INPUTS</span></span>

### <span data-ttu-id="5b1e9-164">System. String</span><span class="sxs-lookup"><span data-stu-id="5b1e9-164">System.String</span></span>

### <span data-ttu-id="5b1e9-165">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b1e9-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5b1e9-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b1e9-166">OUTPUTS</span></span>

### <span data-ttu-id="5b1e9-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5b1e9-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5b1e9-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b1e9-168">NOTES</span></span>

## <span data-ttu-id="5b1e9-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b1e9-169">RELATED LINKS</span></span>
