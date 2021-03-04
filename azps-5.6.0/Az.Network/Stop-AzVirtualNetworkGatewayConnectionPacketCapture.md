---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 9ee9277ccbadf190605d8c9e05a1637011204219
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885367"
---
# <span data-ttu-id="311a0-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="311a0-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="311a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="311a0-102">SYNOPSIS</span></span>
<span data-ttu-id="311a0-103">Interrompe a operação de captura de pacotes em uma conexão de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="311a0-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="311a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="311a0-104">SYNTAX</span></span>

### <span data-ttu-id="311a0-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="311a0-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="311a0-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311a0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="311a0-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="311a0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="311a0-108">DESCRIPTION</span></span>
<span data-ttu-id="311a0-109">Interrompe a Operação de Captura de Pacotes em uma conexão de Gateway de Rede Virtual e carregará o resultado em determinado SasUrl do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="311a0-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="311a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="311a0-110">EXAMPLES</span></span>

### <span data-ttu-id="311a0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="311a0-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="311a0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="311a0-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="311a0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="311a0-113">PARAMETERS</span></span>

### <span data-ttu-id="311a0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="311a0-114">-AsJob</span></span>
<span data-ttu-id="311a0-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="311a0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="311a0-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="311a0-116">-Confirm</span></span>
<span data-ttu-id="311a0-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="311a0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="311a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311a0-118">-DefaultProfile</span></span>
<span data-ttu-id="311a0-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="311a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311a0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="311a0-120">-InputObject</span></span>
<span data-ttu-id="311a0-121">O objeto de conexão de gateway de rede virtual no qual a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="311a0-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="311a0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="311a0-122">-Name</span></span>
<span data-ttu-id="311a0-123">O nome da conexão do gateway de rede virtual onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="311a0-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="311a0-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="311a0-125">The resource group name.</span></span>

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

### <span data-ttu-id="311a0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="311a0-126">-ResourceId</span></span>
<span data-ttu-id="311a0-127">A ID de recurso do Azure do VirtualNetworkGatewayConnection onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="311a0-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="311a0-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="311a0-128">-SasUrl</span></span>
<span data-ttu-id="311a0-129">Url do SAS para parar a captura de pacotes no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="311a0-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311a0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="311a0-130">-WhatIf</span></span>
<span data-ttu-id="311a0-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="311a0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="311a0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="311a0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="311a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311a0-133">CommonParameters</span></span>
<span data-ttu-id="311a0-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311a0-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="311a0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311a0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="311a0-136">INPUTS</span></span>

### <span data-ttu-id="311a0-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="311a0-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="311a0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="311a0-138">System.String</span></span>

## <span data-ttu-id="311a0-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="311a0-139">OUTPUTS</span></span>

### <span data-ttu-id="311a0-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="311a0-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="311a0-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="311a0-141">NOTES</span></span>

## <span data-ttu-id="311a0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="311a0-142">RELATED LINKS</span></span>
[<span data-ttu-id="311a0-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="311a0-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)