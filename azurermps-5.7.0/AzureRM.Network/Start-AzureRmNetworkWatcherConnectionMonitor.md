---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: cf67e27a8f502a753cded74f0cb5bf48ceb2d4ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602366"
---
# <span data-ttu-id="cbf06-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf06-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="cbf06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbf06-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf06-103">Iniciar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="cbf06-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbf06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbf06-104">SYNTAX</span></span>

### <span data-ttu-id="cbf06-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cbf06-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbf06-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cbf06-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf06-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cbf06-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf06-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf06-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf06-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="cbf06-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf06-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbf06-110">DESCRIPTION</span></span>
<span data-ttu-id="cbf06-111">O cmdlet Start-AzureRmNetworkWatcherConnectionMonitor inicia o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="cbf06-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="cbf06-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbf06-112">EXAMPLES</span></span>

### <span data-ttu-id="cbf06-113">Exemplo 1: iniciar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="cbf06-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="cbf06-114">Neste exemplo, começamos o monitor de conexão especificado por nome e Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="cbf06-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="cbf06-115">OS</span><span class="sxs-lookup"><span data-stu-id="cbf06-115">PARAMETERS</span></span>

### <span data-ttu-id="cbf06-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbf06-116">-AsJob</span></span>
<span data-ttu-id="cbf06-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbf06-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbf06-118">-Confirm</span></span>
<span data-ttu-id="cbf06-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf06-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf06-120">-DefaultProfile</span></span>
<span data-ttu-id="cbf06-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf06-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbf06-122">-InputObject</span></span>
<span data-ttu-id="cbf06-123">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="cbf06-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-124">-Local</span><span class="sxs-lookup"><span data-stu-id="cbf06-124">-Location</span></span>
<span data-ttu-id="cbf06-125">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="cbf06-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbf06-126">-Name</span></span>
<span data-ttu-id="cbf06-127">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="cbf06-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf06-128">-NetworkWatcher</span></span>
<span data-ttu-id="cbf06-129">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="cbf06-129">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cbf06-130">-NetworkWatcherName</span></span>
<span data-ttu-id="cbf06-131">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="cbf06-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbf06-132">-PassThru</span></span>
<span data-ttu-id="cbf06-133">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="cbf06-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf06-134">-ResourceGroupName</span></span>
<span data-ttu-id="cbf06-135">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="cbf06-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf06-136">-ResourceId</span></span>
<span data-ttu-id="cbf06-137">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cbf06-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf06-138">-WhatIf</span></span>
<span data-ttu-id="cbf06-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbf06-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf06-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbf06-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf06-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf06-141">CommonParameters</span></span>
<span data-ttu-id="cbf06-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf06-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cbf06-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf06-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf06-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbf06-144">INPUTS</span></span>

### <span data-ttu-id="cbf06-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf06-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cbf06-146">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="cbf06-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="cbf06-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbf06-147">OUTPUTS</span></span>

### <span data-ttu-id="cbf06-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbf06-148">System.Boolean</span></span>

## <span data-ttu-id="cbf06-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbf06-149">NOTES</span></span>
<span data-ttu-id="cbf06-150">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="cbf06-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="cbf06-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbf06-151">RELATED LINKS</span></span>

[<span data-ttu-id="cbf06-152">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf06-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cbf06-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf06-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cbf06-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf06-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cbf06-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cbf06-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="cbf06-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cbf06-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="cbf06-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cbf06-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="cbf06-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cbf06-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="cbf06-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf06-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cbf06-160">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cbf06-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="cbf06-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf06-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cbf06-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf06-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cbf06-163">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf06-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cbf06-164">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf06-164">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cbf06-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cbf06-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="cbf06-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf06-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cbf06-167">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf06-167">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cbf06-168">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf06-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cbf06-169">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf06-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
