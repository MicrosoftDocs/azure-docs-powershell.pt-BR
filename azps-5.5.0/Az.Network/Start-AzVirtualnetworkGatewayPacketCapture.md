---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115044"
---
# <span data-ttu-id="435cd-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="435cd-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="435cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="435cd-102">SYNOPSIS</span></span>
<span data-ttu-id="435cd-103">Inicia a Operação de Captura de Pacotes em um Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="435cd-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="435cd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="435cd-104">SYNTAX</span></span>

### <span data-ttu-id="435cd-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="435cd-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435cd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="435cd-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435cd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="435cd-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435cd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="435cd-108">DESCRIPTION</span></span>
<span data-ttu-id="435cd-109">Inicia a Operação de Captura de Pacotes em um Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="435cd-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="435cd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="435cd-110">EXAMPLES</span></span>

### <span data-ttu-id="435cd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="435cd-111">Example 1</span></span>
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
### <span data-ttu-id="435cd-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="435cd-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="435cd-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="435cd-113">Example 3</span></span>
<span data-ttu-id="435cd-114">Exemplo de Captura de Pacote para capturar todos os pacotes internos e externos</span><span class="sxs-lookup"><span data-stu-id="435cd-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="435cd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="435cd-115">PARAMETERS</span></span>

### <span data-ttu-id="435cd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="435cd-116">-AsJob</span></span>
<span data-ttu-id="435cd-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="435cd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="435cd-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="435cd-118">-Confirm</span></span>
<span data-ttu-id="435cd-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435cd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435cd-120">-DefaultProfile</span></span>
<span data-ttu-id="435cd-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="435cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="435cd-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="435cd-122">-FilterData</span></span>
<span data-ttu-id="435cd-123">Opções de filtro para iniciar a captura de pacotes no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="435cd-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="435cd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="435cd-124">-InputObject</span></span>
<span data-ttu-id="435cd-125">O objeto virtual de gateway de rede onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="435cd-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="435cd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="435cd-126">-Name</span></span>
<span data-ttu-id="435cd-127">O nome do gateway de rede virtual onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="435cd-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="435cd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435cd-128">-ResourceGroupName</span></span>
<span data-ttu-id="435cd-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="435cd-129">The resource group name.</span></span>

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

### <span data-ttu-id="435cd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="435cd-130">-ResourceId</span></span>
<span data-ttu-id="435cd-131">A ID de recurso do Azure do VirtualNetworkGateway onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="435cd-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="435cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435cd-132">-WhatIf</span></span>
<span data-ttu-id="435cd-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="435cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435cd-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="435cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435cd-135">CommonParameters</span></span>
<span data-ttu-id="435cd-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435cd-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="435cd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435cd-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="435cd-138">INPUTS</span></span>

### <span data-ttu-id="435cd-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="435cd-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="435cd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="435cd-140">System.String</span></span>

## <span data-ttu-id="435cd-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="435cd-141">OUTPUTS</span></span>

### <span data-ttu-id="435cd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="435cd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="435cd-143">Notas</span><span class="sxs-lookup"><span data-stu-id="435cd-143">NOTES</span></span>

## <span data-ttu-id="435cd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="435cd-144">RELATED LINKS</span></span>
[<span data-ttu-id="435cd-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="435cd-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)