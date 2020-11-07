---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44f7d3331d32092636c53850b0315f34b7df7808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772825"
---
# <span data-ttu-id="dcb46-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="dcb46-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="dcb46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcb46-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb46-103">Obtém correções de política.</span><span class="sxs-lookup"><span data-stu-id="dcb46-103">Gets policy remediations.</span></span>

## <span data-ttu-id="dcb46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcb46-104">SYNTAX</span></span>

### <span data-ttu-id="dcb46-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcb46-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcb46-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dcb46-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcb46-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="dcb46-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcb46-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="dcb46-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcb46-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="dcb46-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcb46-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcb46-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcb46-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcb46-111">DESCRIPTION</span></span>
<span data-ttu-id="dcb46-112">O cmdlet **Get-AzPolicyRemediation** obtém todas as correções de política em um escopo ou uma correção específica.</span><span class="sxs-lookup"><span data-stu-id="dcb46-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="dcb46-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcb46-113">EXAMPLES</span></span>

### <span data-ttu-id="dcb46-114">Exemplo 1: obter todas as correções de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="dcb46-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="dcb46-115">Esse comando obtém todas as correções criadas em ou abaixo de uma assinatura chamada "minha assinatura".</span><span class="sxs-lookup"><span data-stu-id="dcb46-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="dcb46-116">Exemplo 2: obter uma correção de política específica e os detalhes de implantação</span><span class="sxs-lookup"><span data-stu-id="dcb46-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="dcb46-117">Este comando obtém a correção chamada "remediation1" do grupo de recursos "MyResource Group".</span><span class="sxs-lookup"><span data-stu-id="dcb46-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="dcb46-118">Os detalhes dos recursos que estão sendo corrigidos serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="dcb46-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="dcb46-119">Exemplo 3: obter 10 correções de política em um grupo de gerenciamento com filtros opcionais</span><span class="sxs-lookup"><span data-stu-id="dcb46-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="dcb46-120">Esse comando obtém um máximo de 10 correções de política de um grupo de gerenciamento chamado ' MG1 '.</span><span class="sxs-lookup"><span data-stu-id="dcb46-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="dcb46-121">Somente as correções de política para a atribuição de política fornecida serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="dcb46-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="dcb46-122">OS</span><span class="sxs-lookup"><span data-stu-id="dcb46-122">PARAMETERS</span></span>

### <span data-ttu-id="dcb46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb46-123">-DefaultProfile</span></span>
<span data-ttu-id="dcb46-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcb46-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcb46-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="dcb46-125">-Filter</span></span>
<span data-ttu-id="dcb46-126">Expressão de filtro usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="dcb46-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="dcb46-127">-IncludeDetail</span></span>
<span data-ttu-id="dcb46-128">Inclua detalhes das implantações criadas pela correção.</span><span class="sxs-lookup"><span data-stu-id="dcb46-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb46-129">-ManagementGroupName</span></span>
<span data-ttu-id="dcb46-130">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="dcb46-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcb46-131">-Name</span></span>
<span data-ttu-id="dcb46-132">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dcb46-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb46-133">-ResourceGroupName</span></span>
<span data-ttu-id="dcb46-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dcb46-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcb46-135">-ResourceId</span></span>
<span data-ttu-id="dcb46-136">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="dcb46-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-137">-Escopo</span><span class="sxs-lookup"><span data-stu-id="dcb46-137">-Scope</span></span>
<span data-ttu-id="dcb46-138">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="dcb46-138">Scope of the resource.</span></span> <span data-ttu-id="dcb46-139">Por exemplo, '/subscriptions/{subscriptionId}/resourceGroups/{rgName} '.</span><span class="sxs-lookup"><span data-stu-id="dcb46-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-140">-Início</span><span class="sxs-lookup"><span data-stu-id="dcb46-140">-Top</span></span>
<span data-ttu-id="dcb46-141">Número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="dcb46-141">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb46-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb46-142">CommonParameters</span></span>
<span data-ttu-id="dcb46-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcb46-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb46-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb46-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb46-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcb46-145">INPUTS</span></span>

### <span data-ttu-id="dcb46-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dcb46-146">System.String</span></span>

## <span data-ttu-id="dcb46-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcb46-147">OUTPUTS</span></span>

### <span data-ttu-id="dcb46-148">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="dcb46-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="dcb46-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcb46-149">NOTES</span></span>

## <span data-ttu-id="dcb46-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcb46-150">RELATED LINKS</span></span>
