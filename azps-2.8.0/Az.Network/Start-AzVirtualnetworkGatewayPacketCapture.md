---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 1f0b539e2f5a6e2c387738558fb6db8cbe647457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772710"
---
# <span data-ttu-id="9ed68-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ed68-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="9ed68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ed68-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed68-103">Inicia a operação de captura de pacote em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9ed68-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="9ed68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ed68-104">SYNTAX</span></span>

### <span data-ttu-id="9ed68-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ed68-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed68-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ed68-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ed68-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed68-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed68-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ed68-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed68-109">Inicia a operação de captura de pacote em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9ed68-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="9ed68-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ed68-110">EXAMPLES</span></span>

### <span data-ttu-id="9ed68-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ed68-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="9ed68-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9ed68-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="9ed68-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ed68-113">PARAMETERS</span></span>

### <span data-ttu-id="9ed68-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ed68-114">-AsJob</span></span>
<span data-ttu-id="9ed68-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9ed68-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ed68-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ed68-116">-Confirm</span></span>
<span data-ttu-id="9ed68-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ed68-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed68-118">-DefaultProfile</span></span>
<span data-ttu-id="9ed68-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed68-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed68-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="9ed68-120">-FilterData</span></span>
<span data-ttu-id="9ed68-121">Opções de filtro para iniciar captura de pacote no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9ed68-121">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="9ed68-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ed68-122">-InputObject</span></span>
<span data-ttu-id="9ed68-123">O objeto de gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9ed68-123">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed68-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ed68-124">-Name</span></span>
<span data-ttu-id="9ed68-125">O nome do gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9ed68-125">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed68-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed68-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ed68-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ed68-127">The resource group name.</span></span>

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

### <span data-ttu-id="9ed68-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed68-128">-ResourceId</span></span>
<span data-ttu-id="9ed68-129">A ID de recurso do Azure do VirtualNetworkGateway em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="9ed68-129">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="9ed68-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed68-130">-WhatIf</span></span>
<span data-ttu-id="9ed68-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ed68-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed68-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ed68-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed68-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed68-133">CommonParameters</span></span>
<span data-ttu-id="9ed68-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed68-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed68-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ed68-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed68-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ed68-136">INPUTS</span></span>

### <span data-ttu-id="9ed68-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9ed68-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9ed68-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed68-138">System.String</span></span>

## <span data-ttu-id="9ed68-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ed68-139">OUTPUTS</span></span>

### <span data-ttu-id="9ed68-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="9ed68-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="9ed68-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ed68-141">NOTES</span></span>

## <span data-ttu-id="9ed68-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ed68-142">RELATED LINKS</span></span>
[<span data-ttu-id="9ed68-143">Parar-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ed68-143">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)