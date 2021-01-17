---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: f80543b245c59cee7261d062c741788489fb5cb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433353"
---
# <span data-ttu-id="6c84e-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c84e-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="6c84e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c84e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c84e-103">Interrompe a operação de captura de pacote em uma conexão VPN</span><span class="sxs-lookup"><span data-stu-id="6c84e-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="6c84e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c84e-104">SYNTAX</span></span>

### <span data-ttu-id="6c84e-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6c84e-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c84e-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6c84e-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c84e-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="6c84e-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c84e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c84e-108">DESCRIPTION</span></span>
<span data-ttu-id="6c84e-109">Interrompe a operação de captura de pacote em uma conexão VPN e carrega o resultado em determinado SasUrl contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c84e-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="6c84e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c84e-110">EXAMPLES</span></span>

### <span data-ttu-id="6c84e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c84e-111">Example 1</span></span>
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

### <span data-ttu-id="6c84e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6c84e-112">Example 2</span></span>
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

## <span data-ttu-id="6c84e-113">OS</span><span class="sxs-lookup"><span data-stu-id="6c84e-113">PARAMETERS</span></span>

### <span data-ttu-id="6c84e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c84e-114">-AsJob</span></span>
<span data-ttu-id="6c84e-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6c84e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c84e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c84e-116">-DefaultProfile</span></span>
<span data-ttu-id="6c84e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c84e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c84e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c84e-118">-InputObject</span></span>
<span data-ttu-id="6c84e-119">O objeto de conexão VPN em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6c84e-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="6c84e-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="6c84e-120">-LinkConnectionName</span></span>
<span data-ttu-id="6c84e-121">Os nomes da SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="6c84e-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="6c84e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c84e-122">-Name</span></span>
<span data-ttu-id="6c84e-123">O nome da conexão VPN na qual a captura de pacotes deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6c84e-123">The Vpn connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="6c84e-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6c84e-124">-ParentResourceName</span></span>
<span data-ttu-id="6c84e-125">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="6c84e-125">The parent resource name.</span></span>

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

### <span data-ttu-id="6c84e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c84e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c84e-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c84e-127">The resource group name.</span></span>

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

### <span data-ttu-id="6c84e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c84e-128">-ResourceId</span></span>
<span data-ttu-id="6c84e-129">A ID de recurso do Azure do VpnConnection em que a captura de pacote deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="6c84e-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="6c84e-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="6c84e-130">-SasUrl</span></span>
<span data-ttu-id="6c84e-131">URL SAS para parar captura de pacote na VPN.</span><span class="sxs-lookup"><span data-stu-id="6c84e-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="6c84e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c84e-132">-Confirm</span></span>
<span data-ttu-id="6c84e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c84e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c84e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c84e-134">-WhatIf</span></span>
<span data-ttu-id="6c84e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c84e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c84e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c84e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c84e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c84e-137">CommonParameters</span></span>
<span data-ttu-id="6c84e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c84e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c84e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c84e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c84e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c84e-140">INPUTS</span></span>

### <span data-ttu-id="6c84e-141">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6c84e-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="6c84e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6c84e-142">System.String</span></span>

## <span data-ttu-id="6c84e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c84e-143">OUTPUTS</span></span>

### <span data-ttu-id="6c84e-144">Microsoft. Azure. Commands. Network. Models. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="6c84e-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="6c84e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c84e-145">NOTES</span></span>

## <span data-ttu-id="6c84e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c84e-146">RELATED LINKS</span></span>

[<span data-ttu-id="6c84e-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c84e-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)