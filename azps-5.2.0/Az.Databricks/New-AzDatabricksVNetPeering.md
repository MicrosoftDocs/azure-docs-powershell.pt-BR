---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263881"
---
# <span data-ttu-id="25e7b-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="25e7b-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="25e7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="25e7b-103">Cria um emparelhamento via rede virtual para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="25e7b-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="25e7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25e7b-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25e7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="25e7b-106">Cria um emparelhamento via rede virtual para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="25e7b-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="25e7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="25e7b-108">Exemplo 1: criar um emparelhamento via rede virtual para databricks</span><span class="sxs-lookup"><span data-stu-id="25e7b-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="25e7b-109">Esse comando cria um emparelhamento via rede virtual para databricks.</span><span class="sxs-lookup"><span data-stu-id="25e7b-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="25e7b-110">OS</span><span class="sxs-lookup"><span data-stu-id="25e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="25e7b-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="25e7b-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="25e7b-112">Se o tráfego encaminhado das VMs na rede virtual local será permitido/não permitido na rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="25e7b-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="25e7b-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="25e7b-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="25e7b-114">Se os links de gateway puderem ser usados em redes virtuais remotas para vincular a essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="25e7b-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="25e7b-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="25e7b-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="25e7b-116">Se as VMs no espaço de rede virtual local poderão acessar as VMs em espaço de rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="25e7b-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="25e7b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25e7b-117">-AsJob</span></span>
<span data-ttu-id="25e7b-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="25e7b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="25e7b-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="25e7b-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="25e7b-120">Uma lista de blocos de endereço reservados para esta rede virtual na notação CIDR.</span><span class="sxs-lookup"><span data-stu-id="25e7b-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e7b-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="25e7b-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="25e7b-122">A ID da rede virtual databricks.</span><span class="sxs-lookup"><span data-stu-id="25e7b-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="25e7b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e7b-123">-DefaultProfile</span></span>
<span data-ttu-id="25e7b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25e7b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e7b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="25e7b-125">-Name</span></span>
<span data-ttu-id="25e7b-126">O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="25e7b-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="25e7b-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="25e7b-127">-NoWait</span></span>
<span data-ttu-id="25e7b-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="25e7b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25e7b-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="25e7b-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="25e7b-130">Uma lista de blocos de endereço reservados para esta rede virtual na notação CIDR.</span><span class="sxs-lookup"><span data-stu-id="25e7b-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e7b-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="25e7b-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="25e7b-132">A ID da rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="25e7b-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="25e7b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e7b-133">-ResourceGroupName</span></span>
<span data-ttu-id="25e7b-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25e7b-134">The name of the resource group.</span></span>
<span data-ttu-id="25e7b-135">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="25e7b-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="25e7b-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25e7b-136">-SubscriptionId</span></span>
<span data-ttu-id="25e7b-137">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="25e7b-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="25e7b-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="25e7b-138">-UseRemoteGateway</span></span>
<span data-ttu-id="25e7b-139">Se os gateways remotos puderem ser usados nesta rede virtual.</span><span class="sxs-lookup"><span data-stu-id="25e7b-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="25e7b-140">Se o sinalizador estiver definido como verdadeiro e allowGatewayTransit em emparelhamento remoto também for verdadeiro, a rede virtual usará gateways da rede virtual remota para trânsito.</span><span class="sxs-lookup"><span data-stu-id="25e7b-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="25e7b-141">Somente um emparelhamento pode ter esse sinalizador definido como true.</span><span class="sxs-lookup"><span data-stu-id="25e7b-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="25e7b-142">Este sinalizador não pode ser definido se a rede virtual já tem um gateway.</span><span class="sxs-lookup"><span data-stu-id="25e7b-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="25e7b-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="25e7b-143">-WorkspaceName</span></span>
<span data-ttu-id="25e7b-144">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="25e7b-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="25e7b-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25e7b-145">-Confirm</span></span>
<span data-ttu-id="25e7b-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e7b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e7b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e7b-147">-WhatIf</span></span>
<span data-ttu-id="25e7b-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25e7b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e7b-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25e7b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e7b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e7b-150">CommonParameters</span></span>
<span data-ttu-id="25e7b-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e7b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e7b-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25e7b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e7b-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25e7b-153">INPUTS</span></span>

## <span data-ttu-id="25e7b-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25e7b-154">OUTPUTS</span></span>

### <span data-ttu-id="25e7b-155">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="25e7b-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="25e7b-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25e7b-156">NOTES</span></span>

<span data-ttu-id="25e7b-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="25e7b-157">ALIASES</span></span>

## <span data-ttu-id="25e7b-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25e7b-158">RELATED LINKS</span></span>

