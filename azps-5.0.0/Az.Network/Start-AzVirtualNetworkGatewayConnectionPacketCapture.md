---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284235"
---
# <span data-ttu-id="4feb6-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4feb6-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="4feb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4feb6-102">SYNOPSIS</span></span>
<span data-ttu-id="4feb6-103">Inicia a operação de captura de pacote em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4feb6-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="4feb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4feb6-104">SYNTAX</span></span>

### <span data-ttu-id="4feb6-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4feb6-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4feb6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4feb6-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4feb6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4feb6-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4feb6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4feb6-108">DESCRIPTION</span></span>
<span data-ttu-id="4feb6-109">Inicia a operação de captura de pacote em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4feb6-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="4feb6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4feb6-110">EXAMPLES</span></span>

### <span data-ttu-id="4feb6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4feb6-111">Example 1</span></span>
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
### <span data-ttu-id="4feb6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4feb6-112">Example 2</span></span>
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
### <span data-ttu-id="4feb6-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4feb6-113">Example 3</span></span>
<span data-ttu-id="4feb6-114">Exemplo de captura de pacote para capturar todos os pacotes internos e externos</span><span class="sxs-lookup"><span data-stu-id="4feb6-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="4feb6-115">OS</span><span class="sxs-lookup"><span data-stu-id="4feb6-115">PARAMETERS</span></span>

### <span data-ttu-id="4feb6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4feb6-116">-AsJob</span></span>
<span data-ttu-id="4feb6-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4feb6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4feb6-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4feb6-118">-Confirm</span></span>
<span data-ttu-id="4feb6-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4feb6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4feb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4feb6-120">-DefaultProfile</span></span>
<span data-ttu-id="4feb6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4feb6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4feb6-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="4feb6-122">-FilterData</span></span>
<span data-ttu-id="4feb6-123">Opções de filtro para iniciar captura de pacote na conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4feb6-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="4feb6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4feb6-124">-InputObject</span></span>
<span data-ttu-id="4feb6-125">O objeto de conexão de gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="4feb6-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="4feb6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4feb6-126">-Name</span></span>
<span data-ttu-id="4feb6-127">O nome da conexão de gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="4feb6-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="4feb6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4feb6-128">-ResourceGroupName</span></span>
<span data-ttu-id="4feb6-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4feb6-129">The resource group name.</span></span>

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

### <span data-ttu-id="4feb6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4feb6-130">-ResourceId</span></span>
<span data-ttu-id="4feb6-131">A ID de recurso do Azure do VirtualNetworkGatewayConnection em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="4feb6-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="4feb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4feb6-132">-WhatIf</span></span>
<span data-ttu-id="4feb6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4feb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4feb6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4feb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4feb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4feb6-135">CommonParameters</span></span>
<span data-ttu-id="4feb6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4feb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4feb6-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4feb6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4feb6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4feb6-138">INPUTS</span></span>

### <span data-ttu-id="4feb6-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4feb6-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="4feb6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4feb6-140">System.String</span></span>

## <span data-ttu-id="4feb6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4feb6-141">OUTPUTS</span></span>

### <span data-ttu-id="4feb6-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="4feb6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="4feb6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4feb6-143">NOTES</span></span>

## <span data-ttu-id="4feb6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4feb6-144">RELATED LINKS</span></span>
[<span data-ttu-id="4feb6-145">Parar-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4feb6-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)