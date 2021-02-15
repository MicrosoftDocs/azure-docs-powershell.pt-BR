---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 4fee7f0fc4a22cc5d69196badf4e0ff2cad288d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114620"
---
# <span data-ttu-id="c5bb2-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c5bb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bb2-103">Configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="c5bb2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5bb2-104">SYNTAX</span></span>

### <span data-ttu-id="c5bb2-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c5bb2-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5bb2-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="c5bb2-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5bb2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5bb2-107">DESCRIPTION</span></span>
<span data-ttu-id="c5bb2-108">O cmdlet **Set-AzVirtualNetworkGatewayConnection** configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="c5bb2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="c5bb2-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="c5bb2-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="c5bb2-111">Exemplo 2: Adicionar/Atualizar marcas a uma VirtualNetworkGatewayConnection existente</span><span class="sxs-lookup"><span data-stu-id="c5bb2-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="c5bb2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5bb2-112">PARAMETERS</span></span>

### <span data-ttu-id="c5bb2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5bb2-113">-AsJob</span></span>
<span data-ttu-id="c5bb2-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c5bb2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5bb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bb2-115">-DefaultProfile</span></span>
<span data-ttu-id="c5bb2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c5bb2-117">-EnableBgp</span></span>
<span data-ttu-id="c5bb2-118">Se você quer usar uma sessão BGP em um túnel S2S VPN</span><span class="sxs-lookup"><span data-stu-id="c5bb2-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c5bb2-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="c5bb2-120">Tempo de Tempo De detecção de ponto morto da conexão em segundos</span><span class="sxs-lookup"><span data-stu-id="c5bb2-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-121">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="c5bb2-121">-ConnectionMode</span></span>
<span data-ttu-id="c5bb2-122">Modo de Conexão do Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="c5bb2-122">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c5bb2-123">-Force</span></span>
<span data-ttu-id="c5bb2-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5bb2-125">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="c5bb2-125">-IpsecPolicies</span></span>
<span data-ttu-id="c5bb2-126">Uma lista de políticas IPSec.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-126">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5bb2-127">-Tag</span></span>
<span data-ttu-id="c5bb2-128">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-129">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="c5bb2-129">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="c5bb2-130">Uma lista de políticas do Seletor de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-130">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="c5bb2-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="c5bb2-132">Se você quer usar o PrivateIP para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="c5bb2-132">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="c5bb2-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="c5bb2-134">Se você quer usar seletores de tráfego baseados em política para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="c5bb2-134">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-135">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-135">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="c5bb2-136">Especifica o objeto PSVirtualNetworkGatewayConnection que esse cmdlet usa para modificar a conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-136">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c5bb2-137">-Confirm</span></span>
<span data-ttu-id="c5bb2-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5bb2-139">-WhatIf</span></span>
<span data-ttu-id="c5bb2-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5bb2-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bb2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bb2-142">CommonParameters</span></span>
<span data-ttu-id="c5bb2-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bb2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bb2-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bb2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bb2-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="c5bb2-145">INPUTS</span></span>

### <span data-ttu-id="c5bb2-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="c5bb2-147">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c5bb2-147">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c5bb2-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="c5bb2-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="c5bb2-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="c5bb2-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="c5bb2-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="c5bb2-150">OUTPUTS</span></span>

### <span data-ttu-id="c5bb2-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c5bb2-152">Notas</span><span class="sxs-lookup"><span data-stu-id="c5bb2-152">NOTES</span></span>

## <span data-ttu-id="c5bb2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5bb2-153">RELATED LINKS</span></span>

[<span data-ttu-id="c5bb2-154">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-154">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c5bb2-155">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-155">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c5bb2-156">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c5bb2-156">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


