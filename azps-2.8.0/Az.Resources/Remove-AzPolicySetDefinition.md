---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 5141b4b0c7639580fbb8037193f91ac41464e233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773312"
---
# <span data-ttu-id="1ea99-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1ea99-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1ea99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ea99-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea99-103">Remove uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="1ea99-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="1ea99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ea99-104">SYNTAX</span></span>

### <span data-ttu-id="1ea99-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ea99-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea99-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ea99-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea99-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ea99-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea99-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ea99-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea99-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ea99-109">DESCRIPTION</span></span>
<span data-ttu-id="1ea99-110">O cmdlet **Remove-AzPolicySetDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="1ea99-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="1ea99-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ea99-111">EXAMPLES</span></span>

### <span data-ttu-id="1ea99-112">Exemplo 1: remover definição do conjunto de políticas por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="1ea99-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="1ea99-113">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1ea99-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="1ea99-114">O comando o armazena na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1ea99-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="1ea99-115">O segundo comando Remove a definição do conjunto de políticas identificado pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1ea99-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="1ea99-116">OS</span><span class="sxs-lookup"><span data-stu-id="1ea99-116">PARAMETERS</span></span>

### <span data-ttu-id="1ea99-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1ea99-117">-ApiVersion</span></span>
<span data-ttu-id="1ea99-118">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1ea99-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1ea99-119">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="1ea99-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1ea99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea99-120">-DefaultProfile</span></span>
<span data-ttu-id="1ea99-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1ea99-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ea99-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1ea99-122">-Force</span></span>
<span data-ttu-id="1ea99-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1ea99-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1ea99-124">-ID</span><span class="sxs-lookup"><span data-stu-id="1ea99-124">-Id</span></span>
<span data-ttu-id="1ea99-125">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="1ea99-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="1ea99-126">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1ea99-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="1ea99-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea99-127">-ManagementGroupName</span></span>
<span data-ttu-id="1ea99-128">O nome do grupo de gerenciamento da definição de conjunto de políticas a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="1ea99-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="1ea99-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ea99-129">-Name</span></span>
<span data-ttu-id="1ea99-130">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="1ea99-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="1ea99-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="1ea99-131">-Pre</span></span>
<span data-ttu-id="1ea99-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1ea99-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1ea99-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ea99-133">-SubscriptionId</span></span>
<span data-ttu-id="1ea99-134">A ID da assinatura da definição do conjunto de políticas a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="1ea99-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="1ea99-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ea99-135">-Confirm</span></span>
<span data-ttu-id="1ea99-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea99-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ea99-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea99-137">-WhatIf</span></span>
<span data-ttu-id="1ea99-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ea99-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ea99-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ea99-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ea99-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea99-140">CommonParameters</span></span>
<span data-ttu-id="1ea99-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea99-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea99-142">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ea99-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea99-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ea99-143">INPUTS</span></span>

### <span data-ttu-id="1ea99-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1ea99-144">System.String</span></span>

### <span data-ttu-id="1ea99-145">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1ea99-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1ea99-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ea99-146">OUTPUTS</span></span>

### <span data-ttu-id="1ea99-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ea99-147">System.Boolean</span></span>

## <span data-ttu-id="1ea99-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ea99-148">NOTES</span></span>

## <span data-ttu-id="1ea99-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ea99-149">RELATED LINKS</span></span>