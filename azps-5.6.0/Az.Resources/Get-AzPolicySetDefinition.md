---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 9ea6f37d21d35736116b2e9bf4fc3fcf20becf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888080"
---
# <span data-ttu-id="fc4c7-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="fc4c7-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="fc4c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4c7-103">Obtém definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="fc4c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fc4c7-104">SYNTAX</span></span>

### <span data-ttu-id="fc4c7-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fc4c7-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc4c7-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4c7-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc4c7-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4c7-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc4c7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4c7-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc4c7-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4c7-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc4c7-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4c7-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc4c7-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fc4c7-111">DESCRIPTION</span></span>
<span data-ttu-id="fc4c7-112">O cmdlet **Get-AzPolicySetDefinition** obtém uma coleção de definições de conjunto de políticas ou uma definição de conjunto de políticas específica identificada pelo nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="fc4c7-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc4c7-113">EXAMPLES</span></span>

### <span data-ttu-id="fc4c7-114">Exemplo 1: Obter todas as definições de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="fc4c7-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="fc4c7-115">Este comando obtém todas as definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="fc4c7-116">Exemplo 2: Obter definição do conjunto de políticas da assinatura atual pelo nome</span><span class="sxs-lookup"><span data-stu-id="fc4c7-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="fc4c7-117">Este comando obtém a definição de conjunto de política chamada VMPolicySetDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="fc4c7-118">Exemplo 3: Obter definição de conjunto de política a partir da assinatura por nome</span><span class="sxs-lookup"><span data-stu-id="fc4c7-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="fc4c7-119">Este comando obtém a definição de política chamada VMPolicySetDefinition da assinatura com ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="fc4c7-120">Exemplo 4: Obter todas as definições de conjunto de políticas personalizadas do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc4c7-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="fc4c7-121">Este comando obtém todas as definições de conjunto de políticas personalizadas do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="fc4c7-122">Exemplo 5: Obter definições de conjunto de políticas de uma determinada categoria</span><span class="sxs-lookup"><span data-stu-id="fc4c7-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="fc4c7-123">Este comando obtém todas as definições de conjunto de políticas na categoria "Máquina Virtual".</span><span class="sxs-lookup"><span data-stu-id="fc4c7-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="fc4c7-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fc4c7-124">PARAMETERS</span></span>

### <span data-ttu-id="fc4c7-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc4c7-125">-ApiVersion</span></span>
<span data-ttu-id="fc4c7-126">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc4c7-127">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fc4c7-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="fc4c7-128">-Builtin</span></span>
<span data-ttu-id="fc4c7-129">Limita a lista de resultados apenas definições internas de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc4c7-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="fc4c7-130">-Custom</span></span>
<span data-ttu-id="fc4c7-131">Limita a lista de resultados apenas às definições de conjunto de políticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc4c7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4c7-132">-DefaultProfile</span></span>
<span data-ttu-id="fc4c7-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fc4c7-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc4c7-134">-Id</span><span class="sxs-lookup"><span data-stu-id="fc4c7-134">-Id</span></span>
<span data-ttu-id="fc4c7-135">A ID de definição de conjunto de políticas totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="fc4c7-136">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fc4c7-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="fc4c7-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4c7-137">-ManagementGroupName</span></span>
<span data-ttu-id="fc4c7-138">O nome do grupo de gerenciamento das definições do conjunto de políticas a ser definido.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4c7-139">-Name</span><span class="sxs-lookup"><span data-stu-id="fc4c7-139">-Name</span></span>
<span data-ttu-id="fc4c7-140">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4c7-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc4c7-141">-Pre</span></span>
<span data-ttu-id="fc4c7-142">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fc4c7-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc4c7-143">-SubscriptionId</span></span>
<span data-ttu-id="fc4c7-144">A ID da assinatura das definições(es) de conjunto de políticas a obter.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4c7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4c7-145">CommonParameters</span></span>
<span data-ttu-id="fc4c7-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4c7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4c7-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc4c7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4c7-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc4c7-148">INPUTS</span></span>

### <span data-ttu-id="fc4c7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fc4c7-149">System.String</span></span>

### <span data-ttu-id="fc4c7-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fc4c7-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fc4c7-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fc4c7-151">OUTPUTS</span></span>

### <span data-ttu-id="fc4c7-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="fc4c7-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fc4c7-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="fc4c7-153">NOTES</span></span>

## <span data-ttu-id="fc4c7-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc4c7-154">RELATED LINKS</span></span>
