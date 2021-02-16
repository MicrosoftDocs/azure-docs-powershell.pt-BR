---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: ab58d679e9fc3ad62baeded8622b81a0cb8b2f95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117593"
---
# <span data-ttu-id="c0f58-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="c0f58-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="c0f58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0f58-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f58-103">Cria ou atualiza uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c0f58-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="c0f58-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0f58-104">SYNTAX</span></span>

### <span data-ttu-id="c0f58-105">CreateExpandedEventHub (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c0f58-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c0f58-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c0f58-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0f58-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="c0f58-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c0f58-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c0f58-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0f58-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c0f58-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0f58-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0f58-110">DESCRIPTION</span></span>
<span data-ttu-id="c0f58-111">Cria ou atualiza uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c0f58-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="c0f58-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0f58-112">EXAMPLES</span></span>

### <span data-ttu-id="c0f58-113">Exemplo 1: Criar uma nova conexão de dados eventHub</span><span class="sxs-lookup"><span data-stu-id="c0f58-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c0f58-114">O comando acima cria uma nova conexão de dados eventHub chamada "myeventhubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c0f58-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c0f58-115">Exemplo 2: Criar uma nova conexão de dados EventGrid</span><span class="sxs-lookup"><span data-stu-id="c0f58-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c0f58-116">O comando acima cria uma nova conexão de dados EventGrid chamada "myeventgriddc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c0f58-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c0f58-117">Exemplo 3: Criar uma nova conexão de dados do IotHub</span><span class="sxs-lookup"><span data-stu-id="c0f58-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c0f58-118">O comando acima cria uma nova conexão de dados do IotHub chamada "myiothubdc" para o banco de dados "mykustodatabase" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="c0f58-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c0f58-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0f58-119">PARAMETERS</span></span>

### <span data-ttu-id="c0f58-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0f58-120">-AsJob</span></span>
<span data-ttu-id="c0f58-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c0f58-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c0f58-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="c0f58-122">-BlobStorageEventType</span></span>
<span data-ttu-id="c0f58-123">O nome do tipo de evento de armazenamento de blob para processar.</span><span class="sxs-lookup"><span data-stu-id="c0f58-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="c0f58-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0f58-124">-ClusterName</span></span>
<span data-ttu-id="c0f58-125">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="c0f58-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0f58-126">-Compactação</span><span class="sxs-lookup"><span data-stu-id="c0f58-126">-Compression</span></span>
<span data-ttu-id="c0f58-127">O tipo de compactação de mensagens do hub de evento.</span><span class="sxs-lookup"><span data-stu-id="c0f58-127">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="c0f58-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c0f58-128">-ConsumerGroup</span></span>
<span data-ttu-id="c0f58-129">O grupo de consumidores do hub de eventos/iot.</span><span class="sxs-lookup"><span data-stu-id="c0f58-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="c0f58-130">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="c0f58-130">-DatabaseName</span></span>
<span data-ttu-id="c0f58-131">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="c0f58-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0f58-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="c0f58-132">-DataFormat</span></span>
<span data-ttu-id="c0f58-133">O formato de dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0f58-133">The data format of the message.</span></span>
<span data-ttu-id="c0f58-134">Opcionalmente, o formato de dados pode ser adicionado a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0f58-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="c0f58-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f58-135">-DefaultProfile</span></span>
<span data-ttu-id="c0f58-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f58-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0f58-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c0f58-137">-EventHubResourceId</span></span>
<span data-ttu-id="c0f58-138">A ID do recurso do hub de eventos a ser usado para criar uma conexão de dados/grade de evento está configurada para enviar eventos.</span><span class="sxs-lookup"><span data-stu-id="c0f58-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="c0f58-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="c0f58-139">-EventSystemProperty</span></span>
<span data-ttu-id="c0f58-140">Propriedades do sistema do hub de evento/iot.</span><span class="sxs-lookup"><span data-stu-id="c0f58-140">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="c0f58-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="c0f58-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="c0f58-142">Se definido como verdadeiro, indica que a ingestão deve ignorar o primeiro registro de cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0f58-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="c0f58-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c0f58-143">-IotHubResourceId</span></span>
<span data-ttu-id="c0f58-144">A ID de recurso do hub Iot a ser usado para criar uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c0f58-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="c0f58-145">-Tipo</span><span class="sxs-lookup"><span data-stu-id="c0f58-145">-Kind</span></span>
<span data-ttu-id="c0f58-146">Tipo de ponto de extremidade para a conexão de dados</span><span class="sxs-lookup"><span data-stu-id="c0f58-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="c0f58-147">-Local</span><span class="sxs-lookup"><span data-stu-id="c0f58-147">-Location</span></span>
<span data-ttu-id="c0f58-148">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c0f58-148">Resource location.</span></span>

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

### <span data-ttu-id="c0f58-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="c0f58-149">-MappingRuleName</span></span>
<span data-ttu-id="c0f58-150">A regra de mapeamento a ser usada para ingerir os dados.</span><span class="sxs-lookup"><span data-stu-id="c0f58-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="c0f58-151">Opcionalmente, as informações de mapeamento podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0f58-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="c0f58-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0f58-152">-Name</span></span>
<span data-ttu-id="c0f58-153">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c0f58-153">The name of the data connection.</span></span>

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

### <span data-ttu-id="c0f58-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0f58-154">-NoWait</span></span>
<span data-ttu-id="c0f58-155">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="c0f58-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c0f58-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f58-156">-ResourceGroupName</span></span>
<span data-ttu-id="c0f58-157">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="c0f58-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0f58-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="c0f58-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="c0f58-159">O nome da política de acesso de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c0f58-159">The name of the share access policy.</span></span>

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

### <span data-ttu-id="c0f58-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c0f58-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="c0f58-161">A ID do recurso da conta de armazenamento onde os dados residem.</span><span class="sxs-lookup"><span data-stu-id="c0f58-161">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="c0f58-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0f58-162">-SubscriptionId</span></span>
<span data-ttu-id="c0f58-163">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f58-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0f58-164">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c0f58-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c0f58-165">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="c0f58-165">-TableName</span></span>
<span data-ttu-id="c0f58-166">A tabela onde os dados devem ser ingeridos.</span><span class="sxs-lookup"><span data-stu-id="c0f58-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="c0f58-167">Opcionalmente, as informações da tabela podem ser adicionadas a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0f58-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="c0f58-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c0f58-168">-Confirm</span></span>
<span data-ttu-id="c0f58-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f58-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0f58-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0f58-170">-WhatIf</span></span>
<span data-ttu-id="c0f58-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c0f58-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0f58-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0f58-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0f58-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f58-173">CommonParameters</span></span>
<span data-ttu-id="c0f58-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f58-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f58-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0f58-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f58-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="c0f58-176">INPUTS</span></span>

## <span data-ttu-id="c0f58-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="c0f58-177">OUTPUTS</span></span>

### <span data-ttu-id="c0f58-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="c0f58-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="c0f58-179">Notas</span><span class="sxs-lookup"><span data-stu-id="c0f58-179">NOTES</span></span>

<span data-ttu-id="c0f58-180">Aliases</span><span class="sxs-lookup"><span data-stu-id="c0f58-180">ALIASES</span></span>

## <span data-ttu-id="c0f58-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0f58-181">RELATED LINKS</span></span>

