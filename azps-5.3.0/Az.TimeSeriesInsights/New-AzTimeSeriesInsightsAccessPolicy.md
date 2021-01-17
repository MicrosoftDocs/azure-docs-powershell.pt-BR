---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427876"
---
# <span data-ttu-id="6303f-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6303f-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="6303f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6303f-102">SYNOPSIS</span></span>
<span data-ttu-id="6303f-103">Criar ou atualizar uma política de acesso no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="6303f-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="6303f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6303f-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6303f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6303f-105">DESCRIPTION</span></span>
<span data-ttu-id="6303f-106">Criar ou atualizar uma política de acesso no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="6303f-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="6303f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6303f-107">EXAMPLES</span></span>

### <span data-ttu-id="6303f-108">Exemplo 1: criar uma política de acesso para um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="6303f-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="6303f-109">Esse comando cria uma política de acesso para um ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="6303f-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="6303f-110">OS</span><span class="sxs-lookup"><span data-stu-id="6303f-110">PARAMETERS</span></span>

### <span data-ttu-id="6303f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6303f-111">-DefaultProfile</span></span>
<span data-ttu-id="6303f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6303f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6303f-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6303f-113">-Description</span></span>
<span data-ttu-id="6303f-114">Uma descrição da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="6303f-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="6303f-115">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="6303f-115">-EnvironmentName</span></span>
<span data-ttu-id="6303f-116">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6303f-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6303f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6303f-117">-Name</span></span>
<span data-ttu-id="6303f-118">Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="6303f-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="6303f-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="6303f-119">-PrincipalObjectId</span></span>
<span data-ttu-id="6303f-120">O objectId do objeto de segurança no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6303f-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="6303f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6303f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6303f-122">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6303f-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6303f-123">-Função</span><span class="sxs-lookup"><span data-stu-id="6303f-123">-Role</span></span>
<span data-ttu-id="6303f-124">A lista de funções que o principal está atribuído no ambiente.</span><span class="sxs-lookup"><span data-stu-id="6303f-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="6303f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6303f-125">-SubscriptionId</span></span>
<span data-ttu-id="6303f-126">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6303f-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6303f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6303f-127">-Confirm</span></span>
<span data-ttu-id="6303f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6303f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6303f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6303f-129">-WhatIf</span></span>
<span data-ttu-id="6303f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6303f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6303f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6303f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6303f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6303f-132">CommonParameters</span></span>
<span data-ttu-id="6303f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6303f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6303f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6303f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6303f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6303f-135">INPUTS</span></span>

## <span data-ttu-id="6303f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6303f-136">OUTPUTS</span></span>

### <span data-ttu-id="6303f-137">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="6303f-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="6303f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6303f-138">NOTES</span></span>

<span data-ttu-id="6303f-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6303f-139">ALIASES</span></span>

## <span data-ttu-id="6303f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6303f-140">RELATED LINKS</span></span>

