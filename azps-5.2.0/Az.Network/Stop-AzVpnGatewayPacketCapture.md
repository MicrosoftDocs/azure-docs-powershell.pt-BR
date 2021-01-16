---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263112"
---
# <span data-ttu-id="fd483-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd483-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="fd483-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd483-102">SYNOPSIS</span></span>
<span data-ttu-id="fd483-103">Interrompe a operação de captura de pacote em um gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="fd483-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="fd483-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd483-104">SYNTAX</span></span>

### <span data-ttu-id="fd483-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd483-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd483-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fd483-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd483-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fd483-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd483-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd483-108">DESCRIPTION</span></span>
<span data-ttu-id="fd483-109">Interrompe a operação de captura de pacote em um gateway VPN e carregará o resultado em determinado SasUrl contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fd483-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="fd483-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd483-110">EXAMPLES</span></span>

### <span data-ttu-id="fd483-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd483-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="fd483-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fd483-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="fd483-113">OS</span><span class="sxs-lookup"><span data-stu-id="fd483-113">PARAMETERS</span></span>

### <span data-ttu-id="fd483-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd483-114">-AsJob</span></span>
<span data-ttu-id="fd483-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fd483-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd483-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd483-116">-DefaultProfile</span></span>
<span data-ttu-id="fd483-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd483-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd483-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd483-118">-InputObject</span></span>
<span data-ttu-id="fd483-119">O objeto de gateway VPN em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="fd483-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="fd483-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd483-120">-Name</span></span>
<span data-ttu-id="fd483-121">O nome do gateway VPN em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="fd483-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="fd483-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd483-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd483-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd483-123">The resource group name.</span></span>

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

### <span data-ttu-id="fd483-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd483-124">-ResourceId</span></span>
<span data-ttu-id="fd483-125">A ID de recurso do Azure do VpnGateway em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="fd483-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="fd483-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="fd483-126">-SasUrl</span></span>
<span data-ttu-id="fd483-127">Captura de pacote de URL SAS no gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="fd483-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="fd483-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd483-128">-Confirm</span></span>
<span data-ttu-id="fd483-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd483-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd483-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd483-130">-WhatIf</span></span>
<span data-ttu-id="fd483-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd483-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd483-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd483-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd483-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd483-133">CommonParameters</span></span>
<span data-ttu-id="fd483-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd483-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd483-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd483-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd483-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd483-136">INPUTS</span></span>

### <span data-ttu-id="fd483-137">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fd483-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="fd483-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fd483-138">System.String</span></span>

## <span data-ttu-id="fd483-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd483-139">OUTPUTS</span></span>

### <span data-ttu-id="fd483-140">Microsoft. Azure. Commands. Network. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="fd483-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="fd483-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd483-141">NOTES</span></span>

## <span data-ttu-id="fd483-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd483-142">RELATED LINKS</span></span>

[<span data-ttu-id="fd483-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd483-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)