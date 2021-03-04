---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: ec7307b6bd6d01b7b3f6e2656026eea78e0d3704
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885370"
---
# <span data-ttu-id="d395a-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d395a-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="d395a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d395a-102">SYNOPSIS</span></span>
<span data-ttu-id="d395a-103">Inicia a Operação de Captura de Pacotes em um Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="d395a-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="d395a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d395a-104">SYNTAX</span></span>

### <span data-ttu-id="d395a-105">ByVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d395a-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d395a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d395a-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d395a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d395a-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d395a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d395a-108">DESCRIPTION</span></span>
<span data-ttu-id="d395a-109">Inicia a Operação de Captura de Pacotes em um Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="d395a-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="d395a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d395a-110">EXAMPLES</span></span>

### <span data-ttu-id="d395a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d395a-111">Example 1</span></span>
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

### <span data-ttu-id="d395a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d395a-112">Example 2</span></span>
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

## <span data-ttu-id="d395a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d395a-113">PARAMETERS</span></span>

### <span data-ttu-id="d395a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d395a-114">-AsJob</span></span>
<span data-ttu-id="d395a-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d395a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d395a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d395a-116">-DefaultProfile</span></span>
<span data-ttu-id="d395a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d395a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d395a-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="d395a-118">-FilterData</span></span>
<span data-ttu-id="d395a-119">Opções de filtro para iniciar a captura de pacotes no Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="d395a-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="d395a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d395a-120">-InputObject</span></span>
<span data-ttu-id="d395a-121">O objeto Gateway vpn no qual a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="d395a-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d395a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d395a-122">-Name</span></span>
<span data-ttu-id="d395a-123">O nome do Gateway Vpn onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="d395a-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="d395a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d395a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d395a-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d395a-125">The resource group name.</span></span>

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

### <span data-ttu-id="d395a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d395a-126">-ResourceId</span></span>
<span data-ttu-id="d395a-127">A ID de recurso do Azure do VpnGateway onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="d395a-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="d395a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d395a-128">-Confirm</span></span>
<span data-ttu-id="d395a-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d395a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d395a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d395a-130">-WhatIf</span></span>
<span data-ttu-id="d395a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d395a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d395a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d395a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d395a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d395a-133">CommonParameters</span></span>
<span data-ttu-id="d395a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d395a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d395a-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d395a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d395a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d395a-136">INPUTS</span></span>

### <span data-ttu-id="d395a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d395a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d395a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d395a-138">System.String</span></span>

## <span data-ttu-id="d395a-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d395a-139">OUTPUTS</span></span>

### <span data-ttu-id="d395a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d395a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d395a-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="d395a-141">NOTES</span></span>

## <span data-ttu-id="d395a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d395a-142">RELATED LINKS</span></span>

[<span data-ttu-id="d395a-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d395a-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)