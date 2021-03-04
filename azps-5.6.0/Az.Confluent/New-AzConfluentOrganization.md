---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893223"
---
# <span data-ttu-id="09784-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="09784-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="09784-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09784-102">SYNOPSIS</span></span>
<span data-ttu-id="09784-103">Criar recurso Organization</span><span class="sxs-lookup"><span data-stu-id="09784-103">Create Organization resource</span></span>

## <span data-ttu-id="09784-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09784-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="09784-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09784-105">DESCRIPTION</span></span>
<span data-ttu-id="09784-106">Criar recurso Organization</span><span class="sxs-lookup"><span data-stu-id="09784-106">Create Organization resource</span></span>

## <span data-ttu-id="09784-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09784-107">EXAMPLES</span></span>

### <span data-ttu-id="09784-108">Exemplo 1: Criar uma organização confluente</span><span class="sxs-lookup"><span data-stu-id="09784-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="09784-109">Este comando cria uma organização confluente.</span><span class="sxs-lookup"><span data-stu-id="09784-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="09784-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09784-110">PARAMETERS</span></span>

### <span data-ttu-id="09784-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09784-111">-AsJob</span></span>
<span data-ttu-id="09784-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="09784-112">Run the command as a job</span></span>

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

### <span data-ttu-id="09784-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09784-113">-DefaultProfile</span></span>
<span data-ttu-id="09784-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09784-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09784-115">-Location</span><span class="sxs-lookup"><span data-stu-id="09784-115">-Location</span></span>
<span data-ttu-id="09784-116">Local do recurso Organization</span><span class="sxs-lookup"><span data-stu-id="09784-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="09784-117">-Name</span><span class="sxs-lookup"><span data-stu-id="09784-117">-Name</span></span>
<span data-ttu-id="09784-118">Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="09784-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09784-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09784-119">-NoWait</span></span>
<span data-ttu-id="09784-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="09784-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="09784-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="09784-121">-OfferDetailId</span></span>
<span data-ttu-id="09784-122">Id da oferta</span><span class="sxs-lookup"><span data-stu-id="09784-122">Offer Id</span></span>

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

### <span data-ttu-id="09784-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="09784-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="09784-124">Id do Plano de Oferta</span><span class="sxs-lookup"><span data-stu-id="09784-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="09784-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="09784-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="09784-126">Nome do Plano de Oferta</span><span class="sxs-lookup"><span data-stu-id="09784-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="09784-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="09784-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="09784-128">Publisher Id</span><span class="sxs-lookup"><span data-stu-id="09784-128">Publisher Id</span></span>

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

### <span data-ttu-id="09784-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="09784-129">-OfferDetailStatus</span></span>
<span data-ttu-id="09784-130">Status da oferta saas</span><span class="sxs-lookup"><span data-stu-id="09784-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09784-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="09784-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="09784-132">Unidade De Termos de Plano de Oferta</span><span class="sxs-lookup"><span data-stu-id="09784-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="09784-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09784-133">-ResourceGroupName</span></span>
<span data-ttu-id="09784-134">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="09784-134">Resource group name</span></span>

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

### <span data-ttu-id="09784-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09784-135">-SubscriptionId</span></span>
<span data-ttu-id="09784-136">ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="09784-136">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="09784-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="09784-137">-Tag</span></span>
<span data-ttu-id="09784-138">Marcas de recurso da organização</span><span class="sxs-lookup"><span data-stu-id="09784-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09784-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="09784-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="09784-140">Endereço de email</span><span class="sxs-lookup"><span data-stu-id="09784-140">Email address</span></span>

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

### <span data-ttu-id="09784-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="09784-141">-UserDetailFirstName</span></span>
<span data-ttu-id="09784-142">Nome</span><span class="sxs-lookup"><span data-stu-id="09784-142">First name</span></span>

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

### <span data-ttu-id="09784-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="09784-143">-UserDetailLastName</span></span>
<span data-ttu-id="09784-144">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="09784-144">Last name</span></span>

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

### <span data-ttu-id="09784-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09784-145">-Confirm</span></span>
<span data-ttu-id="09784-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09784-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09784-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09784-147">-WhatIf</span></span>
<span data-ttu-id="09784-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09784-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09784-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09784-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09784-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09784-150">CommonParameters</span></span>
<span data-ttu-id="09784-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09784-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09784-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09784-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09784-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09784-153">INPUTS</span></span>

## <span data-ttu-id="09784-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09784-154">OUTPUTS</span></span>

### <span data-ttu-id="09784-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="09784-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="09784-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="09784-156">NOTES</span></span>

<span data-ttu-id="09784-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="09784-157">ALIASES</span></span>

## <span data-ttu-id="09784-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09784-158">RELATED LINKS</span></span>

