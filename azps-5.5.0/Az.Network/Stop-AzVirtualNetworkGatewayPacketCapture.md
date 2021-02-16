---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118247"
---
# <span data-ttu-id="4b587-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b587-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="4b587-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b587-102">SYNOPSIS</span></span>
<span data-ttu-id="4b587-103">Interrompe a Operação de Captura de Pacotes em um Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4b587-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="4b587-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b587-104">SYNTAX</span></span>

### <span data-ttu-id="4b587-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="4b587-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b587-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b587-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b587-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b587-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b587-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b587-108">DESCRIPTION</span></span>
<span data-ttu-id="4b587-109">Interrompe a Operação de Captura de Pacotes em um Gateway de Rede Virtual e carregará o resultado em determinado SasUrl de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4b587-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="4b587-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b587-110">EXAMPLES</span></span>

### <span data-ttu-id="4b587-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b587-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

### <span data-ttu-id="4b587-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4b587-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

## <span data-ttu-id="4b587-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b587-113">PARAMETERS</span></span>

### <span data-ttu-id="4b587-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b587-114">-AsJob</span></span>
<span data-ttu-id="4b587-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4b587-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b587-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b587-116">-Confirm</span></span>
<span data-ttu-id="4b587-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b587-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b587-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b587-118">-DefaultProfile</span></span>
<span data-ttu-id="4b587-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b587-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b587-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b587-120">-InputObject</span></span>
<span data-ttu-id="4b587-121">O objeto virtual de gateway de rede onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="4b587-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="4b587-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b587-122">-Name</span></span>
<span data-ttu-id="4b587-123">O nome do gateway de rede virtual onde a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="4b587-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="4b587-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b587-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b587-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b587-125">The resource group name.</span></span>

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

### <span data-ttu-id="4b587-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b587-126">-ResourceId</span></span>
<span data-ttu-id="4b587-127">A ID de recurso do Azure do VirtualNetworkGateway onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="4b587-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="4b587-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="4b587-128">-SasUrl</span></span>
<span data-ttu-id="4b587-129">Captura de pacote de URL do SAS no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4b587-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="4b587-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b587-130">-WhatIf</span></span>
<span data-ttu-id="4b587-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b587-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b587-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b587-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b587-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b587-133">CommonParameters</span></span>
<span data-ttu-id="4b587-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b587-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b587-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b587-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b587-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b587-136">INPUTS</span></span>

### <span data-ttu-id="4b587-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4b587-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4b587-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4b587-138">System.String</span></span>

## <span data-ttu-id="4b587-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b587-139">OUTPUTS</span></span>

### <span data-ttu-id="4b587-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="4b587-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="4b587-141">Notas</span><span class="sxs-lookup"><span data-stu-id="4b587-141">NOTES</span></span>

## <span data-ttu-id="4b587-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b587-142">RELATED LINKS</span></span>
[<span data-ttu-id="4b587-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b587-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
