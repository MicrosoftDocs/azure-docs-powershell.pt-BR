---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111325"
---
# <span data-ttu-id="f9985-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="f9985-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="f9985-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9985-102">SYNOPSIS</span></span>
<span data-ttu-id="f9985-103">Retorna os logs de um Grupo de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9985-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f9985-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9985-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9985-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9985-105">DESCRIPTION</span></span>
<span data-ttu-id="f9985-106">O cmdlet **Get-AzSqlSyncGroupLog** retorna os logs de um Grupo de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9985-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f9985-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9985-107">EXAMPLES</span></span>

### <span data-ttu-id="f9985-108">Exemplo 1: Obter os logs de um Grupo de Sincronização SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9985-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="f9985-109">Esse comando obtém os logs de um Grupo de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9985-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="f9985-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9985-110">PARAMETERS</span></span>

### <span data-ttu-id="f9985-111">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="f9985-111">-DatabaseName</span></span>
<span data-ttu-id="f9985-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9985-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f9985-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9985-113">-DefaultProfile</span></span>
<span data-ttu-id="f9985-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f9985-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9985-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f9985-115">-EndTime</span></span>
<span data-ttu-id="f9985-116">A hora de término dos logs para consulta.</span><span class="sxs-lookup"><span data-stu-id="f9985-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="f9985-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="f9985-117">-LogLevel</span></span>
<span data-ttu-id="f9985-118">O tipo de logs para consulta.</span><span class="sxs-lookup"><span data-stu-id="f9985-118">The type of the logs to query.</span></span>
<span data-ttu-id="f9985-119">Os valores válidos são: 'Erro', 'Aviso', 'Sucesso' e 'Tudo'.</span><span class="sxs-lookup"><span data-stu-id="f9985-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="f9985-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9985-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9985-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9985-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9985-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9985-122">-ServerName</span></span>
<span data-ttu-id="f9985-123">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9985-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f9985-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f9985-124">-StartTime</span></span>
<span data-ttu-id="f9985-125">A hora de início dos logs para consulta.</span><span class="sxs-lookup"><span data-stu-id="f9985-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="f9985-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f9985-126">-SyncGroupName</span></span>
<span data-ttu-id="f9985-127">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f9985-127">The sync group name.</span></span>

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

### <span data-ttu-id="f9985-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9985-128">CommonParameters</span></span>
<span data-ttu-id="f9985-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9985-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9985-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9985-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9985-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9985-131">INPUTS</span></span>

### <span data-ttu-id="f9985-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9985-132">System.String</span></span>

## <span data-ttu-id="f9985-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9985-133">OUTPUTS</span></span>

### <span data-ttu-id="f9985-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="f9985-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="f9985-135">Notas</span><span class="sxs-lookup"><span data-stu-id="f9985-135">NOTES</span></span>

## <span data-ttu-id="f9985-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9985-136">RELATED LINKS</span></span>
