---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 0343cddd12fdf1fe438ec2c4c9c3c5763719cd43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598916"
---
# <span data-ttu-id="6ee96-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="6ee96-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="6ee96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ee96-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee96-103">Retorna os logs de um grupo de sincronização de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee96-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6ee96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ee96-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ee96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ee96-105">DESCRIPTION</span></span>
<span data-ttu-id="6ee96-106">O cmdlet **Get-AzSqlSyncGroupLog** retorna os logs de um grupo de sincronização de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee96-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6ee96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ee96-107">EXAMPLES</span></span>

### <span data-ttu-id="6ee96-108">Exemplo 1: obter os logs de um grupo de sincronização do Azure SQL</span><span class="sxs-lookup"><span data-stu-id="6ee96-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="6ee96-109">Esse comando obtém os logs de um grupo Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="6ee96-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="6ee96-110">OS</span><span class="sxs-lookup"><span data-stu-id="6ee96-110">PARAMETERS</span></span>

### <span data-ttu-id="6ee96-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ee96-111">-DatabaseName</span></span>
<span data-ttu-id="6ee96-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee96-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee96-113">-DefaultProfile</span></span>
<span data-ttu-id="6ee96-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6ee96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ee96-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6ee96-115">-EndTime</span></span>
<span data-ttu-id="6ee96-116">A hora de término dos logs para consulta.</span><span class="sxs-lookup"><span data-stu-id="6ee96-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee96-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="6ee96-117">-LogLevel</span></span>
<span data-ttu-id="6ee96-118">O tipo dos logs a serem consultados.</span><span class="sxs-lookup"><span data-stu-id="6ee96-118">The type of the logs to query.</span></span>
<span data-ttu-id="6ee96-119">Os valores válidos são: ' error ', ' Warning ', ' Success ' e ' all'.</span><span class="sxs-lookup"><span data-stu-id="6ee96-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee96-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ee96-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ee96-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ee96-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6ee96-122">-ServerName</span></span>
<span data-ttu-id="6ee96-123">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6ee96-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6ee96-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6ee96-124">-StartTime</span></span>
<span data-ttu-id="6ee96-125">A hora de início do log para consulta.</span><span class="sxs-lookup"><span data-stu-id="6ee96-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee96-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee96-126">-SyncGroupName</span></span>
<span data-ttu-id="6ee96-127">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6ee96-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee96-128">CommonParameters</span></span>
<span data-ttu-id="6ee96-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee96-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ee96-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee96-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ee96-131">INPUTS</span></span>

### <span data-ttu-id="6ee96-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6ee96-132">System.String</span></span>

## <span data-ttu-id="6ee96-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ee96-133">OUTPUTS</span></span>

### <span data-ttu-id="6ee96-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="6ee96-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="6ee96-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ee96-135">NOTES</span></span>

## <span data-ttu-id="6ee96-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ee96-136">RELATED LINKS</span></span>
