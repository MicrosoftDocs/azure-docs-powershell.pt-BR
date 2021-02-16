---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117711"
---
# <span data-ttu-id="f5539-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f5539-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f5539-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5539-102">SYNOPSIS</span></span>
<span data-ttu-id="f5539-103">Cria o peering da vNet para espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5539-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="f5539-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5539-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5539-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5539-105">DESCRIPTION</span></span>
<span data-ttu-id="f5539-106">Cria o peering da vNet para espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5539-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="f5539-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5539-107">EXAMPLES</span></span>

### <span data-ttu-id="f5539-108">Exemplo 1: Criar um par de vnet para databções</span><span class="sxs-lookup"><span data-stu-id="f5539-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="f5539-109">Esse comando cria um peering de vnet para datab peerings.</span><span class="sxs-lookup"><span data-stu-id="f5539-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="f5539-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5539-110">PARAMETERS</span></span>

### <span data-ttu-id="f5539-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="f5539-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="f5539-112">Se o tráfego encaminhado das VMs na rede virtual local será permitido/não permitido na rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="f5539-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="f5539-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="f5539-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="f5539-114">Se os links do gateway puderem ser usados em rede virtual remota para vincular a essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f5539-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="f5539-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f5539-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="f5539-116">Se as VMs no espaço de rede virtual local seriam capazes de acessar as VMs no espaço de rede virtual remoto.</span><span class="sxs-lookup"><span data-stu-id="f5539-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="f5539-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5539-117">-AsJob</span></span>
<span data-ttu-id="f5539-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f5539-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f5539-119">-DatabçõesAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="f5539-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="f5539-120">Uma lista de blocos de endereços reservados para essa rede virtual na notação CIDR.</span><span class="sxs-lookup"><span data-stu-id="f5539-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="f5539-121">-DatabçõesVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f5539-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="f5539-122">A ID da rede virtual Dedados.</span><span class="sxs-lookup"><span data-stu-id="f5539-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="f5539-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5539-123">-DefaultProfile</span></span>
<span data-ttu-id="f5539-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5539-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5539-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5539-125">-Name</span></span>
<span data-ttu-id="f5539-126">O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5539-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="f5539-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f5539-127">-NoWait</span></span>
<span data-ttu-id="f5539-128">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="f5539-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f5539-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="f5539-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="f5539-130">Uma lista de blocos de endereços reservados para essa rede virtual na notação CIDR.</span><span class="sxs-lookup"><span data-stu-id="f5539-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="f5539-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f5539-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="f5539-132">A ID da rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="f5539-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="f5539-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5539-133">-ResourceGroupName</span></span>
<span data-ttu-id="f5539-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5539-134">The name of the resource group.</span></span>
<span data-ttu-id="f5539-135">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5539-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f5539-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5539-136">-SubscriptionId</span></span>
<span data-ttu-id="f5539-137">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f5539-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f5539-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="f5539-138">-UseRemoteGateway</span></span>
<span data-ttu-id="f5539-139">Se os gateways remotos puderem ser usados nesta rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f5539-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="f5539-140">Se o sinalizador estiver definido como verdadeiro e allowGatewayTransit no peering remoto também for verdadeiro, a rede virtual usará gateways de rede virtual remota para transporte público.</span><span class="sxs-lookup"><span data-stu-id="f5539-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="f5539-141">Somente um ponto pode ter esse sinalizador definido como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="f5539-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="f5539-142">Esse sinalizador não poderá ser definido se a rede virtual já tiver um gateway.</span><span class="sxs-lookup"><span data-stu-id="f5539-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="f5539-143">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="f5539-143">-WorkspaceName</span></span>
<span data-ttu-id="f5539-144">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5539-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="f5539-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f5539-145">-Confirm</span></span>
<span data-ttu-id="f5539-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5539-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5539-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5539-147">-WhatIf</span></span>
<span data-ttu-id="f5539-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f5539-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5539-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5539-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5539-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5539-150">CommonParameters</span></span>
<span data-ttu-id="f5539-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5539-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5539-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5539-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5539-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="f5539-153">INPUTS</span></span>

## <span data-ttu-id="f5539-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="f5539-154">OUTPUTS</span></span>

### <span data-ttu-id="f5539-155">Microsoft.Azure.PowerShell.Cmdlets.Datab sérvios.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f5539-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="f5539-156">Notas</span><span class="sxs-lookup"><span data-stu-id="f5539-156">NOTES</span></span>

<span data-ttu-id="f5539-157">Aliases</span><span class="sxs-lookup"><span data-stu-id="f5539-157">ALIASES</span></span>

## <span data-ttu-id="f5539-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5539-158">RELATED LINKS</span></span>

