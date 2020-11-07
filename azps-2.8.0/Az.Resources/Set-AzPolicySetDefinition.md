---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773299"
---
# <span data-ttu-id="a0cf4-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a0cf4-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="a0cf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cf4-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="a0cf4-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="a0cf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0cf4-104">SYNTAX</span></span>

### <span data-ttu-id="a0cf4-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0cf4-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0cf4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0cf4-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0cf4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0cf4-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0cf4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0cf4-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0cf4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0cf4-109">DESCRIPTION</span></span>
<span data-ttu-id="a0cf4-110">O cmdlet **set-AzPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="a0cf4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0cf4-111">EXAMPLES</span></span>

### <span data-ttu-id="a0cf4-112">Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="a0cf4-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="a0cf4-113">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="a0cf4-114">O comando armazena esse objeto na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="a0cf4-115">O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="a0cf4-116">Exemplo 2: atualizar os metadados de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="a0cf4-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="a0cf4-117">Esse comando atualiza os metadados de uma definição de conjunto de políticas chamado VMPolicySetDefinition para indicar que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="a0cf4-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="a0cf4-118">OS</span><span class="sxs-lookup"><span data-stu-id="a0cf4-118">PARAMETERS</span></span>

### <span data-ttu-id="a0cf4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a0cf4-119">-ApiVersion</span></span>
<span data-ttu-id="a0cf4-120">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a0cf4-121">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a0cf4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cf4-122">-DefaultProfile</span></span>
<span data-ttu-id="a0cf4-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a0cf4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0cf4-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a0cf4-124">-Description</span></span>
<span data-ttu-id="a0cf4-125">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="a0cf4-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0cf4-126">-DisplayName</span></span>
<span data-ttu-id="a0cf4-127">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="a0cf4-128">-ID</span><span class="sxs-lookup"><span data-stu-id="a0cf4-128">-Id</span></span>
<span data-ttu-id="a0cf4-129">A ID da definição da política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="a0cf4-130">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a0cf4-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a0cf4-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cf4-131">-ManagementGroupName</span></span>
<span data-ttu-id="a0cf4-132">O nome do grupo de gerenciamento da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="a0cf4-133">-Metadados</span><span class="sxs-lookup"><span data-stu-id="a0cf4-133">-Metadata</span></span>
<span data-ttu-id="a0cf4-134">Os metadados da definição do conjunto de políticas atualizado.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="a0cf4-135">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="a0cf4-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0cf4-136">-Name</span></span>
<span data-ttu-id="a0cf4-137">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-137">The policy set definition name.</span></span>

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

### <span data-ttu-id="a0cf4-138">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0cf4-138">-Parameter</span></span>
<span data-ttu-id="a0cf4-139">A declaração Parameters da definição de conjunto de políticas atualizada.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="a0cf4-140">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="a0cf4-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0cf4-141">-PolicyDefinition</span></span>
<span data-ttu-id="a0cf4-142">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-142">The policy definitions.</span></span> <span data-ttu-id="a0cf4-143">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou as definições da política como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="a0cf4-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="a0cf4-144">-Pre</span></span>
<span data-ttu-id="a0cf4-145">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a0cf4-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0cf4-146">-SubscriptionId</span></span>
<span data-ttu-id="a0cf4-147">A ID da assinatura da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="a0cf4-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0cf4-148">-Confirm</span></span>
<span data-ttu-id="a0cf4-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cf4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cf4-150">-WhatIf</span></span>
<span data-ttu-id="a0cf4-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0cf4-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cf4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cf4-153">CommonParameters</span></span>
<span data-ttu-id="a0cf4-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0cf4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cf4-155">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0cf4-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cf4-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0cf4-156">INPUTS</span></span>

### <span data-ttu-id="a0cf4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a0cf4-157">System.String</span></span>

### <span data-ttu-id="a0cf4-158">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a0cf4-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a0cf4-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0cf4-159">OUTPUTS</span></span>

### <span data-ttu-id="a0cf4-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a0cf4-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a0cf4-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0cf4-161">NOTES</span></span>

## <span data-ttu-id="a0cf4-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0cf4-162">RELATED LINKS</span></span>
