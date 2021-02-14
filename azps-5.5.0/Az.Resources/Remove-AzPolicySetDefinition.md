---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117176"
---
# <span data-ttu-id="3e007-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3e007-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="3e007-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e007-102">SYNOPSIS</span></span>
<span data-ttu-id="3e007-103">Remove uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="3e007-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="3e007-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e007-104">SYNTAX</span></span>

### <span data-ttu-id="3e007-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e007-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e007-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e007-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e007-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e007-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e007-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e007-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e007-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e007-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e007-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e007-110">DESCRIPTION</span></span>
<span data-ttu-id="3e007-111">O cmdlet **Remove-AzPolicySetDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="3e007-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="3e007-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e007-112">EXAMPLES</span></span>

### <span data-ttu-id="3e007-113">Exemplo 1: Remover definição de conjunto de políticas por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="3e007-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="3e007-114">O primeiro comando obtém uma definição de conjunto de políticas usando Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e007-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="3e007-115">O comando o armazena na variável $PolicySetDefinition dados.</span><span class="sxs-lookup"><span data-stu-id="3e007-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="3e007-116">O segundo comando remove a definição de conjunto de políticas identificada pela propriedade **ResourceId** da $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="3e007-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="3e007-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e007-117">PARAMETERS</span></span>

### <span data-ttu-id="3e007-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3e007-118">-ApiVersion</span></span>
<span data-ttu-id="3e007-119">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3e007-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3e007-120">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="3e007-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3e007-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e007-121">-DefaultProfile</span></span>
<span data-ttu-id="3e007-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3e007-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e007-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3e007-123">-Force</span></span>
<span data-ttu-id="3e007-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e007-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e007-125">-ID</span><span class="sxs-lookup"><span data-stu-id="3e007-125">-Id</span></span>
<span data-ttu-id="3e007-126">A ID de definição de conjunto de políticas totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e007-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="3e007-127">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3e007-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="3e007-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e007-128">-InputObject</span></span>
<span data-ttu-id="3e007-129">O objeto de definição de conjunto de políticas para remover a saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e007-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="3e007-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3e007-130">-ManagementGroupName</span></span>
<span data-ttu-id="3e007-131">O nome do grupo de gerenciamento da definição de conjunto de políticas a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3e007-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="3e007-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e007-132">-Name</span></span>
<span data-ttu-id="3e007-133">O nome de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="3e007-133">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e007-134">-Pré-</span><span class="sxs-lookup"><span data-stu-id="3e007-134">-Pre</span></span>
<span data-ttu-id="3e007-135">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3e007-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3e007-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e007-136">-SubscriptionId</span></span>
<span data-ttu-id="3e007-137">A ID da assinatura da definição de conjunto de políticas a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3e007-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="3e007-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e007-138">-Confirm</span></span>
<span data-ttu-id="3e007-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e007-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e007-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e007-140">-WhatIf</span></span>
<span data-ttu-id="3e007-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e007-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e007-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e007-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e007-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e007-143">CommonParameters</span></span>
<span data-ttu-id="3e007-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e007-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e007-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e007-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e007-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e007-146">INPUTS</span></span>

### <span data-ttu-id="3e007-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3e007-147">System.String</span></span>

### <span data-ttu-id="3e007-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3e007-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3e007-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e007-149">OUTPUTS</span></span>

### <span data-ttu-id="3e007-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e007-150">System.Boolean</span></span>

## <span data-ttu-id="3e007-151">Notas</span><span class="sxs-lookup"><span data-stu-id="3e007-151">NOTES</span></span>

## <span data-ttu-id="3e007-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e007-152">RELATED LINKS</span></span>
