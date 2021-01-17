---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432897"
---
# <span data-ttu-id="76083-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="76083-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="76083-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76083-102">SYNOPSIS</span></span>
<span data-ttu-id="76083-103">Atualize o emparelhamento via rede para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76083-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="76083-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76083-104">SYNTAX</span></span>

### <span data-ttu-id="76083-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="76083-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76083-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76083-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76083-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76083-107">DESCRIPTION</span></span>
<span data-ttu-id="76083-108">Atualize o emparelhamento via rede para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76083-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="76083-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76083-109">EXAMPLES</span></span>

### <span data-ttu-id="76083-110">Exemplo 1: atualizar AllowForwardedTraffic de emparelhamento via rede virtual</span><span class="sxs-lookup"><span data-stu-id="76083-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="76083-111">Este comando atualiza o AllowForwardedTraffic de emparelhamento via rede virtual.</span><span class="sxs-lookup"><span data-stu-id="76083-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="76083-112">Exemplo 2: atualizar AllowForwardedTraffic de emparelhamento via rede virtual por objeto</span><span class="sxs-lookup"><span data-stu-id="76083-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="76083-113">Esse comando atualiza AllowForwardedTraffic de emparelhamento via rede virtual por objeto.</span><span class="sxs-lookup"><span data-stu-id="76083-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="76083-114">OS</span><span class="sxs-lookup"><span data-stu-id="76083-114">PARAMETERS</span></span>

### <span data-ttu-id="76083-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="76083-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="76083-116">[System. Management. Automation. SwitchParameter] se o tráfego encaminhado das VMs na rede virtual local será permitido/não permitido em uma rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="76083-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76083-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="76083-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="76083-118">[System. Management. Automation. SwitchParameter] se links de gateway podem ser usados em redes virtuais remotas para vincular a essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="76083-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76083-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="76083-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="76083-120">[System. Management. Automation. SwitchParameter] se as VMs no espaço de rede virtual local possam acessar as VMs em espaço de rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="76083-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76083-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76083-121">-AsJob</span></span>
<span data-ttu-id="76083-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="76083-122">Run the command as a job</span></span>

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

### <span data-ttu-id="76083-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76083-123">-DefaultProfile</span></span>
<span data-ttu-id="76083-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76083-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76083-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76083-125">-InputObject</span></span>
<span data-ttu-id="76083-126">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="76083-126">Identity parameter.</span></span>
<span data-ttu-id="76083-127">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="76083-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76083-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="76083-128">-Name</span></span>
<span data-ttu-id="76083-129">O nome do VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="76083-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76083-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="76083-130">-NoWait</span></span>
<span data-ttu-id="76083-131">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="76083-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76083-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76083-132">-ResourceGroupName</span></span>
<span data-ttu-id="76083-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76083-133">The name of the resource group.</span></span>
<span data-ttu-id="76083-134">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76083-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="76083-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76083-135">-SubscriptionId</span></span>
<span data-ttu-id="76083-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="76083-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="76083-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="76083-137">-UseRemoteGateway</span></span>
<span data-ttu-id="76083-138">[System. Management. Automation. SwitchParameter] se os gateways remotos puderem ser usados nesta rede virtual.</span><span class="sxs-lookup"><span data-stu-id="76083-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="76083-139">Se o sinalizador estiver definido como verdadeiro e allowGatewayTransit em emparelhamento remoto também for verdadeiro, a rede virtual usará gateways da rede virtual remota para trânsito.</span><span class="sxs-lookup"><span data-stu-id="76083-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="76083-140">Somente um emparelhamento pode ter esse sinalizador definido como true.</span><span class="sxs-lookup"><span data-stu-id="76083-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="76083-141">Este sinalizador não pode ser definido se a rede virtual já tem um gateway.</span><span class="sxs-lookup"><span data-stu-id="76083-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76083-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76083-142">-WorkspaceName</span></span>
<span data-ttu-id="76083-143">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76083-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="76083-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76083-144">-Confirm</span></span>
<span data-ttu-id="76083-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76083-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76083-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76083-146">-WhatIf</span></span>
<span data-ttu-id="76083-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76083-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76083-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76083-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76083-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76083-149">CommonParameters</span></span>
<span data-ttu-id="76083-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76083-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76083-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76083-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76083-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76083-152">INPUTS</span></span>

### <span data-ttu-id="76083-153">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="76083-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="76083-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76083-154">OUTPUTS</span></span>

### <span data-ttu-id="76083-155">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="76083-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="76083-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76083-156">NOTES</span></span>

<span data-ttu-id="76083-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="76083-157">ALIASES</span></span>

<span data-ttu-id="76083-158">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="76083-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76083-159">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="76083-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76083-160">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76083-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76083-161">INPUTobject <IDatabricksIdentity> : Parameter de identidade.</span><span class="sxs-lookup"><span data-stu-id="76083-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="76083-162">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="76083-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76083-163">`[PeeringName <String>]`: O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76083-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="76083-164">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76083-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76083-165">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76083-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="76083-166">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="76083-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76083-167">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76083-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="76083-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76083-168">RELATED LINKS</span></span>

