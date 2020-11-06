---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d0a1097407c9941b5be49b19ea7ba99e75b3fce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610065"
---
# <span data-ttu-id="e5f36-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e5f36-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e5f36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5f36-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f36-103">Obtém definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e5f36-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5f36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5f36-104">SYNTAX</span></span>

### <span data-ttu-id="e5f36-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5f36-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f36-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f36-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f36-108">IdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f36-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f36-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5f36-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5f36-111">DESCRIPTION</span></span>
<span data-ttu-id="e5f36-112">O cmdlet **Get-AzureRmPolicySetDefinition** Obtém uma coleção de definições de conjuntos de políticas ou uma definição específica de conjunto de políticas identificadas por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="e5f36-112">The **Get-AzureRmPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="e5f36-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5f36-113">EXAMPLES</span></span>

### <span data-ttu-id="e5f36-114">Exemplo 1: obter todas as definições de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="e5f36-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="e5f36-115">Esse comando obtém todas as definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e5f36-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="e5f36-116">Exemplo 2: obter definição de política definida da assinatura atual por nome</span><span class="sxs-lookup"><span data-stu-id="e5f36-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="e5f36-117">Esse comando obtém a definição do conjunto de políticas chamado VMPolicySetDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="e5f36-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="e5f36-118">Exemplo 3: obter definição de política definida da assinatura por nome</span><span class="sxs-lookup"><span data-stu-id="e5f36-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="e5f36-119">Esse comando obtém a definição de política chamada VMPolicySetDefinition da assinatura com ID 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="e5f36-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="e5f36-120">Exemplo 4: obter todas as definições de conjuntos de políticas personalizadas do grupo Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e5f36-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="e5f36-121">Esse comando obtém todas as definições de conjuntos de políticas personalizadas do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="e5f36-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="e5f36-122">OS</span><span class="sxs-lookup"><span data-stu-id="e5f36-122">PARAMETERS</span></span>

### <span data-ttu-id="e5f36-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5f36-123">-ApiVersion</span></span>
<span data-ttu-id="e5f36-124">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e5f36-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5f36-125">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e5f36-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e5f36-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="e5f36-126">-Builtin</span></span>
<span data-ttu-id="e5f36-127">Limita a lista de resultados a somente definições de conjunto de políticas internas.</span><span class="sxs-lookup"><span data-stu-id="e5f36-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="e5f36-128">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="e5f36-128">-Custom</span></span>
<span data-ttu-id="e5f36-129">Limita a lista de resultados a somente definições de conjuntos de políticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e5f36-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="e5f36-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f36-130">-DefaultProfile</span></span>
<span data-ttu-id="e5f36-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e5f36-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f36-132">-ID</span><span class="sxs-lookup"><span data-stu-id="e5f36-132">-Id</span></span>
<span data-ttu-id="e5f36-133">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e5f36-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="e5f36-134">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e5f36-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e5f36-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f36-135">-ManagementGroupName</span></span>
<span data-ttu-id="e5f36-136">O nome do grupo de gerenciamento da (s) definição (ões) do conjunto de políticas a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e5f36-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="e5f36-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5f36-137">-Name</span></span>
<span data-ttu-id="e5f36-138">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e5f36-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="e5f36-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5f36-139">-Pre</span></span>
<span data-ttu-id="e5f36-140">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e5f36-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e5f36-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5f36-141">-SubscriptionId</span></span>
<span data-ttu-id="e5f36-142">A ID da assinatura da (s) definição (ões) do conjunto de políticas a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e5f36-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="e5f36-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f36-143">CommonParameters</span></span>
<span data-ttu-id="e5f36-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f36-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f36-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f36-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f36-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5f36-146">INPUTS</span></span>

### <span data-ttu-id="e5f36-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e5f36-147">System.String</span></span>

### <span data-ttu-id="e5f36-148">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e5f36-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e5f36-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5f36-149">OUTPUTS</span></span>

### <span data-ttu-id="e5f36-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e5f36-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5f36-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5f36-151">NOTES</span></span>

## <span data-ttu-id="e5f36-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5f36-152">RELATED LINKS</span></span>
