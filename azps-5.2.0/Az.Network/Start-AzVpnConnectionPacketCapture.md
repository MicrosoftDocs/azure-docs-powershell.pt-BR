---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263345"
---
# <span data-ttu-id="e714b-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e714b-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="e714b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e714b-102">SYNOPSIS</span></span>
<span data-ttu-id="e714b-103">Inicia a operação de captura de pacote em uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="e714b-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="e714b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e714b-104">SYNTAX</span></span>

### <span data-ttu-id="e714b-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e714b-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e714b-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e714b-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e714b-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e714b-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e714b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e714b-108">DESCRIPTION</span></span>
<span data-ttu-id="e714b-109">Inicia a operação de captura de pacote em uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="e714b-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="e714b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e714b-110">EXAMPLES</span></span>

### <span data-ttu-id="e714b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e714b-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="e714b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e714b-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="e714b-113">OS</span><span class="sxs-lookup"><span data-stu-id="e714b-113">PARAMETERS</span></span>

### <span data-ttu-id="e714b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e714b-114">-AsJob</span></span>
<span data-ttu-id="e714b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e714b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e714b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e714b-116">-DefaultProfile</span></span>
<span data-ttu-id="e714b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e714b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e714b-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="e714b-118">-FilterData</span></span>
<span data-ttu-id="e714b-119">Opções de filtro para iniciar a captura de pacotes em conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="e714b-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="e714b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e714b-120">-InputObject</span></span>
<span data-ttu-id="e714b-121">O objeto de conexão VPN em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="e714b-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e714b-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="e714b-122">-LinkConnectionName</span></span>
<span data-ttu-id="e714b-123">Os nomes da SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="e714b-123">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e714b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e714b-124">-Name</span></span>
<span data-ttu-id="e714b-125">O nome da conexão VPN na qual a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="e714b-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e714b-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e714b-126">-ParentResourceName</span></span>
<span data-ttu-id="e714b-127">O nome do Vpngateway pai.</span><span class="sxs-lookup"><span data-stu-id="e714b-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e714b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e714b-128">-ResourceGroupName</span></span>
<span data-ttu-id="e714b-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e714b-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e714b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e714b-130">-ResourceId</span></span>
<span data-ttu-id="e714b-131">A ID de recurso do Azure do VpnConnection em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="e714b-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e714b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e714b-132">-Confirm</span></span>
<span data-ttu-id="e714b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e714b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e714b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e714b-134">-WhatIf</span></span>
<span data-ttu-id="e714b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e714b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e714b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e714b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e714b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e714b-137">CommonParameters</span></span>
<span data-ttu-id="e714b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e714b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e714b-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e714b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e714b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e714b-140">INPUTS</span></span>

### <span data-ttu-id="e714b-141">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e714b-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="e714b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e714b-142">System.String</span></span>

## <span data-ttu-id="e714b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e714b-143">OUTPUTS</span></span>

### <span data-ttu-id="e714b-144">Microsoft. Azure. Commands. Network. Models. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e714b-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="e714b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e714b-145">NOTES</span></span>

## <span data-ttu-id="e714b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e714b-146">RELATED LINKS</span></span>

[<span data-ttu-id="e714b-147">Parar-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e714b-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)