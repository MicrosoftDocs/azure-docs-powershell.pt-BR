---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116039"
---
# <span data-ttu-id="6eedb-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6eedb-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="6eedb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eedb-102">SYNOPSIS</span></span>
<span data-ttu-id="6eedb-103">Criar ou atualizar uma política de acesso no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="6eedb-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="6eedb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eedb-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6eedb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6eedb-105">DESCRIPTION</span></span>
<span data-ttu-id="6eedb-106">Criar ou atualizar uma política de acesso no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="6eedb-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="6eedb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6eedb-107">EXAMPLES</span></span>

### <span data-ttu-id="6eedb-108">Exemplo 1: Criar uma política de acesso para um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="6eedb-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="6eedb-109">Esse comando cria uma política de acesso para um ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="6eedb-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="6eedb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eedb-110">PARAMETERS</span></span>

### <span data-ttu-id="6eedb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eedb-111">-DefaultProfile</span></span>
<span data-ttu-id="6eedb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6eedb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eedb-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6eedb-113">-Description</span></span>
<span data-ttu-id="6eedb-114">Uma descrição da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="6eedb-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="6eedb-115">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="6eedb-115">-EnvironmentName</span></span>
<span data-ttu-id="6eedb-116">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6eedb-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6eedb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eedb-117">-Name</span></span>
<span data-ttu-id="6eedb-118">Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="6eedb-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="6eedb-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="6eedb-119">-PrincipalObjectId</span></span>
<span data-ttu-id="6eedb-120">A objectId do principal no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6eedb-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="6eedb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eedb-121">-ResourceGroupName</span></span>
<span data-ttu-id="6eedb-122">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6eedb-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6eedb-123">-Função</span><span class="sxs-lookup"><span data-stu-id="6eedb-123">-Role</span></span>
<span data-ttu-id="6eedb-124">A lista de funções que a entidade atribuiu ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="6eedb-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="6eedb-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6eedb-125">-SubscriptionId</span></span>
<span data-ttu-id="6eedb-126">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6eedb-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6eedb-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6eedb-127">-Confirm</span></span>
<span data-ttu-id="6eedb-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eedb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eedb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eedb-129">-WhatIf</span></span>
<span data-ttu-id="6eedb-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6eedb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eedb-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6eedb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eedb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eedb-132">CommonParameters</span></span>
<span data-ttu-id="6eedb-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eedb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eedb-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eedb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eedb-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="6eedb-135">INPUTS</span></span>

## <span data-ttu-id="6eedb-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="6eedb-136">OUTPUTS</span></span>

### <span data-ttu-id="6eedb-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="6eedb-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="6eedb-138">Notas</span><span class="sxs-lookup"><span data-stu-id="6eedb-138">NOTES</span></span>

<span data-ttu-id="6eedb-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="6eedb-139">ALIASES</span></span>

## <span data-ttu-id="6eedb-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eedb-140">RELATED LINKS</span></span>

