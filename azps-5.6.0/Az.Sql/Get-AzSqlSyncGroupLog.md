---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 40a269ab3d8378ce2f5a2024baee5bca18fe2134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890065"
---
# <span data-ttu-id="bcdad-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="bcdad-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="bcdad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcdad-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdad-103">Retorna os logs de um grupo de sincronização SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdad-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="bcdad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bcdad-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcdad-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bcdad-105">DESCRIPTION</span></span>
<span data-ttu-id="bcdad-106">O cmdlet **Get-AzSqlSyncGroupLog** retorna os logs de um Grupo de Sincronização de Banco de Dados do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="bcdad-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="bcdad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcdad-107">EXAMPLES</span></span>

### <span data-ttu-id="bcdad-108">Exemplo 1: Obter os logs de um grupo de sincronização do Azure SQL Sincronização</span><span class="sxs-lookup"><span data-stu-id="bcdad-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="bcdad-109">Este comando obtém os logs de um grupo de sincronização do Azure SQL Sincronização.</span><span class="sxs-lookup"><span data-stu-id="bcdad-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="bcdad-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bcdad-110">PARAMETERS</span></span>

### <span data-ttu-id="bcdad-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bcdad-111">-DatabaseName</span></span>
<span data-ttu-id="bcdad-112">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bcdad-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bcdad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdad-113">-DefaultProfile</span></span>
<span data-ttu-id="bcdad-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bcdad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcdad-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bcdad-115">-EndTime</span></span>
<span data-ttu-id="bcdad-116">A hora de término dos logs a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="bcdad-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="bcdad-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="bcdad-117">-LogLevel</span></span>
<span data-ttu-id="bcdad-118">O tipo de logs a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="bcdad-118">The type of the logs to query.</span></span>
<span data-ttu-id="bcdad-119">Os valores válidos são: 'Error', 'Warning', 'Success' e 'All'.</span><span class="sxs-lookup"><span data-stu-id="bcdad-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="bcdad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdad-120">-ResourceGroupName</span></span>
<span data-ttu-id="bcdad-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bcdad-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="bcdad-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bcdad-122">-ServerName</span></span>
<span data-ttu-id="bcdad-123">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bcdad-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bcdad-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bcdad-124">-StartTime</span></span>
<span data-ttu-id="bcdad-125">A hora de início dos logs para consulta.</span><span class="sxs-lookup"><span data-stu-id="bcdad-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="bcdad-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdad-126">-SyncGroupName</span></span>
<span data-ttu-id="bcdad-127">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="bcdad-127">The sync group name.</span></span>

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

### <span data-ttu-id="bcdad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdad-128">CommonParameters</span></span>
<span data-ttu-id="bcdad-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdad-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcdad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdad-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcdad-131">INPUTS</span></span>

### <span data-ttu-id="bcdad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bcdad-132">System.String</span></span>

## <span data-ttu-id="bcdad-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bcdad-133">OUTPUTS</span></span>

### <span data-ttu-id="bcdad-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="bcdad-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="bcdad-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="bcdad-135">NOTES</span></span>

## <span data-ttu-id="bcdad-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcdad-136">RELATED LINKS</span></span>
