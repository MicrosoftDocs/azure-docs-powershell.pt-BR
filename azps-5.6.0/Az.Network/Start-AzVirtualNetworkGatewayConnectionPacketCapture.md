---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 2bbf5fb703a0c8a6905dff26bf62171c24fd3eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885373"
---
# <span data-ttu-id="2e698-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e698-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="2e698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e698-102">SYNOPSIS</span></span>
<span data-ttu-id="2e698-103">Inicia a operação de captura de pacotes em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2e698-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="2e698-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2e698-104">SYNTAX</span></span>

### <span data-ttu-id="2e698-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e698-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e698-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e698-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e698-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e698-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e698-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2e698-108">DESCRIPTION</span></span>
<span data-ttu-id="2e698-109">Inicia a operação de captura de pacotes em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2e698-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="2e698-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e698-110">EXAMPLES</span></span>

### <span data-ttu-id="2e698-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e698-111">Example 1</span></span>
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
### <span data-ttu-id="2e698-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2e698-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="2e698-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2e698-113">Example 3</span></span>
<span data-ttu-id="2e698-114">Exemplo de Captura de Pacotes para capturar todos os pacotes internos e externos</span><span class="sxs-lookup"><span data-stu-id="2e698-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="2e698-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2e698-115">PARAMETERS</span></span>

### <span data-ttu-id="2e698-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e698-116">-AsJob</span></span>
<span data-ttu-id="2e698-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2e698-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e698-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e698-118">-Confirm</span></span>
<span data-ttu-id="2e698-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e698-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e698-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e698-120">-DefaultProfile</span></span>
<span data-ttu-id="2e698-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e698-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e698-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="2e698-122">-FilterData</span></span>
<span data-ttu-id="2e698-123">Opções de filtro para iniciar a captura de pacotes na conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2e698-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="2e698-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e698-124">-InputObject</span></span>
<span data-ttu-id="2e698-125">O objeto de conexão de gateway de rede virtual no qual a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="2e698-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="2e698-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2e698-126">-Name</span></span>
<span data-ttu-id="2e698-127">O nome da conexão do gateway de rede virtual no qual a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="2e698-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="2e698-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e698-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e698-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e698-129">The resource group name.</span></span>

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

### <span data-ttu-id="2e698-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e698-130">-ResourceId</span></span>
<span data-ttu-id="2e698-131">A ID de recurso do Azure do VirtualNetworkGatewayConnection onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="2e698-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="2e698-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e698-132">-WhatIf</span></span>
<span data-ttu-id="2e698-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e698-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e698-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e698-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e698-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e698-135">CommonParameters</span></span>
<span data-ttu-id="2e698-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e698-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e698-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e698-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e698-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e698-138">INPUTS</span></span>

### <span data-ttu-id="2e698-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2e698-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="2e698-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2e698-140">System.String</span></span>

## <span data-ttu-id="2e698-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2e698-141">OUTPUTS</span></span>

### <span data-ttu-id="2e698-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2e698-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2e698-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="2e698-143">NOTES</span></span>

## <span data-ttu-id="2e698-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e698-144">RELATED LINKS</span></span>
[<span data-ttu-id="2e698-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e698-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)