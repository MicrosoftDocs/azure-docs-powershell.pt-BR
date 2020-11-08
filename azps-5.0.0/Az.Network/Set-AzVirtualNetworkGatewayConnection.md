---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118087"
---
# <span data-ttu-id="7bb6a-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7bb6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb6a-103">Configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="7bb6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bb6a-104">SYNTAX</span></span>

### <span data-ttu-id="7bb6a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="7bb6a-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb6a-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7bb6a-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb6a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bb6a-107">DESCRIPTION</span></span>
<span data-ttu-id="7bb6a-108">O cmdlet **set-AzVirtualNetworkGatewayConnection** configura uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="7bb6a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bb6a-109">EXAMPLES</span></span>

### <span data-ttu-id="7bb6a-110">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="7bb6a-110">Example 1:</span></span>
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

### <span data-ttu-id="7bb6a-111">Exemplo 2: Adicionar/atualizar marcas para um VirtualNetworkGatewayConnection existente</span><span class="sxs-lookup"><span data-stu-id="7bb6a-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="7bb6a-112">OS</span><span class="sxs-lookup"><span data-stu-id="7bb6a-112">PARAMETERS</span></span>

### <span data-ttu-id="7bb6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bb6a-113">-AsJob</span></span>
<span data-ttu-id="7bb6a-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7bb6a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bb6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb6a-115">-DefaultProfile</span></span>
<span data-ttu-id="7bb6a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb6a-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7bb6a-117">-EnableBgp</span></span>
<span data-ttu-id="7bb6a-118">Se você deve usar uma sessão BGP em um túnel VPN S2S</span><span class="sxs-lookup"><span data-stu-id="7bb6a-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="7bb6a-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="7bb6a-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="7bb6a-120">Tempo limite de detecção de par inativo da conexão em segundos</span><span class="sxs-lookup"><span data-stu-id="7bb6a-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="7bb6a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7bb6a-121">-Force</span></span>
<span data-ttu-id="7bb6a-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7bb6a-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="7bb6a-123">-IpsecPolicies</span></span>
<span data-ttu-id="7bb6a-124">Uma lista de diretivas IPSec.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="7bb6a-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="7bb6a-125">-Tag</span></span>
<span data-ttu-id="7bb6a-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7bb6a-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7bb6a-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="7bb6a-128">Uma lista de políticas do seletor de tráfego.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-128">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="7bb6a-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="7bb6a-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="7bb6a-130">Se o PrivateIP deve ser usado para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="7bb6a-130">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="7bb6a-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7bb6a-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7bb6a-132">Se os seletores de tráfego baseados em políticas devem ser usados para uma conexão S2S</span><span class="sxs-lookup"><span data-stu-id="7bb6a-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="7bb6a-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="7bb6a-134">Especifica o objeto PSVirtualNetworkGatewayConnection que este cmdlet usa para modificar a conexão do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="7bb6a-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bb6a-135">-Confirm</span></span>
<span data-ttu-id="7bb6a-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb6a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb6a-137">-WhatIf</span></span>
<span data-ttu-id="7bb6a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb6a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb6a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb6a-140">CommonParameters</span></span>
<span data-ttu-id="7bb6a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb6a-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb6a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb6a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bb6a-143">INPUTS</span></span>

### <span data-ttu-id="7bb6a-144">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="7bb6a-145">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7bb6a-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7bb6a-146">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="7bb6a-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7bb6a-147">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="7bb6a-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="7bb6a-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bb6a-148">OUTPUTS</span></span>

### <span data-ttu-id="7bb6a-149">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7bb6a-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bb6a-150">NOTES</span></span>

## <span data-ttu-id="7bb6a-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bb6a-151">RELATED LINKS</span></span>

[<span data-ttu-id="7bb6a-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7bb6a-153">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7bb6a-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7bb6a-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


