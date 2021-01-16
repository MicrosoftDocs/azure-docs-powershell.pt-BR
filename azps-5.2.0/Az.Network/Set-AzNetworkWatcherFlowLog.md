---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260075"
---
# <span data-ttu-id="44db5-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="44db5-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="44db5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44db5-102">SYNOPSIS</span></span>
<span data-ttu-id="44db5-103">Atualiza o recurso de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-103">Updates flow log resource.</span></span>

## <span data-ttu-id="44db5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44db5-104">SYNTAX</span></span>

### <span data-ttu-id="44db5-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="44db5-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="44db5-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="44db5-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="44db5-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="44db5-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="44db5-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="44db5-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="44db5-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db5-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="44db5-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44db5-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44db5-114">DESCRIPTION</span></span>
<span data-ttu-id="44db5-115">Atualiza o recurso de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-115">Updates flow log resource.</span></span>

## <span data-ttu-id="44db5-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44db5-116">EXAMPLES</span></span>

### <span data-ttu-id="44db5-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44db5-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="44db5-118">Nome: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: localização bem-sucedida: lesteus TargetResourceId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG Storageid:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/mystorage habilitado: true RetentionPolicy: {"Days", "versão", ", false} Format: {" Type ":" JSON "," versão ": 2} FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="44db5-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="44db5-119">OS</span><span class="sxs-lookup"><span data-stu-id="44db5-119">PARAMETERS</span></span>

### <span data-ttu-id="44db5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44db5-120">-DefaultProfile</span></span>
<span data-ttu-id="44db5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44db5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44db5-122">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="44db5-122">-Enabled</span></span>
<span data-ttu-id="44db5-123">Sinalizador para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="44db5-124">-EnableRetention</span></span>
<span data-ttu-id="44db5-125">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="44db5-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="44db5-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="44db5-127">Sinalizar para habilitar/desabilitar TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="44db5-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-128">-Force</span><span class="sxs-lookup"><span data-stu-id="44db5-128">-Force</span></span>
<span data-ttu-id="44db5-129">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="44db5-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="44db5-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="44db5-130">-FormatType</span></span>
<span data-ttu-id="44db5-131">O tipo de arquivo do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-131">The file type of flow log.</span></span>
<span data-ttu-id="44db5-132">Agora, o único valor com suporte é ' JSON '.</span><span class="sxs-lookup"><span data-stu-id="44db5-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="44db5-133">-FormatVersion</span></span>
<span data-ttu-id="44db5-134">A versão (revisão) do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44db5-135">-InputObject</span></span>
<span data-ttu-id="44db5-136">Objeto LOF de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-137">-Local</span><span class="sxs-lookup"><span data-stu-id="44db5-137">-Location</span></span>
<span data-ttu-id="44db5-138">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="44db5-138">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="44db5-139">-Name</span></span>
<span data-ttu-id="44db5-140">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44db5-141">-NetworkWatcher</span></span>
<span data-ttu-id="44db5-142">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="44db5-142">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="44db5-143">-NetworkWatcherName</span></span>
<span data-ttu-id="44db5-144">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="44db5-144">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44db5-145">-ResourceGroupName</span></span>
<span data-ttu-id="44db5-146">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="44db5-146">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44db5-147">-ResourceId</span></span>
<span data-ttu-id="44db5-148">FlowLog ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="44db5-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="44db5-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="44db5-150">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-151">-Storageid</span><span class="sxs-lookup"><span data-stu-id="44db5-151">-StorageId</span></span>
<span data-ttu-id="44db5-152">ID da conta de armazenamento que é usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-153">-Marca</span><span class="sxs-lookup"><span data-stu-id="44db5-153">-Tag</span></span>
<span data-ttu-id="44db5-154">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="44db5-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="44db5-155">-TargetResourceId</span></span>
<span data-ttu-id="44db5-156">ID do grupo de segurança de rede para o qual o log de fluxo será aplicado.</span><span class="sxs-lookup"><span data-stu-id="44db5-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="44db5-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="44db5-158">O intervalo em minutos que decidiria com que frequência o serviço TA deve fazer análises de fluxo.</span><span class="sxs-lookup"><span data-stu-id="44db5-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="44db5-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="44db5-160">ID do recurso do espaço de trabalho anexado.</span><span class="sxs-lookup"><span data-stu-id="44db5-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44db5-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44db5-161">-Confirm</span></span>
<span data-ttu-id="44db5-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44db5-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44db5-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44db5-163">-WhatIf</span></span>
<span data-ttu-id="44db5-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44db5-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44db5-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44db5-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44db5-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44db5-166">CommonParameters</span></span>
<span data-ttu-id="44db5-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44db5-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44db5-168">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44db5-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44db5-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44db5-169">INPUTS</span></span>

### <span data-ttu-id="44db5-170">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44db5-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="44db5-171">System. String</span><span class="sxs-lookup"><span data-stu-id="44db5-171">System.String</span></span>

### <span data-ttu-id="44db5-172">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="44db5-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="44db5-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44db5-173">OUTPUTS</span></span>

### <span data-ttu-id="44db5-174">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="44db5-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="44db5-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44db5-175">NOTES</span></span>

## <span data-ttu-id="44db5-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44db5-176">RELATED LINKS</span></span>

[<span data-ttu-id="44db5-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44db5-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="44db5-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44db5-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="44db5-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44db5-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="44db5-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="44db5-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="44db5-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="44db5-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="44db5-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="44db5-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="44db5-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="44db5-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="44db5-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44db5-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44db5-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="44db5-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="44db5-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44db5-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44db5-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44db5-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44db5-188">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44db5-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44db5-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="44db5-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="44db5-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="44db5-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="44db5-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="44db5-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="44db5-192">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44db5-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44db5-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44db5-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44db5-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44db5-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44db5-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="44db5-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="44db5-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44db5-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44db5-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44db5-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44db5-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="44db5-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="44db5-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="44db5-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="44db5-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="44db5-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="44db5-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="44db5-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="44db5-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="44db5-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="44db5-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44db5-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="44db5-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="44db5-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="44db5-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="44db5-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="44db5-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="44db5-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
