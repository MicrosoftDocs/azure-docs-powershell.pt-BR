---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 4e9c99f2985be335f2750e500ee0c01394195c39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610198"
---
# <span data-ttu-id="7fca7-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7fca7-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="7fca7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fca7-102">SYNOPSIS</span></span>
<span data-ttu-id="7fca7-103">Retorna informações de conectividade para uma VM de origem especificada e um destino.</span><span class="sxs-lookup"><span data-stu-id="7fca7-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fca7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fca7-104">SYNTAX</span></span>

### <span data-ttu-id="7fca7-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fca7-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fca7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7fca7-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fca7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fca7-107">DESCRIPTION</span></span>
<span data-ttu-id="7fca7-108">O cmdlet Test-AzureRmNetworkWatcherConnectivity retorna informações de conectividade para uma VM de origem especificada e um destino.</span><span class="sxs-lookup"><span data-stu-id="7fca7-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="7fca7-109">Se não for possível estabelecer conectividade entre a origem e o destino, o cmdlet retornará detalhes sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="7fca7-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="7fca7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fca7-110">EXAMPLES</span></span>

### <span data-ttu-id="7fca7-111">---------------Exemplo 1: testar a conectividade do Inspetor de rede de uma VM para um site---------------</span><span class="sxs-lookup"><span data-stu-id="7fca7-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
<span data-ttu-id="7fca7-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7fca7-112">@{paragraph=PS C:\\\>}</span></span>










```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="7fca7-113">Neste exemplo, testamos a conectividade de uma VM no Azure para www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="7fca7-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="7fca7-114">OS</span><span class="sxs-lookup"><span data-stu-id="7fca7-114">PARAMETERS</span></span>

### <span data-ttu-id="7fca7-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7fca7-115">-DestinationAddress</span></span>
<span data-ttu-id="7fca7-116">O endereço IP ou URI o recurso para o qual uma tentativa de conexão será feita.</span><span class="sxs-lookup"><span data-stu-id="7fca7-116">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="7fca7-117">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="7fca7-117">-DestinationId</span></span>
<span data-ttu-id="7fca7-118">A ID do recurso para o qual uma tentativa de conexão será feita.</span><span class="sxs-lookup"><span data-stu-id="7fca7-118">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="7fca7-119">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7fca7-119">-DestinationPort</span></span>
<span data-ttu-id="7fca7-120">Porta na qual verificação de conectividade será realizada.</span><span class="sxs-lookup"><span data-stu-id="7fca7-120">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fca7-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fca7-121">-NetworkWatcher</span></span>
<span data-ttu-id="7fca7-122">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7fca7-122">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fca7-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7fca7-123">-NetworkWatcherName</span></span>
<span data-ttu-id="7fca7-124">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7fca7-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fca7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fca7-125">-ResourceGroupName</span></span>
<span data-ttu-id="7fca7-126">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="7fca7-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fca7-127">-SourceID</span><span class="sxs-lookup"><span data-stu-id="7fca7-127">-SourceId</span></span>
<span data-ttu-id="7fca7-128">A ID do recurso a partir do qual uma verificação de conectividade será iniciada.</span><span class="sxs-lookup"><span data-stu-id="7fca7-128">The ID of the resource from which a connectivity check will be initiated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fca7-129">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="7fca7-129">-SourcePort</span></span>
<span data-ttu-id="7fca7-130">A porta de origem da qual uma verificação de conectividade será realizada.</span><span class="sxs-lookup"><span data-stu-id="7fca7-130">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="7fca7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fca7-131">-DefaultProfile</span></span>
<span data-ttu-id="7fca7-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fca7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fca7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fca7-133">CommonParameters</span></span>
<span data-ttu-id="7fca7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fca7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fca7-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fca7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fca7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fca7-136">INPUTS</span></span>

### <span data-ttu-id="7fca7-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fca7-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7fca7-138">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="7fca7-138">System.String System.Int32</span></span>

## <span data-ttu-id="7fca7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fca7-139">OUTPUTS</span></span>

### <span data-ttu-id="7fca7-140">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="7fca7-140">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="7fca7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fca7-141">NOTES</span></span>
<span data-ttu-id="7fca7-142">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="7fca7-142">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="7fca7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fca7-143">RELATED LINKS</span></span>

<span data-ttu-id="7fca7-144">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="7fca7-144">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="7fca7-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="7fca7-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="7fca7-146">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Parar-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="7fca7-146">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
