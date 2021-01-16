---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271654"
---
# <span data-ttu-id="c4546-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="c4546-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="c4546-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4546-102">SYNOPSIS</span></span>
<span data-ttu-id="c4546-103">Atualiza um painel existente.</span><span class="sxs-lookup"><span data-stu-id="c4546-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="c4546-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4546-104">SYNTAX</span></span>

### <span data-ttu-id="c4546-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4546-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4546-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c4546-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4546-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4546-107">DESCRIPTION</span></span>
<span data-ttu-id="c4546-108">Atualiza um painel existente.</span><span class="sxs-lookup"><span data-stu-id="c4546-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="c4546-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4546-109">EXAMPLES</span></span>

### <span data-ttu-id="c4546-110">Exemplo 1: atualizar as marcas de um painel</span><span class="sxs-lookup"><span data-stu-id="c4546-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="c4546-111">Atualize as marcas em um painel.</span><span class="sxs-lookup"><span data-stu-id="c4546-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="c4546-112">As marcas são representadas como uma Hashtable embutido.</span><span class="sxs-lookup"><span data-stu-id="c4546-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="c4546-113">Exemplo 2: atualizar marcas de painel usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c4546-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="c4546-114">Atualize as marcas em um painel repetido usando Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="c4546-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="c4546-115">Isso pode ser usado para atualizar as marcas em um único painel ou em vários dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="c4546-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="c4546-116">OS</span><span class="sxs-lookup"><span data-stu-id="c4546-116">PARAMETERS</span></span>

### <span data-ttu-id="c4546-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4546-117">-DefaultProfile</span></span>
<span data-ttu-id="c4546-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4546-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4546-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4546-119">-InputObject</span></span>
<span data-ttu-id="c4546-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c4546-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4546-121">-Lente</span><span class="sxs-lookup"><span data-stu-id="c4546-121">-Lens</span></span>
<span data-ttu-id="c4546-122">As lentes do painel.</span><span class="sxs-lookup"><span data-stu-id="c4546-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="c4546-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="c4546-123">-Metadata</span></span>
<span data-ttu-id="c4546-124">Os metadados do painel.</span><span class="sxs-lookup"><span data-stu-id="c4546-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="c4546-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4546-125">-Name</span></span>
<span data-ttu-id="c4546-126">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="c4546-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="c4546-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4546-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4546-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4546-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4546-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4546-129">-SubscriptionId</span></span>
<span data-ttu-id="c4546-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4546-130">The Azure subscription ID.</span></span>
<span data-ttu-id="c4546-131">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c4546-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c4546-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="c4546-132">-Tag</span></span>
<span data-ttu-id="c4546-133">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="c4546-133">Resource tags</span></span>

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

### <span data-ttu-id="c4546-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4546-134">-Confirm</span></span>
<span data-ttu-id="c4546-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4546-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4546-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4546-136">-WhatIf</span></span>
<span data-ttu-id="c4546-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4546-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4546-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4546-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4546-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4546-139">CommonParameters</span></span>
<span data-ttu-id="c4546-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4546-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4546-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4546-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4546-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4546-142">INPUTS</span></span>

### <span data-ttu-id="c4546-143">Microsoft. Azure. PowerShell. cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="c4546-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="c4546-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4546-144">OUTPUTS</span></span>

### <span data-ttu-id="c4546-145">Microsoft. Azure. PowerShell. cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="c4546-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="c4546-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4546-146">NOTES</span></span>

<span data-ttu-id="c4546-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c4546-147">ALIASES</span></span>

<span data-ttu-id="c4546-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c4546-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4546-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c4546-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4546-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4546-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4546-151">INPUTobject <IPortalIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c4546-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4546-152">`[DashboardName <String>]`: O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="c4546-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="c4546-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c4546-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4546-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4546-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c4546-155">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4546-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c4546-156">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c4546-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c4546-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4546-157">RELATED LINKS</span></span>

