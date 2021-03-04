---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 97d5519d1b643a04fb1f6375030f178f9ccfbfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890086"
---
# <span data-ttu-id="b0c03-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="b0c03-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="b0c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c03-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c03-103">Atualiza um Painel existente.</span><span class="sxs-lookup"><span data-stu-id="b0c03-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="b0c03-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b0c03-104">SYNTAX</span></span>

### <span data-ttu-id="b0c03-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b0c03-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b0c03-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b0c03-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0c03-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b0c03-107">DESCRIPTION</span></span>
<span data-ttu-id="b0c03-108">Atualiza um Painel existente.</span><span class="sxs-lookup"><span data-stu-id="b0c03-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="b0c03-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0c03-109">EXAMPLES</span></span>

### <span data-ttu-id="b0c03-110">Exemplo 1: Atualizar as Marcas de um Painel</span><span class="sxs-lookup"><span data-stu-id="b0c03-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="b0c03-111">Atualize as marcas em um painel.</span><span class="sxs-lookup"><span data-stu-id="b0c03-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="b0c03-112">As marcas são representadas como uma hashtable em linha.</span><span class="sxs-lookup"><span data-stu-id="b0c03-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="b0c03-113">Exemplo 2: Atualizar marcas do Painel usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="b0c03-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="b0c03-114">Atualize as Marcas em um Painel que foi recuperada usando Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="b0c03-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="b0c03-115">Isso pode ser usado para atualizar as marcas em um único painel ou vários dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="b0c03-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="b0c03-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b0c03-116">PARAMETERS</span></span>

### <span data-ttu-id="b0c03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c03-117">-DefaultProfile</span></span>
<span data-ttu-id="b0c03-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c03-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c03-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0c03-119">-InputObject</span></span>
<span data-ttu-id="b0c03-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b0c03-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c03-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="b0c03-121">-Lens</span></span>
<span data-ttu-id="b0c03-122">As lentes do painel.</span><span class="sxs-lookup"><span data-stu-id="b0c03-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="b0c03-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="b0c03-123">-Metadata</span></span>
<span data-ttu-id="b0c03-124">Os metadados do painel.</span><span class="sxs-lookup"><span data-stu-id="b0c03-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="b0c03-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b0c03-125">-Name</span></span>
<span data-ttu-id="b0c03-126">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="b0c03-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c03-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0c03-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0c03-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c03-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0c03-129">-SubscriptionId</span></span>
<span data-ttu-id="b0c03-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c03-130">The Azure subscription ID.</span></span>
<span data-ttu-id="b0c03-131">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="b0c03-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c03-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0c03-132">-Tag</span></span>
<span data-ttu-id="b0c03-133">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="b0c03-133">Resource tags</span></span>

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

### <span data-ttu-id="b0c03-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0c03-134">-Confirm</span></span>
<span data-ttu-id="b0c03-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0c03-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0c03-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0c03-136">-WhatIf</span></span>
<span data-ttu-id="b0c03-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0c03-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0c03-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0c03-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0c03-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c03-139">CommonParameters</span></span>
<span data-ttu-id="b0c03-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c03-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c03-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0c03-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c03-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0c03-142">INPUTS</span></span>

### <span data-ttu-id="b0c03-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="b0c03-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="b0c03-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b0c03-144">OUTPUTS</span></span>

### <span data-ttu-id="b0c03-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="b0c03-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="b0c03-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="b0c03-146">NOTES</span></span>

<span data-ttu-id="b0c03-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b0c03-147">ALIASES</span></span>

<span data-ttu-id="b0c03-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b0c03-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0c03-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b0c03-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0c03-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0c03-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0c03-151">INPUTOBJECT <IPortalIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b0c03-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0c03-152">`[DashboardName <String>]`: O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="b0c03-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="b0c03-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b0c03-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0c03-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0c03-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b0c03-155">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c03-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b0c03-156">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="b0c03-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b0c03-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0c03-157">RELATED LINKS</span></span>

