---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: 5422b416d7fc6bf16625625a991e17d65061339e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890090"
---
# <span data-ttu-id="679d2-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="679d2-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="679d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679d2-102">SYNOPSIS</span></span>
<span data-ttu-id="679d2-103">Exclui o Painel.</span><span class="sxs-lookup"><span data-stu-id="679d2-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="679d2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="679d2-104">SYNTAX</span></span>

### <span data-ttu-id="679d2-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="679d2-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="679d2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="679d2-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="679d2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="679d2-107">DESCRIPTION</span></span>
<span data-ttu-id="679d2-108">Exclui o Painel.</span><span class="sxs-lookup"><span data-stu-id="679d2-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="679d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="679d2-109">EXAMPLES</span></span>

### <span data-ttu-id="679d2-110">Exemplo 1: Remover um Painel</span><span class="sxs-lookup"><span data-stu-id="679d2-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="679d2-111">Remova um Dashbaord usando o nome do grupo de recursos e o nome do painel.</span><span class="sxs-lookup"><span data-stu-id="679d2-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="679d2-112">Exemplo 2: Remover um Painel usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="679d2-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="679d2-113">Remova o painel retornado de uma Get-AzDashboard chamada.</span><span class="sxs-lookup"><span data-stu-id="679d2-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="679d2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="679d2-114">PARAMETERS</span></span>

### <span data-ttu-id="679d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679d2-115">-DefaultProfile</span></span>
<span data-ttu-id="679d2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="679d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679d2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679d2-117">-InputObject</span></span>
<span data-ttu-id="679d2-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="679d2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="679d2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="679d2-119">-Name</span></span>
<span data-ttu-id="679d2-120">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="679d2-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679d2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="679d2-121">-PassThru</span></span>
<span data-ttu-id="679d2-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="679d2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="679d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="679d2-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="679d2-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679d2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="679d2-125">-SubscriptionId</span></span>
<span data-ttu-id="679d2-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="679d2-126">The Azure subscription ID.</span></span>
<span data-ttu-id="679d2-127">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="679d2-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679d2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="679d2-128">-Confirm</span></span>
<span data-ttu-id="679d2-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679d2-130">-WhatIf</span></span>
<span data-ttu-id="679d2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="679d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679d2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="679d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679d2-133">CommonParameters</span></span>
<span data-ttu-id="679d2-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679d2-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="679d2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679d2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="679d2-136">INPUTS</span></span>

### <span data-ttu-id="679d2-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="679d2-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="679d2-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="679d2-138">OUTPUTS</span></span>

### <span data-ttu-id="679d2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="679d2-139">System.Boolean</span></span>

## <span data-ttu-id="679d2-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="679d2-140">NOTES</span></span>

<span data-ttu-id="679d2-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="679d2-141">ALIASES</span></span>

<span data-ttu-id="679d2-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="679d2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="679d2-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="679d2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="679d2-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="679d2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="679d2-145">INPUTOBJECT <IPortalIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="679d2-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="679d2-146">`[DashboardName <String>]`: O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="679d2-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="679d2-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="679d2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="679d2-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="679d2-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="679d2-149">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="679d2-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="679d2-150">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="679d2-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="679d2-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="679d2-151">RELATED LINKS</span></span>

