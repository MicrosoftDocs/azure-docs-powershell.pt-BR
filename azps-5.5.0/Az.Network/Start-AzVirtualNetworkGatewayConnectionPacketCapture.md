---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115047"
---
# <span data-ttu-id="a85ba-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a85ba-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="a85ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a85ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a85ba-103">Inicia a Operação de Captura de Pacotes em uma Conexão virtual de Gateway de Rede.</span><span class="sxs-lookup"><span data-stu-id="a85ba-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="a85ba-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a85ba-104">SYNTAX</span></span>

### <span data-ttu-id="a85ba-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="a85ba-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a85ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a85ba-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a85ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a85ba-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85ba-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a85ba-108">DESCRIPTION</span></span>
<span data-ttu-id="a85ba-109">Inicia a Operação de Captura de Pacotes em uma Conexão virtual de Gateway de Rede.</span><span class="sxs-lookup"><span data-stu-id="a85ba-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="a85ba-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a85ba-110">EXAMPLES</span></span>

### <span data-ttu-id="a85ba-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a85ba-111">Example 1</span></span>
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
### <span data-ttu-id="a85ba-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a85ba-112">Example 2</span></span>
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
### <span data-ttu-id="a85ba-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a85ba-113">Example 3</span></span>
<span data-ttu-id="a85ba-114">Exemplo de Captura de Pacote para capturar todos os pacotes internos e externos</span><span class="sxs-lookup"><span data-stu-id="a85ba-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="a85ba-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a85ba-115">PARAMETERS</span></span>

### <span data-ttu-id="a85ba-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a85ba-116">-AsJob</span></span>
<span data-ttu-id="a85ba-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a85ba-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a85ba-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a85ba-118">-Confirm</span></span>
<span data-ttu-id="a85ba-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a85ba-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85ba-120">-DefaultProfile</span></span>
<span data-ttu-id="a85ba-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a85ba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85ba-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="a85ba-122">-FilterData</span></span>
<span data-ttu-id="a85ba-123">Opções de filtro para iniciar a captura de pacotes na conexão virtual do gateway de rede.</span><span class="sxs-lookup"><span data-stu-id="a85ba-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="a85ba-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a85ba-124">-InputObject</span></span>
<span data-ttu-id="a85ba-125">O objeto de conexão do gateway de rede virtual onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="a85ba-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="a85ba-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a85ba-126">-Name</span></span>
<span data-ttu-id="a85ba-127">O nome da conexão do gateway de rede virtual onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="a85ba-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="a85ba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85ba-128">-ResourceGroupName</span></span>
<span data-ttu-id="a85ba-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a85ba-129">The resource group name.</span></span>

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

### <span data-ttu-id="a85ba-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a85ba-130">-ResourceId</span></span>
<span data-ttu-id="a85ba-131">A ID de recurso do Azure da VirtualNetworkGatewayConnection onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="a85ba-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="a85ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85ba-132">-WhatIf</span></span>
<span data-ttu-id="a85ba-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a85ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85ba-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a85ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85ba-135">CommonParameters</span></span>
<span data-ttu-id="a85ba-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85ba-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a85ba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85ba-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a85ba-138">INPUTS</span></span>

### <span data-ttu-id="a85ba-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a85ba-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="a85ba-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a85ba-140">System.String</span></span>

## <span data-ttu-id="a85ba-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="a85ba-141">OUTPUTS</span></span>

### <span data-ttu-id="a85ba-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a85ba-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a85ba-143">Notas</span><span class="sxs-lookup"><span data-stu-id="a85ba-143">NOTES</span></span>

## <span data-ttu-id="a85ba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a85ba-144">RELATED LINKS</span></span>
[<span data-ttu-id="a85ba-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a85ba-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)