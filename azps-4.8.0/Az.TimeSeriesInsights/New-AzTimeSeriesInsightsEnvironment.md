---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113445"
---
# <span data-ttu-id="bb33f-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb33f-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="bb33f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb33f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb33f-103">Criar um ambiente na assinatura especificada e no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb33f-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="bb33f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb33f-104">SYNTAX</span></span>

### <span data-ttu-id="bb33f-105">Gen1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb33f-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb33f-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="bb33f-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bb33f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb33f-107">DESCRIPTION</span></span>
<span data-ttu-id="bb33f-108">Criar um ambiente na assinatura especificada e no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb33f-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="bb33f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb33f-109">EXAMPLES</span></span>

### <span data-ttu-id="bb33f-110">Exemplo 1: criar um ambiente do insights série de tempo do Gen1</span><span class="sxs-lookup"><span data-stu-id="bb33f-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="bb33f-111">Esse comando cria um ambiente do insights série tempo do Gen1.</span><span class="sxs-lookup"><span data-stu-id="bb33f-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="bb33f-112">Exemplo 2: criar um ambiente do insights série de tempo do Gen2</span><span class="sxs-lookup"><span data-stu-id="bb33f-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="bb33f-113">Esse comando cria um ambiente do insights série tempo do Gen2.</span><span class="sxs-lookup"><span data-stu-id="bb33f-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="bb33f-114">OS</span><span class="sxs-lookup"><span data-stu-id="bb33f-114">PARAMETERS</span></span>

### <span data-ttu-id="bb33f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb33f-115">-AsJob</span></span>
<span data-ttu-id="bb33f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="bb33f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bb33f-117">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="bb33f-117">-Capacity</span></span>
<span data-ttu-id="bb33f-118">A capacidade da SKU.</span><span class="sxs-lookup"><span data-stu-id="bb33f-118">The capacity of the sku.</span></span>
<span data-ttu-id="bb33f-119">Para ambientes Gen1, esse valor pode ser alterado para dar suporte ao dimensionamento de ambientes após a criação.</span><span class="sxs-lookup"><span data-stu-id="bb33f-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="bb33f-120">-Dataretençãotime</span><span class="sxs-lookup"><span data-stu-id="bb33f-120">-DataRetentionTime</span></span>
<span data-ttu-id="bb33f-121">O tempo de retenção de dados.</span><span class="sxs-lookup"><span data-stu-id="bb33f-121">The data retention time.</span></span>

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

### <span data-ttu-id="bb33f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb33f-122">-DefaultProfile</span></span>
<span data-ttu-id="bb33f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb33f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb33f-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="bb33f-124">-Kind</span></span>
<span data-ttu-id="bb33f-125">O tipo do ambiente.</span><span class="sxs-lookup"><span data-stu-id="bb33f-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="bb33f-126">-Local</span><span class="sxs-lookup"><span data-stu-id="bb33f-126">-Location</span></span>
<span data-ttu-id="bb33f-127">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="bb33f-127">The location of the resource.</span></span>

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

### <span data-ttu-id="bb33f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb33f-128">-Name</span></span>
<span data-ttu-id="bb33f-129">Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="bb33f-129">Name of the environment</span></span>

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

### <span data-ttu-id="bb33f-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bb33f-130">-NoWait</span></span>
<span data-ttu-id="bb33f-131">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="bb33f-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb33f-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="bb33f-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="bb33f-133">A lista de propriedades de evento que será usada para particionar dados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="bb33f-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="bb33f-134">Para construir, consulte a seção notas para propriedades PARTITIONKEYPROPERTY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bb33f-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb33f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb33f-135">-ResourceGroupName</span></span>
<span data-ttu-id="bb33f-136">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb33f-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="bb33f-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="bb33f-137">-Sku</span></span>
<span data-ttu-id="bb33f-138">O nome desta SKU.</span><span class="sxs-lookup"><span data-stu-id="bb33f-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="bb33f-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bb33f-139">-StorageAccountKey</span></span>
<span data-ttu-id="bb33f-140">O valor da chave de gerenciamento que concede o acesso de gravação do serviço de insights série de tempo à conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bb33f-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="bb33f-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb33f-141">-StorageAccountName</span></span>
<span data-ttu-id="bb33f-142">O nome da conta de armazenamento que manterá os dados de longo prazo do ambiente.</span><span class="sxs-lookup"><span data-stu-id="bb33f-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="bb33f-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="bb33f-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="bb33f-144">O comportamento que o serviço insights de série de tempo deve levar quando a capacidade do ambiente foi excedida</span><span class="sxs-lookup"><span data-stu-id="bb33f-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="bb33f-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb33f-145">-SubscriptionId</span></span>
<span data-ttu-id="bb33f-146">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb33f-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bb33f-147">-Marca</span><span class="sxs-lookup"><span data-stu-id="bb33f-147">-Tag</span></span>
<span data-ttu-id="bb33f-148">Pares de valores chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bb33f-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="bb33f-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="bb33f-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="bb33f-150">A lista de propriedades do evento que será usada para definir a ID da série temporal do ambiente. Para construir, consulte a seção notas para propriedades TIMESERIESIDPROPERTY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bb33f-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb33f-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="bb33f-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="bb33f-152">ISO8601 TimeSpan especificando o número de dias pelos quais os eventos do ambiente estarão disponíveis para consulta na loja quente.</span><span class="sxs-lookup"><span data-stu-id="bb33f-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="bb33f-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb33f-153">-Confirm</span></span>
<span data-ttu-id="bb33f-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb33f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb33f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb33f-155">-WhatIf</span></span>
<span data-ttu-id="bb33f-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb33f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb33f-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb33f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb33f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb33f-158">CommonParameters</span></span>
<span data-ttu-id="bb33f-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb33f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb33f-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb33f-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb33f-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb33f-161">INPUTS</span></span>

## <span data-ttu-id="bb33f-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb33f-162">OUTPUTS</span></span>

### <span data-ttu-id="bb33f-163">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="bb33f-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="bb33f-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb33f-164">NOTES</span></span>

<span data-ttu-id="bb33f-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bb33f-165">ALIASES</span></span>

<span data-ttu-id="bb33f-166">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="bb33f-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb33f-167">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="bb33f-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb33f-168">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb33f-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb33f-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: a lista de propriedades do evento que será usada para particionar dados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="bb33f-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="bb33f-170">`[Name <String>]`: O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb33f-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="bb33f-171">`[Type <PropertyType?>]`: O tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb33f-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="bb33f-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: a lista de propriedades do evento que será usada para definir a ID da série temporal do ambiente.</span><span class="sxs-lookup"><span data-stu-id="bb33f-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="bb33f-173">`[Name <String>]`: O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb33f-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="bb33f-174">`[Type <PropertyType?>]`: O tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb33f-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="bb33f-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb33f-175">RELATED LINKS</span></span>

