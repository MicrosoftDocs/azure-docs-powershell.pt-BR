---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: ed697798694063c516621d25fb43e153b7a23dbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114801"
---
# <span data-ttu-id="55ed9-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="55ed9-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="55ed9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="55ed9-103">Atualiza uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="55ed9-103">Updates a data connection.</span></span>

## <span data-ttu-id="55ed9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55ed9-104">SYNTAX</span></span>

### <span data-ttu-id="55ed9-105">UpdateExpandedEventHub (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55ed9-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55ed9-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="55ed9-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55ed9-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="55ed9-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55ed9-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="55ed9-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55ed9-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="55ed9-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55ed9-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="55ed9-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55ed9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="55ed9-111">DESCRIPTION</span></span>
<span data-ttu-id="55ed9-112">Atualiza uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="55ed9-112">Updates a data connection.</span></span>

## <span data-ttu-id="55ed9-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55ed9-113">EXAMPLES</span></span>

### <span data-ttu-id="55ed9-114">Exemplo 1: Atualizar uma conexão de dados existente do EventHub</span><span class="sxs-lookup"><span data-stu-id="55ed9-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="55ed9-115">O comando acima atualiza a conexão de dados existente do EventHub chamada "myeventhubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="55ed9-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="55ed9-116">Exemplo 2: Atualizar uma conexão de dados EventGrid existente</span><span class="sxs-lookup"><span data-stu-id="55ed9-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="55ed9-117">O comando acima atualiza a conexão de dados EventGrid existente chamada "myeventgriddc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="55ed9-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="55ed9-118">Exemplo 3: Atualizar uma conexão de dados existente do IotHub</span><span class="sxs-lookup"><span data-stu-id="55ed9-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="55ed9-119">O comando acima atualiza a conexão de dados existente do IotHub chamada "myiothubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="55ed9-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="55ed9-120">Exemplo 4: Atualizar uma conexão de dados existente do EventHub via identidade</span><span class="sxs-lookup"><span data-stu-id="55ed9-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="55ed9-121">O comando acima atualiza a conexão de dados existente do EventHub chamada "myeventhubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="55ed9-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="55ed9-122">Exemplo 5: Atualizar uma conexão de dados EventGrid existente por meio de identidade</span><span class="sxs-lookup"><span data-stu-id="55ed9-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="55ed9-123">O comando acima atualiza a conexão de dados EventGrid existente chamada "myeventgriddc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="55ed9-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="55ed9-124">Exemplo 6: Atualizar uma conexão de dados existente do IotHub via identidade</span><span class="sxs-lookup"><span data-stu-id="55ed9-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="55ed9-125">O comando acima atualiza a conexão de dados existente do IotHub chamada "myiothubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="55ed9-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="55ed9-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55ed9-126">PARAMETERS</span></span>

### <span data-ttu-id="55ed9-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55ed9-127">-AsJob</span></span>
<span data-ttu-id="55ed9-128">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="55ed9-128">Run the command as a job</span></span>

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

### <span data-ttu-id="55ed9-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="55ed9-129">-BlobStorageEventType</span></span>
<span data-ttu-id="55ed9-130">O nome do tipo de evento de armazenamento de blob para processar.</span><span class="sxs-lookup"><span data-stu-id="55ed9-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="55ed9-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="55ed9-131">-ClusterName</span></span>
<span data-ttu-id="55ed9-132">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="55ed9-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-133">-Compactação</span><span class="sxs-lookup"><span data-stu-id="55ed9-133">-Compression</span></span>
<span data-ttu-id="55ed9-134">O tipo de compactação de mensagens do hub de evento.</span><span class="sxs-lookup"><span data-stu-id="55ed9-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="55ed9-135">-ConsumerGroup</span></span>
<span data-ttu-id="55ed9-136">O grupo de consumidores do hub de eventos/iot.</span><span class="sxs-lookup"><span data-stu-id="55ed9-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="55ed9-137">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="55ed9-137">-DatabaseName</span></span>
<span data-ttu-id="55ed9-138">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="55ed9-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="55ed9-139">-DataFormat</span></span>
<span data-ttu-id="55ed9-140">O formato de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="55ed9-140">The data format of the message.</span></span>
<span data-ttu-id="55ed9-141">Opcionalmente, o formato de dados pode ser adicionado a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="55ed9-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="55ed9-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ed9-142">-DefaultProfile</span></span>
<span data-ttu-id="55ed9-143">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55ed9-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ed9-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="55ed9-144">-EventHubResourceId</span></span>
<span data-ttu-id="55ed9-145">A ID do recurso do hub de eventos a ser usado para criar uma conexão de dados/grade de evento está configurada para enviar eventos.</span><span class="sxs-lookup"><span data-stu-id="55ed9-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="55ed9-146">-EventSystemProperty</span></span>
<span data-ttu-id="55ed9-147">Propriedades do sistema do hub de evento/iot.</span><span class="sxs-lookup"><span data-stu-id="55ed9-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="55ed9-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="55ed9-149">Se definido como verdadeiro, indica que a ingestão deve ignorar o primeiro registro de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="55ed9-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="55ed9-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55ed9-150">-InputObject</span></span>
<span data-ttu-id="55ed9-151">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="55ed9-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="55ed9-152">-IotHubResourceId</span></span>
<span data-ttu-id="55ed9-153">A ID de recurso do hub Iot a ser usado para criar uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="55ed9-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-154">-Tipo</span><span class="sxs-lookup"><span data-stu-id="55ed9-154">-Kind</span></span>
<span data-ttu-id="55ed9-155">Tipo de ponto de extremidade para a conexão de dados</span><span class="sxs-lookup"><span data-stu-id="55ed9-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="55ed9-156">-Local</span><span class="sxs-lookup"><span data-stu-id="55ed9-156">-Location</span></span>
<span data-ttu-id="55ed9-157">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="55ed9-157">Resource location.</span></span>

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

### <span data-ttu-id="55ed9-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="55ed9-158">-MappingRuleName</span></span>
<span data-ttu-id="55ed9-159">A regra de mapeamento a ser usada para ingerir os dados.</span><span class="sxs-lookup"><span data-stu-id="55ed9-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="55ed9-160">Opcionalmente, as informações de mapeamento podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="55ed9-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="55ed9-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="55ed9-161">-Name</span></span>
<span data-ttu-id="55ed9-162">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="55ed9-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55ed9-163">-NoWait</span></span>
<span data-ttu-id="55ed9-164">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="55ed9-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55ed9-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ed9-165">-ResourceGroupName</span></span>
<span data-ttu-id="55ed9-166">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="55ed9-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="55ed9-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="55ed9-168">O nome da política de acesso de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="55ed9-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="55ed9-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="55ed9-170">A ID do recurso da conta de armazenamento onde os dados residem.</span><span class="sxs-lookup"><span data-stu-id="55ed9-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55ed9-171">-SubscriptionId</span></span>
<span data-ttu-id="55ed9-172">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="55ed9-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="55ed9-173">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="55ed9-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed9-174">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="55ed9-174">-TableName</span></span>
<span data-ttu-id="55ed9-175">A tabela onde os dados devem ser ingeridos.</span><span class="sxs-lookup"><span data-stu-id="55ed9-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="55ed9-176">Opcionalmente, as informações da tabela podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="55ed9-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="55ed9-177">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55ed9-177">-Confirm</span></span>
<span data-ttu-id="55ed9-178">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55ed9-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ed9-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ed9-179">-WhatIf</span></span>
<span data-ttu-id="55ed9-180">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55ed9-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ed9-181">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55ed9-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ed9-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ed9-182">CommonParameters</span></span>
<span data-ttu-id="55ed9-183">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ed9-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ed9-184">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55ed9-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ed9-185">Entradas</span><span class="sxs-lookup"><span data-stu-id="55ed9-185">INPUTS</span></span>

### <span data-ttu-id="55ed9-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="55ed9-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="55ed9-187">Saídas</span><span class="sxs-lookup"><span data-stu-id="55ed9-187">OUTPUTS</span></span>

### <span data-ttu-id="55ed9-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="55ed9-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="55ed9-189">Notas</span><span class="sxs-lookup"><span data-stu-id="55ed9-189">NOTES</span></span>

<span data-ttu-id="55ed9-190">Aliases</span><span class="sxs-lookup"><span data-stu-id="55ed9-190">ALIASES</span></span>

<span data-ttu-id="55ed9-191">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="55ed9-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55ed9-192">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="55ed9-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55ed9-193">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55ed9-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55ed9-194">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="55ed9-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55ed9-195">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="55ed9-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="55ed9-196">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="55ed9-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="55ed9-197">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="55ed9-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="55ed9-198">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="55ed9-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="55ed9-199">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="55ed9-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55ed9-200">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="55ed9-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="55ed9-201">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="55ed9-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="55ed9-202">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="55ed9-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="55ed9-203">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="55ed9-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="55ed9-204">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="55ed9-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="55ed9-205">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55ed9-205">RELATED LINKS</span></span>

