---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 3a1d9c2f415d56263529fcd66aa1ee9535823bbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772711"
---
# <span data-ttu-id="09fef-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09fef-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="09fef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09fef-102">SYNOPSIS</span></span>
<span data-ttu-id="09fef-103">Inicia a operação de captura de pacote em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="09fef-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="09fef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09fef-104">SYNTAX</span></span>

### <span data-ttu-id="09fef-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="09fef-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09fef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09fef-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09fef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09fef-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fef-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09fef-108">DESCRIPTION</span></span>
<span data-ttu-id="09fef-109">Inicia a operação de captura de pacote em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="09fef-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="09fef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09fef-110">EXAMPLES</span></span>

### <span data-ttu-id="09fef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09fef-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="09fef-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="09fef-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="09fef-113">OS</span><span class="sxs-lookup"><span data-stu-id="09fef-113">PARAMETERS</span></span>

### <span data-ttu-id="09fef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09fef-114">-AsJob</span></span>
<span data-ttu-id="09fef-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="09fef-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09fef-116">-Confirm</span></span>
<span data-ttu-id="09fef-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09fef-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fef-118">-DefaultProfile</span></span>
<span data-ttu-id="09fef-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09fef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="09fef-120">-FilterData</span></span>
<span data-ttu-id="09fef-121">Opções de filtro para iniciar captura de pacote na conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="09fef-121">Filter options for start packet capture on virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09fef-122">-InputObject</span></span>
<span data-ttu-id="09fef-123">O objeto de conexão de gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="09fef-123">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="09fef-124">-Name</span></span>
<span data-ttu-id="09fef-125">O nome da conexão de gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="09fef-125">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fef-126">-ResourceGroupName</span></span>
<span data-ttu-id="09fef-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09fef-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09fef-128">-ResourceId</span></span>
<span data-ttu-id="09fef-129">A ID de recurso do Azure do VirtualNetworkGatewayConnection em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="09fef-129">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fef-130">-WhatIf</span></span>
<span data-ttu-id="09fef-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09fef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09fef-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09fef-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fef-133">CommonParameters</span></span>
<span data-ttu-id="09fef-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fef-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09fef-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fef-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09fef-136">INPUTS</span></span>

### <span data-ttu-id="09fef-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="09fef-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="09fef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="09fef-138">System.String</span></span>

## <span data-ttu-id="09fef-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09fef-139">OUTPUTS</span></span>

### <span data-ttu-id="09fef-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="09fef-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="09fef-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09fef-141">NOTES</span></span>

## <span data-ttu-id="09fef-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09fef-142">RELATED LINKS</span></span>
[<span data-ttu-id="09fef-143">Parar-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09fef-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)