---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112722"
---
# <span data-ttu-id="75341-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="75341-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="75341-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75341-102">SYNOPSIS</span></span>
<span data-ttu-id="75341-103">Atualiza um Painel existente.</span><span class="sxs-lookup"><span data-stu-id="75341-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="75341-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75341-104">SYNTAX</span></span>

### <span data-ttu-id="75341-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75341-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75341-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75341-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75341-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="75341-107">DESCRIPTION</span></span>
<span data-ttu-id="75341-108">Atualiza um Painel existente.</span><span class="sxs-lookup"><span data-stu-id="75341-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="75341-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75341-109">EXAMPLES</span></span>

### <span data-ttu-id="75341-110">Exemplo 1: Atualizar as Marcas de um Painel</span><span class="sxs-lookup"><span data-stu-id="75341-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="75341-111">Atualize as marcas em um painel.</span><span class="sxs-lookup"><span data-stu-id="75341-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="75341-112">As marcas são representadas como uma hashtable em linha.</span><span class="sxs-lookup"><span data-stu-id="75341-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="75341-113">Exemplo 2: Atualizar marcas do Painel usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="75341-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="75341-114">Atualize as Marcas em um Painel reprometido usando Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="75341-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="75341-115">Isso pode ser usado para atualizar as marcas em um único painel ou em vários dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="75341-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="75341-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75341-116">PARAMETERS</span></span>

### <span data-ttu-id="75341-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75341-117">-DefaultProfile</span></span>
<span data-ttu-id="75341-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75341-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75341-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75341-119">-InputObject</span></span>
<span data-ttu-id="75341-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="75341-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="75341-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="75341-121">-Lens</span></span>
<span data-ttu-id="75341-122">As lentes do painel.</span><span class="sxs-lookup"><span data-stu-id="75341-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="75341-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="75341-123">-Metadata</span></span>
<span data-ttu-id="75341-124">Os metadados do painel.</span><span class="sxs-lookup"><span data-stu-id="75341-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="75341-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="75341-125">-Name</span></span>
<span data-ttu-id="75341-126">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="75341-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="75341-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75341-127">-ResourceGroupName</span></span>
<span data-ttu-id="75341-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75341-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="75341-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75341-129">-SubscriptionId</span></span>
<span data-ttu-id="75341-130">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="75341-130">The Azure subscription ID.</span></span>
<span data-ttu-id="75341-131">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="75341-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="75341-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="75341-132">-Tag</span></span>
<span data-ttu-id="75341-133">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="75341-133">Resource tags</span></span>

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

### <span data-ttu-id="75341-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="75341-134">-Confirm</span></span>
<span data-ttu-id="75341-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75341-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75341-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75341-136">-WhatIf</span></span>
<span data-ttu-id="75341-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="75341-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75341-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75341-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75341-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75341-139">CommonParameters</span></span>
<span data-ttu-id="75341-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75341-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75341-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75341-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75341-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="75341-142">INPUTS</span></span>

### <span data-ttu-id="75341-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="75341-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="75341-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="75341-144">OUTPUTS</span></span>

### <span data-ttu-id="75341-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="75341-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="75341-146">Notas</span><span class="sxs-lookup"><span data-stu-id="75341-146">NOTES</span></span>

<span data-ttu-id="75341-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="75341-147">ALIASES</span></span>

<span data-ttu-id="75341-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="75341-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75341-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="75341-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75341-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75341-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75341-151">INPUTOBJECT: <IPortalIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="75341-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75341-152">`[DashboardName <String>]`: o nome do painel.</span><span class="sxs-lookup"><span data-stu-id="75341-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="75341-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="75341-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75341-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75341-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="75341-155">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="75341-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="75341-156">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="75341-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="75341-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75341-157">RELATED LINKS</span></span>

