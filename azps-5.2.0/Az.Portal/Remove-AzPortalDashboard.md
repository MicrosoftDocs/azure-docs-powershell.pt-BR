---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264180"
---
# <span data-ttu-id="97dec-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="97dec-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="97dec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97dec-102">SYNOPSIS</span></span>
<span data-ttu-id="97dec-103">Exclui o painel.</span><span class="sxs-lookup"><span data-stu-id="97dec-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="97dec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97dec-104">SYNTAX</span></span>

### <span data-ttu-id="97dec-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="97dec-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97dec-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97dec-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97dec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97dec-107">DESCRIPTION</span></span>
<span data-ttu-id="97dec-108">Exclui o painel.</span><span class="sxs-lookup"><span data-stu-id="97dec-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="97dec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97dec-109">EXAMPLES</span></span>

### <span data-ttu-id="97dec-110">Exemplo 1: remover um painel</span><span class="sxs-lookup"><span data-stu-id="97dec-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="97dec-111">Remover um Dashbaord usando o nome e o nome do painel do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97dec-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="97dec-112">Exemplo 2: remover um painel usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="97dec-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="97dec-113">Remova o painel retornado de uma chamada de Get-AzDashboard.</span><span class="sxs-lookup"><span data-stu-id="97dec-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="97dec-114">OS</span><span class="sxs-lookup"><span data-stu-id="97dec-114">PARAMETERS</span></span>

### <span data-ttu-id="97dec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97dec-115">-DefaultProfile</span></span>
<span data-ttu-id="97dec-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97dec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97dec-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97dec-117">-InputObject</span></span>
<span data-ttu-id="97dec-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="97dec-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97dec-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="97dec-119">-Name</span></span>
<span data-ttu-id="97dec-120">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="97dec-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="97dec-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97dec-121">-PassThru</span></span>
<span data-ttu-id="97dec-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="97dec-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97dec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97dec-123">-ResourceGroupName</span></span>
<span data-ttu-id="97dec-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97dec-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="97dec-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97dec-125">-SubscriptionId</span></span>
<span data-ttu-id="97dec-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="97dec-126">The Azure subscription ID.</span></span>
<span data-ttu-id="97dec-127">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="97dec-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="97dec-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97dec-128">-Confirm</span></span>
<span data-ttu-id="97dec-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97dec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97dec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97dec-130">-WhatIf</span></span>
<span data-ttu-id="97dec-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97dec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97dec-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97dec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97dec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97dec-133">CommonParameters</span></span>
<span data-ttu-id="97dec-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97dec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97dec-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97dec-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97dec-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97dec-136">INPUTS</span></span>

### <span data-ttu-id="97dec-137">Microsoft. Azure. PowerShell. cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="97dec-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="97dec-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97dec-138">OUTPUTS</span></span>

### <span data-ttu-id="97dec-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97dec-139">System.Boolean</span></span>

## <span data-ttu-id="97dec-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97dec-140">NOTES</span></span>

<span data-ttu-id="97dec-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97dec-141">ALIASES</span></span>

<span data-ttu-id="97dec-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="97dec-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97dec-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="97dec-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97dec-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97dec-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97dec-145">INPUTobject <IPortalIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="97dec-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97dec-146">`[DashboardName <String>]`: O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="97dec-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="97dec-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="97dec-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97dec-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97dec-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="97dec-149">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="97dec-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="97dec-150">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="97dec-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="97dec-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97dec-151">RELATED LINKS</span></span>

