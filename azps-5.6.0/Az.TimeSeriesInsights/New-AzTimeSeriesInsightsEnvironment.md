---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 51cbe7cd6d4e08543feadb5ddd096330763b7236
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885767"
---
# <span data-ttu-id="94e1f-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="94e1f-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="94e1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="94e1f-103">Crie um ambiente no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="94e1f-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="94e1f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="94e1f-104">SYNTAX</span></span>

### <span data-ttu-id="94e1f-105">Gen1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="94e1f-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94e1f-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="94e1f-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="94e1f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="94e1f-107">DESCRIPTION</span></span>
<span data-ttu-id="94e1f-108">Crie um ambiente no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="94e1f-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="94e1f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94e1f-109">EXAMPLES</span></span>

### <span data-ttu-id="94e1f-110">Exemplo 1: criar um ambiente de insights de série de tempo Gen1</span><span class="sxs-lookup"><span data-stu-id="94e1f-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="94e1f-111">Este comando cria um ambiente de insights da série de tempo Gen1.</span><span class="sxs-lookup"><span data-stu-id="94e1f-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="94e1f-112">Exemplo 2: Criar um ambiente de insights da série de tempo Gen2</span><span class="sxs-lookup"><span data-stu-id="94e1f-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="94e1f-113">Este comando cria um ambiente de insights da série de tempo Gen2.</span><span class="sxs-lookup"><span data-stu-id="94e1f-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="94e1f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="94e1f-114">PARAMETERS</span></span>

### <span data-ttu-id="94e1f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94e1f-115">-AsJob</span></span>
<span data-ttu-id="94e1f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="94e1f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="94e1f-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="94e1f-117">-Capacity</span></span>
<span data-ttu-id="94e1f-118">A capacidade do sku.</span><span class="sxs-lookup"><span data-stu-id="94e1f-118">The capacity of the sku.</span></span>
<span data-ttu-id="94e1f-119">Para ambientes Gen1, esse valor pode ser alterado para dar suporte à escala fora dos ambientes após a criação.</span><span class="sxs-lookup"><span data-stu-id="94e1f-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="94e1f-120">-DataRetentionTime</span></span>
<span data-ttu-id="94e1f-121">O tempo de retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="94e1f-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e1f-122">-DefaultProfile</span></span>
<span data-ttu-id="94e1f-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94e1f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e1f-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="94e1f-124">-Kind</span></span>
<span data-ttu-id="94e1f-125">O tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="94e1f-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-126">-Location</span><span class="sxs-lookup"><span data-stu-id="94e1f-126">-Location</span></span>
<span data-ttu-id="94e1f-127">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="94e1f-127">The location of the resource.</span></span>

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

### <span data-ttu-id="94e1f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="94e1f-128">-Name</span></span>
<span data-ttu-id="94e1f-129">Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="94e1f-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94e1f-130">-NoWait</span></span>
<span data-ttu-id="94e1f-131">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="94e1f-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94e1f-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="94e1f-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="94e1f-133">A lista de propriedades de evento que serão usadas para particionar dados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="94e1f-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="94e1f-134">Para construir, consulte a seção NOTES para propriedades PARTITIONKEYPROPERTY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="94e1f-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e1f-135">-ResourceGroupName</span></span>
<span data-ttu-id="94e1f-136">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="94e1f-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="94e1f-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="94e1f-137">-Sku</span></span>
<span data-ttu-id="94e1f-138">O nome desse SKU.</span><span class="sxs-lookup"><span data-stu-id="94e1f-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="94e1f-139">-StorageAccountKey</span></span>
<span data-ttu-id="94e1f-140">O valor da chave de gerenciamento que concede acesso de gravação de gravação do serviço Insights de Séries Temporárias à conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94e1f-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94e1f-141">-StorageAccountName</span></span>
<span data-ttu-id="94e1f-142">O nome da conta de armazenamento que armazenará os dados de longo prazo do ambiente.</span><span class="sxs-lookup"><span data-stu-id="94e1f-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="94e1f-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="94e1f-144">O comportamento que o serviço Insights da Série de Tempo deve ter quando a capacidade do ambiente tiver sido excedida</span><span class="sxs-lookup"><span data-stu-id="94e1f-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94e1f-145">-SubscriptionId</span></span>
<span data-ttu-id="94e1f-146">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="94e1f-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="94e1f-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="94e1f-147">-Tag</span></span>
<span data-ttu-id="94e1f-148">Pares de valores-chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="94e1f-148">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="94e1f-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="94e1f-150">A lista de propriedades de evento que serão usadas para definir a ID da série de tempo do ambiente. Para construir, consulte a seção NOTES para propriedades TIMESERIESIDPROPERTY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="94e1f-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="94e1f-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="94e1f-152">Timespan ISO8601 especificando o número de dias em que os eventos do ambiente estarão disponíveis para consulta no armazenamento morno.</span><span class="sxs-lookup"><span data-stu-id="94e1f-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e1f-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94e1f-153">-Confirm</span></span>
<span data-ttu-id="94e1f-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94e1f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e1f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e1f-155">-WhatIf</span></span>
<span data-ttu-id="94e1f-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94e1f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e1f-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94e1f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e1f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e1f-158">CommonParameters</span></span>
<span data-ttu-id="94e1f-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e1f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e1f-160">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94e1f-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e1f-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94e1f-161">INPUTS</span></span>

## <span data-ttu-id="94e1f-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="94e1f-162">OUTPUTS</span></span>

### <span data-ttu-id="94e1f-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="94e1f-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="94e1f-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="94e1f-164">NOTES</span></span>

<span data-ttu-id="94e1f-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="94e1f-165">ALIASES</span></span>

<span data-ttu-id="94e1f-166">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="94e1f-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94e1f-167">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="94e1f-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94e1f-168">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94e1f-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94e1f-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: a lista de propriedades de evento que serão usadas para particionar dados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="94e1f-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="94e1f-170">`[Name <String>]`: O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="94e1f-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="94e1f-171">`[Type <PropertyType?>]`: O tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="94e1f-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="94e1f-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: a lista de propriedades de evento que serão usadas para definir a id da série de tempo do ambiente.</span><span class="sxs-lookup"><span data-stu-id="94e1f-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="94e1f-173">`[Name <String>]`: O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="94e1f-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="94e1f-174">`[Type <PropertyType?>]`: O tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="94e1f-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="94e1f-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94e1f-175">RELATED LINKS</span></span>

