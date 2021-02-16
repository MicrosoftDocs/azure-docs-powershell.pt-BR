---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127022"
---
# <span data-ttu-id="34743-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="34743-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="34743-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34743-102">SYNOPSIS</span></span>
<span data-ttu-id="34743-103">Atualize o peering da vNet para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="34743-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="34743-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34743-104">SYNTAX</span></span>

### <span data-ttu-id="34743-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34743-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34743-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="34743-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34743-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="34743-107">DESCRIPTION</span></span>
<span data-ttu-id="34743-108">Atualize o peering da vNet para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="34743-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="34743-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34743-109">EXAMPLES</span></span>

### <span data-ttu-id="34743-110">Exemplo 1: Atualizar AllowForwardedTraffic do peering da vnet</span><span class="sxs-lookup"><span data-stu-id="34743-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="34743-111">Este comando atualiza AllowForwardedTraffic do peering da vnet.</span><span class="sxs-lookup"><span data-stu-id="34743-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="34743-112">Exemplo 2: Atualizar AllowForwardedTraffic de peering de vnet por objeto</span><span class="sxs-lookup"><span data-stu-id="34743-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="34743-113">Este comando atualiza AllowForwardedTraffic do peering de vnet por objeto.</span><span class="sxs-lookup"><span data-stu-id="34743-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="34743-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34743-114">PARAMETERS</span></span>

### <span data-ttu-id="34743-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="34743-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="34743-116">[System.Management.Automation.SwitchParameter] Se o tráfego encaminhado das VMs na rede virtual local será permitido/não permitido na rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="34743-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="34743-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="34743-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="34743-118">[System.Management.Automation.SwitchParameter] Se os links de gateway puderem ser usados em rede virtual remota para vincular a essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="34743-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="34743-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="34743-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="34743-120">[System.Management.Automation.SwitchParameter] Se os VMs no espaço de rede virtual local seriam capazes de acessar as VMs em espaço de rede virtual remoto.</span><span class="sxs-lookup"><span data-stu-id="34743-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="34743-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34743-121">-AsJob</span></span>
<span data-ttu-id="34743-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="34743-122">Run the command as a job</span></span>

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

### <span data-ttu-id="34743-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34743-123">-DefaultProfile</span></span>
<span data-ttu-id="34743-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34743-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34743-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34743-125">-InputObject</span></span>
<span data-ttu-id="34743-126">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="34743-126">Identity parameter.</span></span>
<span data-ttu-id="34743-127">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="34743-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34743-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="34743-128">-Name</span></span>
<span data-ttu-id="34743-129">O nome da VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="34743-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="34743-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="34743-130">-NoWait</span></span>
<span data-ttu-id="34743-131">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="34743-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="34743-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34743-132">-ResourceGroupName</span></span>
<span data-ttu-id="34743-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34743-133">The name of the resource group.</span></span>
<span data-ttu-id="34743-134">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="34743-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34743-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34743-135">-SubscriptionId</span></span>
<span data-ttu-id="34743-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="34743-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34743-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="34743-137">-UseRemoteGateway</span></span>
<span data-ttu-id="34743-138">[System.Management.Automation.SwitchParameter] Se gateways remotos puderem ser usados nesta rede virtual.</span><span class="sxs-lookup"><span data-stu-id="34743-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="34743-139">Se o sinalizador estiver definido como verdadeiro e allowGatewayTransit no peering remoto também for verdadeiro, a rede virtual usará gateways de rede virtual remota para transporte público.</span><span class="sxs-lookup"><span data-stu-id="34743-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="34743-140">Somente um ponto pode ter esse sinalizador definido como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="34743-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="34743-141">Esse sinalizador não poderá ser definido se a rede virtual já tiver um gateway.</span><span class="sxs-lookup"><span data-stu-id="34743-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="34743-142">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="34743-142">-WorkspaceName</span></span>
<span data-ttu-id="34743-143">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="34743-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="34743-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="34743-144">-Confirm</span></span>
<span data-ttu-id="34743-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34743-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34743-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34743-146">-WhatIf</span></span>
<span data-ttu-id="34743-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="34743-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34743-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34743-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34743-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34743-149">CommonParameters</span></span>
<span data-ttu-id="34743-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34743-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34743-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34743-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34743-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="34743-152">INPUTS</span></span>

### <span data-ttu-id="34743-153">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.IDatabtabçõesIdentity</span><span class="sxs-lookup"><span data-stu-id="34743-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="34743-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="34743-154">OUTPUTS</span></span>

### <span data-ttu-id="34743-155">Microsoft.Azure.PowerShell.Cmdlets.Datab sérvios.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34743-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="34743-156">Notas</span><span class="sxs-lookup"><span data-stu-id="34743-156">NOTES</span></span>

<span data-ttu-id="34743-157">Aliases</span><span class="sxs-lookup"><span data-stu-id="34743-157">ALIASES</span></span>

<span data-ttu-id="34743-158">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="34743-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34743-159">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="34743-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34743-160">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34743-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34743-161">INPUTOBJECT: <IDatabricksIdentity> Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="34743-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="34743-162">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="34743-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34743-163">`[PeeringName <String>]`: o nome do pario vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="34743-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="34743-164">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34743-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34743-165">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="34743-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="34743-166">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="34743-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34743-167">`[WorkspaceName <String>]`: o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="34743-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="34743-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34743-168">RELATED LINKS</span></span>

