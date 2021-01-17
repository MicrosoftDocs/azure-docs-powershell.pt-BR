---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433368"
---
# <span data-ttu-id="6d101-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d101-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="6d101-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d101-102">SYNOPSIS</span></span>
<span data-ttu-id="6d101-103">Inicia a operação de captura de pacote em um gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="6d101-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="6d101-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d101-104">SYNTAX</span></span>

### <span data-ttu-id="6d101-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d101-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d101-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6d101-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d101-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6d101-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d101-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d101-108">DESCRIPTION</span></span>
<span data-ttu-id="6d101-109">Inicia a operação de captura de pacote em um gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="6d101-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="6d101-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d101-110">EXAMPLES</span></span>

### <span data-ttu-id="6d101-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d101-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="6d101-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6d101-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="6d101-113">OS</span><span class="sxs-lookup"><span data-stu-id="6d101-113">PARAMETERS</span></span>

### <span data-ttu-id="6d101-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d101-114">-AsJob</span></span>
<span data-ttu-id="6d101-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6d101-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d101-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d101-116">-DefaultProfile</span></span>
<span data-ttu-id="6d101-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d101-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d101-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="6d101-118">-FilterData</span></span>
<span data-ttu-id="6d101-119">Opções de filtro para iniciar captura de pacote no gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="6d101-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="6d101-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d101-120">-InputObject</span></span>
<span data-ttu-id="6d101-121">O objeto de gateway VPN em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6d101-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d101-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d101-122">-Name</span></span>
<span data-ttu-id="6d101-123">O nome do gateway VPN em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6d101-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d101-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d101-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d101-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d101-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d101-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d101-126">-ResourceId</span></span>
<span data-ttu-id="6d101-127">A ID de recurso do Azure do VpnGateway em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6d101-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d101-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d101-128">-Confirm</span></span>
<span data-ttu-id="6d101-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d101-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d101-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d101-130">-WhatIf</span></span>
<span data-ttu-id="6d101-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d101-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d101-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d101-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d101-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d101-133">CommonParameters</span></span>
<span data-ttu-id="6d101-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d101-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d101-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d101-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d101-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d101-136">INPUTS</span></span>

### <span data-ttu-id="6d101-137">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6d101-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="6d101-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6d101-138">System.String</span></span>

## <span data-ttu-id="6d101-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d101-139">OUTPUTS</span></span>

### <span data-ttu-id="6d101-140">Microsoft. Azure. Commands. Network. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="6d101-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="6d101-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d101-141">NOTES</span></span>

## <span data-ttu-id="6d101-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d101-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d101-143">Parar-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d101-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)