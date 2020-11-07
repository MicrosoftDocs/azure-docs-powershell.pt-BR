---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945190"
---
# <span data-ttu-id="d6af8-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="d6af8-101">New-AzsPlan</span></span>

## <span data-ttu-id="d6af8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6af8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6af8-103">Crie ou atualize o plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-103">Create or update the plan.</span></span>

## <span data-ttu-id="d6af8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6af8-104">SYNTAX</span></span>

### <span data-ttu-id="d6af8-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6af8-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6af8-106">Criados</span><span class="sxs-lookup"><span data-stu-id="d6af8-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6af8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6af8-107">DESCRIPTION</span></span>
<span data-ttu-id="d6af8-108">Crie ou atualize o plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-108">Create or update the plan.</span></span>

## <span data-ttu-id="d6af8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6af8-109">EXAMPLES</span></span>

### <span data-ttu-id="d6af8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6af8-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="d6af8-111">Cria um novo plano</span><span class="sxs-lookup"><span data-stu-id="d6af8-111">Creates a new plan</span></span>

## <span data-ttu-id="d6af8-112">OS</span><span class="sxs-lookup"><span data-stu-id="d6af8-112">PARAMETERS</span></span>

### <span data-ttu-id="d6af8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6af8-113">-DefaultProfile</span></span>
<span data-ttu-id="d6af8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6af8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6af8-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d6af8-115">-Description</span></span>
<span data-ttu-id="d6af8-116">Descrição do plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6af8-117">-DisplayName</span></span>
<span data-ttu-id="d6af8-118">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="d6af8-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="d6af8-119">-ExternalReferenceId</span></span>
<span data-ttu-id="d6af8-120">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="d6af8-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-121">-Local</span><span class="sxs-lookup"><span data-stu-id="d6af8-121">-Location</span></span>
<span data-ttu-id="d6af8-122">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="d6af8-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6af8-123">-Name</span></span>
<span data-ttu-id="d6af8-124">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-124">Name of the plan.</span></span>

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

### <span data-ttu-id="d6af8-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="d6af8-125">-PlanDefinition</span></span>
<span data-ttu-id="d6af8-126">Um plano representa um pacote de cotas e recursos que são locatários oferecidos.</span><span class="sxs-lookup"><span data-stu-id="d6af8-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="d6af8-127">Um locatário pode adquirir esse plano por meio de uma oferta para atualizar o acesso aos serviços de nuvem subjacentes.</span><span class="sxs-lookup"><span data-stu-id="d6af8-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="d6af8-128">Para construir, consulte a seção notas para propriedades PLANDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d6af8-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-129">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="d6af8-129">-PropertiesName</span></span>
<span data-ttu-id="d6af8-130">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="d6af8-131">-QuotaIds</span></span>
<span data-ttu-id="d6af8-132">Identificadores de cota sob o plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6af8-133">-ResourceGroupName</span></span>
<span data-ttu-id="d6af8-134">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="d6af8-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d6af8-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="d6af8-135">-SkuIds</span></span>
<span data-ttu-id="d6af8-136">Identificadores de SKU.</span><span class="sxs-lookup"><span data-stu-id="d6af8-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="d6af8-137">-SubscriptionCount</span></span>
<span data-ttu-id="d6af8-138">Contagem de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="d6af8-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6af8-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6af8-139">-SubscriptionId</span></span>
<span data-ttu-id="d6af8-140">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d6af8-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6af8-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6af8-141">-Confirm</span></span>
<span data-ttu-id="d6af8-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6af8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6af8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6af8-143">-WhatIf</span></span>
<span data-ttu-id="d6af8-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6af8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6af8-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6af8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6af8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6af8-146">CommonParameters</span></span>
<span data-ttu-id="d6af8-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6af8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6af8-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6af8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6af8-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6af8-149">INPUTS</span></span>

### <span data-ttu-id="d6af8-150">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="d6af8-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="d6af8-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6af8-151">OUTPUTS</span></span>

### <span data-ttu-id="d6af8-152">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="d6af8-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="d6af8-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d6af8-153">ALIASES</span></span>

## <span data-ttu-id="d6af8-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6af8-154">NOTES</span></span>

<span data-ttu-id="d6af8-155">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d6af8-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6af8-156">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6af8-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d6af8-157">PLANDEFINITION <IPlan> : um plano representa um pacote de cotas e recursos que são locatários oferecidos.</span><span class="sxs-lookup"><span data-stu-id="d6af8-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="d6af8-158">Um locatário pode adquirir esse plano por meio de uma oferta para atualizar o acesso aos serviços de nuvem subjacentes.</span><span class="sxs-lookup"><span data-stu-id="d6af8-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="d6af8-159">`[Location <String>]`: Localização do recurso</span><span class="sxs-lookup"><span data-stu-id="d6af8-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="d6af8-160">`[Description <String>]`: Descrição do plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="d6af8-161">`[DisplayName <String>]`: Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="d6af8-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="d6af8-162">`[ExternalReferenceId <String>]`: Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="d6af8-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="d6af8-163">`[PropertiesName <String>]`: Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d6af8-164">`[QuotaIds <String[]>]`: Identificadores de cota sob o plano.</span><span class="sxs-lookup"><span data-stu-id="d6af8-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="d6af8-165">`[SkuIds <String[]>]`: Identificadores de SKU.</span><span class="sxs-lookup"><span data-stu-id="d6af8-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="d6af8-166">`[SubscriptionCount <Int32?>]`: Contagem de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="d6af8-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="d6af8-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6af8-167">RELATED LINKS</span></span>

