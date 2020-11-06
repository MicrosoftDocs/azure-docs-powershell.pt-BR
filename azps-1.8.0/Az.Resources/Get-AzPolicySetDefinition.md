---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 3bfc546c39e46c4b3e7a5a504107c873c2e96888
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599429"
---
# <span data-ttu-id="08ccd-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="08ccd-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="08ccd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="08ccd-103">Obtém definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="08ccd-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="08ccd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08ccd-104">SYNTAX</span></span>

### <span data-ttu-id="08ccd-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="08ccd-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ccd-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ccd-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ccd-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ccd-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ccd-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ccd-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08ccd-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ccd-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08ccd-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ccd-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08ccd-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08ccd-111">DESCRIPTION</span></span>
<span data-ttu-id="08ccd-112">O cmdlet **Get-AzPolicySetDefinition** Obtém uma coleção de definições de conjuntos de políticas ou uma definição específica de conjunto de políticas identificadas por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="08ccd-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="08ccd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08ccd-113">EXAMPLES</span></span>

### <span data-ttu-id="08ccd-114">Exemplo 1: obter todas as definições de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="08ccd-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="08ccd-115">Esse comando obtém todas as definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="08ccd-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="08ccd-116">Exemplo 2: obter definição de política definida da assinatura atual por nome</span><span class="sxs-lookup"><span data-stu-id="08ccd-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="08ccd-117">Esse comando obtém a definição do conjunto de políticas chamado VMPolicySetDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="08ccd-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="08ccd-118">Exemplo 3: obter definição de política definida da assinatura por nome</span><span class="sxs-lookup"><span data-stu-id="08ccd-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="08ccd-119">Esse comando obtém a definição de política chamada VMPolicySetDefinition da assinatura com ID 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="08ccd-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="08ccd-120">Exemplo 4: obter todas as definições de conjuntos de políticas personalizadas do grupo Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="08ccd-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="08ccd-121">Esse comando obtém todas as definições de conjuntos de políticas personalizadas do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="08ccd-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="08ccd-122">OS</span><span class="sxs-lookup"><span data-stu-id="08ccd-122">PARAMETERS</span></span>

### <span data-ttu-id="08ccd-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="08ccd-123">-ApiVersion</span></span>
<span data-ttu-id="08ccd-124">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="08ccd-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="08ccd-125">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="08ccd-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="08ccd-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="08ccd-126">-Builtin</span></span>
<span data-ttu-id="08ccd-127">Limita a lista de resultados a somente definições de conjunto de políticas internas.</span><span class="sxs-lookup"><span data-stu-id="08ccd-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="08ccd-128">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="08ccd-128">-Custom</span></span>
<span data-ttu-id="08ccd-129">Limita a lista de resultados a somente definições de conjuntos de políticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="08ccd-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="08ccd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ccd-130">-DefaultProfile</span></span>
<span data-ttu-id="08ccd-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="08ccd-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08ccd-132">-ID</span><span class="sxs-lookup"><span data-stu-id="08ccd-132">-Id</span></span>
<span data-ttu-id="08ccd-133">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="08ccd-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="08ccd-134">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="08ccd-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="08ccd-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="08ccd-135">-ManagementGroupName</span></span>
<span data-ttu-id="08ccd-136">O nome do grupo de gerenciamento da (s) definição (ões) do conjunto de políticas a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="08ccd-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="08ccd-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="08ccd-137">-Name</span></span>
<span data-ttu-id="08ccd-138">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="08ccd-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="08ccd-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="08ccd-139">-Pre</span></span>
<span data-ttu-id="08ccd-140">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="08ccd-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="08ccd-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08ccd-141">-SubscriptionId</span></span>
<span data-ttu-id="08ccd-142">A ID da assinatura da (s) definição (ões) do conjunto de políticas a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="08ccd-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="08ccd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ccd-143">CommonParameters</span></span>
<span data-ttu-id="08ccd-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ccd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ccd-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ccd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ccd-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08ccd-146">INPUTS</span></span>

### <span data-ttu-id="08ccd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="08ccd-147">System.String</span></span>

### <span data-ttu-id="08ccd-148">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08ccd-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="08ccd-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08ccd-149">OUTPUTS</span></span>

### <span data-ttu-id="08ccd-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="08ccd-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="08ccd-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08ccd-151">NOTES</span></span>

## <span data-ttu-id="08ccd-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08ccd-152">RELATED LINKS</span></span>
