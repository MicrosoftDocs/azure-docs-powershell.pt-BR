---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 924e00578383e103d1451e311d027edd02752496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427756"
---
# <span data-ttu-id="3b6de-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="3b6de-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="3b6de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b6de-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6de-103">Retorna os logs de um grupo de sincronização de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6de-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b6de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b6de-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b6de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b6de-105">DESCRIPTION</span></span>
<span data-ttu-id="3b6de-106">O cmdlet **Get-AzureRmSqlSyncGroupLog** retorna os logs de um grupo de sincronização de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6de-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3b6de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b6de-107">EXAMPLES</span></span>

### <span data-ttu-id="3b6de-108">Exemplo 1: obter os logs de um grupo de sincronização do Azure SQL</span><span class="sxs-lookup"><span data-stu-id="3b6de-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="3b6de-109">Esse comando obtém os logs de um grupo Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="3b6de-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="3b6de-110">OS</span><span class="sxs-lookup"><span data-stu-id="3b6de-110">PARAMETERS</span></span>

### <span data-ttu-id="3b6de-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b6de-111">-DatabaseName</span></span>
<span data-ttu-id="3b6de-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6de-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3b6de-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3b6de-113">-EndTime</span></span>
<span data-ttu-id="3b6de-114">A hora de término dos logs para consulta.</span><span class="sxs-lookup"><span data-stu-id="3b6de-114">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="3b6de-115">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="3b6de-115">-LogLevel</span></span>
<span data-ttu-id="3b6de-116">O tipo dos logs a serem consultados.</span><span class="sxs-lookup"><span data-stu-id="3b6de-116">The type of the logs to query.</span></span>
<span data-ttu-id="3b6de-117">Os valores válidos são: ' error ', ' Warning ', ' Success ' e ' all'.</span><span class="sxs-lookup"><span data-stu-id="3b6de-117">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="3b6de-118">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6de-118">-SyncGroupName</span></span>
<span data-ttu-id="3b6de-119">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="3b6de-119">The sync group name.</span></span>

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

### <span data-ttu-id="3b6de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6de-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b6de-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b6de-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="3b6de-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3b6de-122">-ServerName</span></span>
<span data-ttu-id="3b6de-123">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b6de-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3b6de-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3b6de-124">-StartTime</span></span>
<span data-ttu-id="3b6de-125">A hora de início do log para consulta.</span><span class="sxs-lookup"><span data-stu-id="3b6de-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="3b6de-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6de-126">-DefaultProfile</span></span>
<span data-ttu-id="3b6de-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6de-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6de-128">CommonParameters</span></span>
<span data-ttu-id="3b6de-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b6de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6de-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b6de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6de-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b6de-131">INPUTS</span></span>

## <span data-ttu-id="3b6de-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b6de-132">OUTPUTS</span></span>

### <span data-ttu-id="3b6de-133">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="3b6de-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="3b6de-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b6de-134">NOTES</span></span>

## <span data-ttu-id="3b6de-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b6de-135">RELATED LINKS</span></span>

