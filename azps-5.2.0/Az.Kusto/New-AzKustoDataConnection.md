---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261296"
---
# <span data-ttu-id="8b0f1-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="8b0f1-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="8b0f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0f1-103">Cria ou atualiza uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="8b0f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b0f1-104">SYNTAX</span></span>

### <span data-ttu-id="8b0f1-105">CreateExpandedEventHub (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b0f1-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8b0f1-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8b0f1-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b0f1-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="8b0f1-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8b0f1-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8b0f1-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b0f1-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="8b0f1-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b0f1-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b0f1-110">DESCRIPTION</span></span>
<span data-ttu-id="8b0f1-111">Cria ou atualiza uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="8b0f1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b0f1-112">EXAMPLES</span></span>

### <span data-ttu-id="8b0f1-113">Exemplo 1: criar uma nova conexão de dados do EventHub</span><span class="sxs-lookup"><span data-stu-id="8b0f1-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8b0f1-114">O comando acima cria uma nova conexão de dados do EventHub chamada "myeventhubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8b0f1-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8b0f1-115">Exemplo 2: criar uma nova conexão de dados do EventGrid</span><span class="sxs-lookup"><span data-stu-id="8b0f1-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8b0f1-116">O comando acima cria uma nova conexão de dados EventGrid chamada "myeventgriddc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8b0f1-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8b0f1-117">Exemplo 3: criar uma nova conexão de dados do IotHub</span><span class="sxs-lookup"><span data-stu-id="8b0f1-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8b0f1-118">O comando acima cria uma nova conexão de dados IotHub chamada "myiothubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="8b0f1-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="8b0f1-119">OS</span><span class="sxs-lookup"><span data-stu-id="8b0f1-119">PARAMETERS</span></span>

### <span data-ttu-id="8b0f1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b0f1-120">-AsJob</span></span>
<span data-ttu-id="8b0f1-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8b0f1-121">Run the command as a job</span></span>

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

### <span data-ttu-id="8b0f1-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="8b0f1-122">-BlobStorageEventType</span></span>
<span data-ttu-id="8b0f1-123">O nome do tipo de evento de armazenamento de blob a processar.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8b0f1-124">-ClusterName</span></span>
<span data-ttu-id="8b0f1-125">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8b0f1-126">-Compactação</span><span class="sxs-lookup"><span data-stu-id="8b0f1-126">-Compression</span></span>
<span data-ttu-id="8b0f1-127">O tipo de compactação de mensagens do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-128">-Consumer</span><span class="sxs-lookup"><span data-stu-id="8b0f1-128">-ConsumerGroup</span></span>
<span data-ttu-id="8b0f1-129">O grupo de consumidores do evento/Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="8b0f1-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b0f1-130">-DatabaseName</span></span>
<span data-ttu-id="8b0f1-131">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="8b0f1-132">-Formato DataFormat</span><span class="sxs-lookup"><span data-stu-id="8b0f1-132">-DataFormat</span></span>
<span data-ttu-id="8b0f1-133">O formato de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-133">The data format of the message.</span></span>
<span data-ttu-id="8b0f1-134">Opcionalmente, o formato de dados pode ser adicionado a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0f1-135">-DefaultProfile</span></span>
<span data-ttu-id="8b0f1-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8b0f1-137">-EventHubResourceId</span></span>
<span data-ttu-id="8b0f1-138">A ID do recurso do hub de eventos a ser usado para criar uma conexão de dados/grade de eventos está configurada para enviar eventos.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="8b0f1-139">-EventSystemProperty</span></span>
<span data-ttu-id="8b0f1-140">Propriedades do sistema do hub de eventos/IOT.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="8b0f1-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="8b0f1-142">Se definido como true, indica que a inclusão deve ignorar o primeiro registro de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8b0f1-143">-IotHubResourceId</span></span>
<span data-ttu-id="8b0f1-144">A ID do recurso do Hub IOT a ser usado para criar uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="8b0f1-145">-Kind</span></span>
<span data-ttu-id="8b0f1-146">Tipo de ponto de extremidade para conexão de dados</span><span class="sxs-lookup"><span data-stu-id="8b0f1-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-147">-Local</span><span class="sxs-lookup"><span data-stu-id="8b0f1-147">-Location</span></span>
<span data-ttu-id="8b0f1-148">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-148">Resource location.</span></span>

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

### <span data-ttu-id="8b0f1-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="8b0f1-149">-MappingRuleName</span></span>
<span data-ttu-id="8b0f1-150">A regra de mapeamento a ser usada para absorver os dados.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="8b0f1-151">Opcionalmente, as informações de mapeamento podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="8b0f1-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b0f1-152">-Name</span></span>
<span data-ttu-id="8b0f1-153">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-154">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8b0f1-154">-NoWait</span></span>
<span data-ttu-id="8b0f1-155">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8b0f1-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b0f1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0f1-156">-ResourceGroupName</span></span>
<span data-ttu-id="8b0f1-157">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8b0f1-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="8b0f1-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="8b0f1-159">O nome da política de acesso de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8b0f1-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="8b0f1-161">A ID do recurso da conta de armazenamento na qual os dados residem.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b0f1-162">-SubscriptionId</span></span>
<span data-ttu-id="8b0f1-163">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b0f1-164">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0f1-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="8b0f1-165">-TableName</span></span>
<span data-ttu-id="8b0f1-166">A tabela na qual os dados devem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="8b0f1-167">Opcionalmente, as informações da tabela podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="8b0f1-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b0f1-168">-Confirm</span></span>
<span data-ttu-id="8b0f1-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0f1-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0f1-170">-WhatIf</span></span>
<span data-ttu-id="8b0f1-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0f1-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0f1-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0f1-173">CommonParameters</span></span>
<span data-ttu-id="8b0f1-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0f1-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0f1-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b0f1-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0f1-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b0f1-176">INPUTS</span></span>

## <span data-ttu-id="8b0f1-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b0f1-177">OUTPUTS</span></span>

### <span data-ttu-id="8b0f1-178">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="8b0f1-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="8b0f1-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b0f1-179">NOTES</span></span>

<span data-ttu-id="8b0f1-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b0f1-180">ALIASES</span></span>

## <span data-ttu-id="8b0f1-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b0f1-181">RELATED LINKS</span></span>

