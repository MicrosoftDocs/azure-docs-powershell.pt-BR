---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: d37bd9fa620b6da68c311399be811f639ea85aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885356"
---
# <span data-ttu-id="286ed-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="286ed-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="286ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286ed-102">SYNOPSIS</span></span>
<span data-ttu-id="286ed-103">Interrompe a operação de captura de pacotes em uma conexão Vpn</span><span class="sxs-lookup"><span data-stu-id="286ed-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="286ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="286ed-104">SYNTAX</span></span>

### <span data-ttu-id="286ed-105">ByVpnConnectionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="286ed-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286ed-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="286ed-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286ed-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="286ed-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286ed-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="286ed-108">DESCRIPTION</span></span>
<span data-ttu-id="286ed-109">Interrompe a Operação de Captura de Pacotes em uma conexão Vpn e carregará o resultado em determinado SasUrl do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="286ed-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="286ed-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="286ed-110">EXAMPLES</span></span>

### <span data-ttu-id="286ed-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="286ed-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="286ed-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="286ed-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="286ed-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="286ed-113">PARAMETERS</span></span>

### <span data-ttu-id="286ed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="286ed-114">-AsJob</span></span>
<span data-ttu-id="286ed-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="286ed-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="286ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286ed-116">-DefaultProfile</span></span>
<span data-ttu-id="286ed-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="286ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286ed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="286ed-118">-InputObject</span></span>
<span data-ttu-id="286ed-119">O objeto de conexão Vpn no qual a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="286ed-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="286ed-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="286ed-120">-LinkConnectionName</span></span>
<span data-ttu-id="286ed-121">Os nomes do SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="286ed-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="286ed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="286ed-122">-Name</span></span>
<span data-ttu-id="286ed-123">O nome da conexão vpn onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="286ed-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286ed-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="286ed-124">-ParentResourceName</span></span>
<span data-ttu-id="286ed-125">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="286ed-125">The parent resource name.</span></span>

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

### <span data-ttu-id="286ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="286ed-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="286ed-127">The resource group name.</span></span>

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

### <span data-ttu-id="286ed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="286ed-128">-ResourceId</span></span>
<span data-ttu-id="286ed-129">A ID de recurso do Azure da VpnConnection onde a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="286ed-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="286ed-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="286ed-130">-SasUrl</span></span>
<span data-ttu-id="286ed-131">Url do SAS para parar a captura de pacotes na Vpn.</span><span class="sxs-lookup"><span data-stu-id="286ed-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="286ed-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="286ed-132">-Confirm</span></span>
<span data-ttu-id="286ed-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286ed-134">-WhatIf</span></span>
<span data-ttu-id="286ed-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="286ed-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286ed-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="286ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286ed-137">CommonParameters</span></span>
<span data-ttu-id="286ed-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286ed-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="286ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286ed-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="286ed-140">INPUTS</span></span>

### <span data-ttu-id="286ed-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="286ed-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="286ed-142">System.String</span><span class="sxs-lookup"><span data-stu-id="286ed-142">System.String</span></span>

## <span data-ttu-id="286ed-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="286ed-143">OUTPUTS</span></span>

### <span data-ttu-id="286ed-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="286ed-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="286ed-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="286ed-145">NOTES</span></span>

## <span data-ttu-id="286ed-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="286ed-146">RELATED LINKS</span></span>

[<span data-ttu-id="286ed-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="286ed-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)