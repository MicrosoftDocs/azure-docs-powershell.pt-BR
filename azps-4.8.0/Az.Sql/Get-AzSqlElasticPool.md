---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110836"
---
# <span data-ttu-id="4e907-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4e907-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="4e907-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e907-102">SYNOPSIS</span></span>
<span data-ttu-id="4e907-103">Obtém pools elásticos e seus valores de propriedade em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e907-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="4e907-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e907-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e907-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e907-105">DESCRIPTION</span></span>
<span data-ttu-id="4e907-106">O cmdlet **Get-AzSqlElasticPool** Obtém pools elásticos e seus valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="4e907-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="4e907-107">Especifique o nome de um pool elástico existente para ver os valores de propriedade somente para esse pool.</span><span class="sxs-lookup"><span data-stu-id="4e907-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="4e907-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e907-108">EXAMPLES</span></span>

### <span data-ttu-id="4e907-109">Exemplo 1: obter todos os pools elásticos</span><span class="sxs-lookup"><span data-stu-id="4e907-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4e907-110">Esse comando obtém todos os pools elásticos no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="4e907-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="4e907-111">Exemplo 2: obter um pool elástico específico</span><span class="sxs-lookup"><span data-stu-id="4e907-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4e907-112">Esse comando obtém o pool elástico chamado ElasticPool0127 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="4e907-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="4e907-113">Exemplo 3: obter métricas para um pool de banco de dados elástico do Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4e907-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="4e907-114">Esse comando retorna métricas de um pool de banco de dados elástico do Azure SQL chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4e907-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="4e907-115">Exemplo 4: obter todos os pools elásticos usando a filtragem – ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="4e907-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4e907-116">Esse comando obtém todos os pools elásticos no servidor chamado Server01 que começam com "ElasticPool".</span><span class="sxs-lookup"><span data-stu-id="4e907-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="4e907-117">OS</span><span class="sxs-lookup"><span data-stu-id="4e907-117">PARAMETERS</span></span>

### <span data-ttu-id="4e907-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e907-118">-DefaultProfile</span></span>
<span data-ttu-id="4e907-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4e907-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e907-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4e907-120">-ElasticPoolName</span></span>
<span data-ttu-id="4e907-121">Especifica o nome do pool elástico que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4e907-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e907-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e907-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e907-123">Especifica o nome do grupo de recursos que contém o pool elástico que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4e907-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e907-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4e907-124">-ServerName</span></span>
<span data-ttu-id="4e907-125">Especifica o nome do servidor que contém o pool elástico que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4e907-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e907-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e907-126">CommonParameters</span></span>
<span data-ttu-id="4e907-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e907-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e907-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e907-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e907-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e907-129">INPUTS</span></span>

### <span data-ttu-id="4e907-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e907-130">System.String</span></span>

## <span data-ttu-id="4e907-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e907-131">OUTPUTS</span></span>

### <span data-ttu-id="4e907-132">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4e907-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4e907-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e907-133">NOTES</span></span>

## <span data-ttu-id="4e907-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e907-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e907-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4e907-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="4e907-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4e907-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="4e907-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4e907-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


