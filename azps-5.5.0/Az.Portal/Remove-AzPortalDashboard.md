---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111508"
---
# <span data-ttu-id="74d6e-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="74d6e-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="74d6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="74d6e-103">Exclui o Painel.</span><span class="sxs-lookup"><span data-stu-id="74d6e-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="74d6e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74d6e-104">SYNTAX</span></span>

### <span data-ttu-id="74d6e-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="74d6e-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74d6e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74d6e-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74d6e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="74d6e-107">DESCRIPTION</span></span>
<span data-ttu-id="74d6e-108">Exclui o Painel.</span><span class="sxs-lookup"><span data-stu-id="74d6e-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="74d6e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74d6e-109">EXAMPLES</span></span>

### <span data-ttu-id="74d6e-110">Exemplo 1: Remover um Painel</span><span class="sxs-lookup"><span data-stu-id="74d6e-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="74d6e-111">Remova um Dashbaord usando o nome do grupo de recursos e o nome do painel.</span><span class="sxs-lookup"><span data-stu-id="74d6e-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="74d6e-112">Exemplo 2: Remover um Painel usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="74d6e-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="74d6e-113">Remova o painel retornado de uma Get-AzDashboard chamada.</span><span class="sxs-lookup"><span data-stu-id="74d6e-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="74d6e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74d6e-114">PARAMETERS</span></span>

### <span data-ttu-id="74d6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d6e-115">-DefaultProfile</span></span>
<span data-ttu-id="74d6e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74d6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d6e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74d6e-117">-InputObject</span></span>
<span data-ttu-id="74d6e-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="74d6e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74d6e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="74d6e-119">-Name</span></span>
<span data-ttu-id="74d6e-120">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="74d6e-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="74d6e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d6e-121">-PassThru</span></span>
<span data-ttu-id="74d6e-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="74d6e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="74d6e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d6e-123">-ResourceGroupName</span></span>
<span data-ttu-id="74d6e-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74d6e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="74d6e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74d6e-125">-SubscriptionId</span></span>
<span data-ttu-id="74d6e-126">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="74d6e-126">The Azure subscription ID.</span></span>
<span data-ttu-id="74d6e-127">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="74d6e-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="74d6e-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="74d6e-128">-Confirm</span></span>
<span data-ttu-id="74d6e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d6e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d6e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d6e-130">-WhatIf</span></span>
<span data-ttu-id="74d6e-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="74d6e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d6e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74d6e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d6e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d6e-133">CommonParameters</span></span>
<span data-ttu-id="74d6e-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d6e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d6e-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74d6e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d6e-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="74d6e-136">INPUTS</span></span>

### <span data-ttu-id="74d6e-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="74d6e-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="74d6e-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="74d6e-138">OUTPUTS</span></span>

### <span data-ttu-id="74d6e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74d6e-139">System.Boolean</span></span>

## <span data-ttu-id="74d6e-140">Notas</span><span class="sxs-lookup"><span data-stu-id="74d6e-140">NOTES</span></span>

<span data-ttu-id="74d6e-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="74d6e-141">ALIASES</span></span>

<span data-ttu-id="74d6e-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="74d6e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74d6e-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="74d6e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74d6e-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74d6e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74d6e-145">INPUTOBJECT: <IPortalIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="74d6e-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74d6e-146">`[DashboardName <String>]`: o nome do painel.</span><span class="sxs-lookup"><span data-stu-id="74d6e-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="74d6e-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="74d6e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74d6e-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74d6e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="74d6e-149">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="74d6e-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="74d6e-150">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="74d6e-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="74d6e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74d6e-151">RELATED LINKS</span></span>

