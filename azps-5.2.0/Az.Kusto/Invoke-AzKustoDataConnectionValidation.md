---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258075"
---
# <span data-ttu-id="30e57-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="30e57-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="30e57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30e57-102">SYNOPSIS</span></span>
<span data-ttu-id="30e57-103">Verifica se os parâmetros de conexão de dados são válidos.</span><span class="sxs-lookup"><span data-stu-id="30e57-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="30e57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30e57-104">SYNTAX</span></span>

### <span data-ttu-id="30e57-105">DataExpandedEventHub (padrão)</span><span class="sxs-lookup"><span data-stu-id="30e57-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30e57-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="30e57-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30e57-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="30e57-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30e57-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="30e57-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30e57-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="30e57-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="30e57-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="30e57-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="30e57-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="30e57-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30e57-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="30e57-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30e57-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30e57-113">DESCRIPTION</span></span>
<span data-ttu-id="30e57-114">Verifica se os parâmetros de conexão de dados são válidos.</span><span class="sxs-lookup"><span data-stu-id="30e57-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="30e57-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30e57-115">EXAMPLES</span></span>

### <span data-ttu-id="30e57-116">Exemplo 1: validar parâmetros de conexão de dados do EventHub</span><span class="sxs-lookup"><span data-stu-id="30e57-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="30e57-117">O comando acima valida a conexão de dados do EventHub chamada "myeventhubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="30e57-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30e57-118">Exemplo 2: validar parâmetros de conexão de dados do EventGrid</span><span class="sxs-lookup"><span data-stu-id="30e57-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="30e57-119">O comando acima valida a conexão de dados do EventGrid chamada "myeventgriddc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="30e57-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30e57-120">Exemplo 3: validar parâmetros de conexão de dados do IotHub</span><span class="sxs-lookup"><span data-stu-id="30e57-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="30e57-121">O comando acima valida a conexão de dados do IotHub chamada "myiothubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="30e57-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30e57-122">Exemplo 4: validar parâmetros de conexão de dados do EventHub via identidade</span><span class="sxs-lookup"><span data-stu-id="30e57-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="30e57-123">O comando acima valida a conexão de dados do EventHub chamada "myeventhubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="30e57-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30e57-124">Exemplo 5: validar parâmetros de conexão de dados EventGrid via identidade</span><span class="sxs-lookup"><span data-stu-id="30e57-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="30e57-125">O comando acima valida a conexão de dados do EventGrid chamada "myeventgriddc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="30e57-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="30e57-126">Exemplo 6: validar parâmetros de conexão de dados IotHub via identidade</span><span class="sxs-lookup"><span data-stu-id="30e57-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="30e57-127">O comando acima valida a conexão de dados do IotHub chamada "myiothubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="30e57-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="30e57-128">OS</span><span class="sxs-lookup"><span data-stu-id="30e57-128">PARAMETERS</span></span>

### <span data-ttu-id="30e57-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="30e57-129">-BlobStorageEventType</span></span>
<span data-ttu-id="30e57-130">O nome do tipo de evento de armazenamento de blob a processar.</span><span class="sxs-lookup"><span data-stu-id="30e57-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="30e57-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30e57-131">-ClusterName</span></span>
<span data-ttu-id="30e57-132">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-133">-Compactação</span><span class="sxs-lookup"><span data-stu-id="30e57-133">-Compression</span></span>
<span data-ttu-id="30e57-134">O tipo de compactação de mensagens do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="30e57-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-135">-Consumer</span><span class="sxs-lookup"><span data-stu-id="30e57-135">-ConsumerGroup</span></span>
<span data-ttu-id="30e57-136">O grupo de consumidores do evento/Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="30e57-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="30e57-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30e57-137">-DatabaseName</span></span>
<span data-ttu-id="30e57-138">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-139">-Dataconnectionname</span><span class="sxs-lookup"><span data-stu-id="30e57-139">-DataConnectionName</span></span>
<span data-ttu-id="30e57-140">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="30e57-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="30e57-141">-Formato DataFormat</span><span class="sxs-lookup"><span data-stu-id="30e57-141">-DataFormat</span></span>
<span data-ttu-id="30e57-142">O formato de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="30e57-142">The data format of the message.</span></span>
<span data-ttu-id="30e57-143">Opcionalmente, o formato de dados pode ser adicionado a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="30e57-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="30e57-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e57-144">-DefaultProfile</span></span>
<span data-ttu-id="30e57-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30e57-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e57-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="30e57-146">-EventHubResourceId</span></span>
<span data-ttu-id="30e57-147">A ID do recurso do hub de eventos a ser usado para criar uma conexão de dados/grade de eventos está configurada para enviar eventos.</span><span class="sxs-lookup"><span data-stu-id="30e57-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="30e57-148">-EventSystemProperty</span></span>
<span data-ttu-id="30e57-149">Propriedades do sistema do hub de eventos/IOT.</span><span class="sxs-lookup"><span data-stu-id="30e57-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="30e57-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="30e57-151">Se definido como true, indica que a inclusão deve ignorar o primeiro registro de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="30e57-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="30e57-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30e57-152">-InputObject</span></span>
<span data-ttu-id="30e57-153">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="30e57-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="30e57-154">-IotHubResourceId</span></span>
<span data-ttu-id="30e57-155">A ID do recurso do Hub IOT a ser usado para criar uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="30e57-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="30e57-156">-Kind</span></span>
<span data-ttu-id="30e57-157">Tipo de ponto de extremidade para conexão de dados</span><span class="sxs-lookup"><span data-stu-id="30e57-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="30e57-158">-Local</span><span class="sxs-lookup"><span data-stu-id="30e57-158">-Location</span></span>
<span data-ttu-id="30e57-159">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="30e57-159">Resource location.</span></span>

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

### <span data-ttu-id="30e57-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="30e57-160">-MappingRuleName</span></span>
<span data-ttu-id="30e57-161">A regra de mapeamento a ser usada para absorver os dados.</span><span class="sxs-lookup"><span data-stu-id="30e57-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="30e57-162">Opcionalmente, as informações de mapeamento podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="30e57-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="30e57-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e57-163">-ResourceGroupName</span></span>
<span data-ttu-id="30e57-164">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="30e57-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="30e57-166">O nome da política de acesso de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="30e57-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="30e57-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="30e57-168">A ID do recurso da conta de armazenamento na qual os dados residem.</span><span class="sxs-lookup"><span data-stu-id="30e57-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30e57-169">-SubscriptionId</span></span>
<span data-ttu-id="30e57-170">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30e57-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30e57-171">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="30e57-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e57-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="30e57-172">-TableName</span></span>
<span data-ttu-id="30e57-173">A tabela na qual os dados devem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="30e57-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="30e57-174">Opcionalmente, as informações da tabela podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="30e57-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="30e57-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="30e57-175">-Confirm</span></span>
<span data-ttu-id="30e57-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30e57-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e57-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e57-177">-WhatIf</span></span>
<span data-ttu-id="30e57-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="30e57-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30e57-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30e57-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e57-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e57-180">CommonParameters</span></span>
<span data-ttu-id="30e57-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e57-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e57-182">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30e57-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e57-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30e57-183">INPUTS</span></span>

### <span data-ttu-id="30e57-184">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="30e57-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="30e57-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30e57-185">OUTPUTS</span></span>

### <span data-ttu-id="30e57-186">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="30e57-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="30e57-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30e57-187">NOTES</span></span>

<span data-ttu-id="30e57-188">ALIASES</span><span class="sxs-lookup"><span data-stu-id="30e57-188">ALIASES</span></span>

<span data-ttu-id="30e57-189">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="30e57-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30e57-190">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="30e57-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30e57-191">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30e57-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30e57-192">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="30e57-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30e57-193">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="30e57-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="30e57-194">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="30e57-195">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="30e57-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="30e57-196">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="30e57-197">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="30e57-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30e57-198">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="30e57-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="30e57-199">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="30e57-200">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e57-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="30e57-201">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30e57-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30e57-202">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="30e57-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="30e57-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30e57-203">RELATED LINKS</span></span>

