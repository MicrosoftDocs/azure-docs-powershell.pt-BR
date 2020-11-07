---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 39bb650333c59bd7d7185449025de7bdd6254fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772703"
---
# <span data-ttu-id="93e22-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93e22-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="93e22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93e22-102">SYNOPSIS</span></span>
<span data-ttu-id="93e22-103">Interrompe a operação de captura de pacote em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="93e22-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="93e22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93e22-104">SYNTAX</span></span>

### <span data-ttu-id="93e22-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="93e22-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e22-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="93e22-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e22-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="93e22-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e22-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93e22-108">DESCRIPTION</span></span>
<span data-ttu-id="93e22-109">Interrompe a operação de captura de pacote em um gateway de rede virtual e carregará o resultado em determinado SasUrl contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="93e22-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="93e22-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93e22-110">EXAMPLES</span></span>

### <span data-ttu-id="93e22-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93e22-111">Example 1</span></span>
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
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="93e22-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="93e22-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="93e22-113">OS</span><span class="sxs-lookup"><span data-stu-id="93e22-113">PARAMETERS</span></span>

### <span data-ttu-id="93e22-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93e22-114">-AsJob</span></span>
<span data-ttu-id="93e22-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="93e22-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93e22-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93e22-116">-Confirm</span></span>
<span data-ttu-id="93e22-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93e22-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e22-118">-DefaultProfile</span></span>
<span data-ttu-id="93e22-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93e22-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e22-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93e22-120">-InputObject</span></span>
<span data-ttu-id="93e22-121">O objeto de gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="93e22-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="93e22-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="93e22-122">-Name</span></span>
<span data-ttu-id="93e22-123">O nome do gateway de rede virtual em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="93e22-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="93e22-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e22-124">-ResourceGroupName</span></span>
<span data-ttu-id="93e22-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93e22-125">The resource group name.</span></span>

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

### <span data-ttu-id="93e22-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e22-126">-ResourceId</span></span>
<span data-ttu-id="93e22-127">A ID de recurso do Azure do VirtualNetworkGateway em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="93e22-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="93e22-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="93e22-128">-SasUrl</span></span>
<span data-ttu-id="93e22-129">Captura de pacote de URL SAS no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="93e22-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="93e22-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e22-130">-WhatIf</span></span>
<span data-ttu-id="93e22-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93e22-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e22-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93e22-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e22-133">CommonParameters</span></span>
<span data-ttu-id="93e22-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e22-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93e22-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e22-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93e22-136">INPUTS</span></span>

### <span data-ttu-id="93e22-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="93e22-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="93e22-138">System. String</span><span class="sxs-lookup"><span data-stu-id="93e22-138">System.String</span></span>

## <span data-ttu-id="93e22-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93e22-139">OUTPUTS</span></span>

### <span data-ttu-id="93e22-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="93e22-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="93e22-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93e22-141">NOTES</span></span>

## <span data-ttu-id="93e22-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93e22-142">RELATED LINKS</span></span>
[<span data-ttu-id="93e22-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93e22-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)