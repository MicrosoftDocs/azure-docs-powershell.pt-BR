---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 9a57b38f77d299a69cbb1f38b006d616b9c9b825
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889057"
---
# <span data-ttu-id="1a86c-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a86c-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="1a86c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a86c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a86c-103">Crie ou atualize uma política de acesso no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="1a86c-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="1a86c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1a86c-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a86c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1a86c-105">DESCRIPTION</span></span>
<span data-ttu-id="1a86c-106">Crie ou atualize uma política de acesso no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="1a86c-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="1a86c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a86c-107">EXAMPLES</span></span>

### <span data-ttu-id="1a86c-108">Exemplo 1: Criar uma política de acesso para um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="1a86c-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="1a86c-109">Este comando cria uma política de acesso para um ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="1a86c-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="1a86c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1a86c-110">PARAMETERS</span></span>

### <span data-ttu-id="1a86c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a86c-111">-DefaultProfile</span></span>
<span data-ttu-id="1a86c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a86c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a86c-113">-Description</span><span class="sxs-lookup"><span data-stu-id="1a86c-113">-Description</span></span>
<span data-ttu-id="1a86c-114">Uma descrição da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="1a86c-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="1a86c-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1a86c-115">-EnvironmentName</span></span>
<span data-ttu-id="1a86c-116">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="1a86c-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a86c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1a86c-117">-Name</span></span>
<span data-ttu-id="1a86c-118">Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="1a86c-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a86c-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="1a86c-119">-PrincipalObjectId</span></span>
<span data-ttu-id="1a86c-120">O objectId da entidade principal no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a86c-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="1a86c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a86c-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a86c-122">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a86c-122">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a86c-123">-Role</span><span class="sxs-lookup"><span data-stu-id="1a86c-123">-Role</span></span>
<span data-ttu-id="1a86c-124">A lista de funções atribuídas à entidade no ambiente.</span><span class="sxs-lookup"><span data-stu-id="1a86c-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a86c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a86c-125">-SubscriptionId</span></span>
<span data-ttu-id="1a86c-126">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a86c-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a86c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a86c-127">-Confirm</span></span>
<span data-ttu-id="1a86c-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a86c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a86c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a86c-129">-WhatIf</span></span>
<span data-ttu-id="1a86c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a86c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a86c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a86c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a86c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a86c-132">CommonParameters</span></span>
<span data-ttu-id="1a86c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a86c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a86c-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a86c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a86c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a86c-135">INPUTS</span></span>

## <span data-ttu-id="1a86c-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1a86c-136">OUTPUTS</span></span>

### <span data-ttu-id="1a86c-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="1a86c-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="1a86c-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="1a86c-138">NOTES</span></span>

<span data-ttu-id="1a86c-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1a86c-139">ALIASES</span></span>

## <span data-ttu-id="1a86c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a86c-140">RELATED LINKS</span></span>

