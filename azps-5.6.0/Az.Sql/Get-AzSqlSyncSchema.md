---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: e32f693b5f0bfc114f3ac40a4fc5761ec3a3ca70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891553"
---
# <span data-ttu-id="aaf26-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="aaf26-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="aaf26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf26-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf26-103">Retorna informações sobre o esquema de sincronização de um banco de dados membro ou de um banco de dados de hub.</span><span class="sxs-lookup"><span data-stu-id="aaf26-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="aaf26-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aaf26-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaf26-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aaf26-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf26-106">O cmdlet **Get-AzSqlSyncSchema** retorna informações sobre o esquema de sincronização de um banco de dados membro ou de um banco de dados de hub.</span><span class="sxs-lookup"><span data-stu-id="aaf26-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="aaf26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaf26-107">EXAMPLES</span></span>

### <span data-ttu-id="aaf26-108">Exemplo 1: Obter o esquema de sincronização para um banco de dados de hub</span><span class="sxs-lookup"><span data-stu-id="aaf26-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="aaf26-109">Este comando obtém o esquema de sincronização do banco de dados de hub na sincronização do grupo de sincronizaçãoGroup01.</span><span class="sxs-lookup"><span data-stu-id="aaf26-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="aaf26-110">Exemplo 2: obter o esquema de sincronização para um banco de dados de hub e expandir Tabelas</span><span class="sxs-lookup"><span data-stu-id="aaf26-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="aaf26-111">Este comando obtém o esquema de sincronização do banco de dados de hub no grupo de sincronização syncGroup01 e expanda a propriedade Tables.</span><span class="sxs-lookup"><span data-stu-id="aaf26-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="aaf26-112">Exemplo 3: Obter o esquema de sincronização para um banco de dados de membros</span><span class="sxs-lookup"><span data-stu-id="aaf26-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="aaf26-113">Este comando obtém o esquema de sincronização do banco de dados de membro na sincronização de membros de sincronizaçãoMember01.</span><span class="sxs-lookup"><span data-stu-id="aaf26-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="aaf26-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aaf26-114">PARAMETERS</span></span>

### <span data-ttu-id="aaf26-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aaf26-115">-DatabaseName</span></span>
<span data-ttu-id="aaf26-116">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="aaf26-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="aaf26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf26-117">-DefaultProfile</span></span>
<span data-ttu-id="aaf26-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aaf26-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaf26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf26-119">-ResourceGroupName</span></span>
<span data-ttu-id="aaf26-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aaf26-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="aaf26-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aaf26-121">-ServerName</span></span>
<span data-ttu-id="aaf26-122">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aaf26-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="aaf26-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf26-123">-SyncGroupName</span></span>
<span data-ttu-id="aaf26-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="aaf26-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf26-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="aaf26-125">-SyncMemberName</span></span>
<span data-ttu-id="aaf26-126">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="aaf26-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf26-127">CommonParameters</span></span>
<span data-ttu-id="aaf26-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf26-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaf26-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf26-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaf26-130">INPUTS</span></span>

### <span data-ttu-id="aaf26-131">System.String</span><span class="sxs-lookup"><span data-stu-id="aaf26-131">System.String</span></span>

## <span data-ttu-id="aaf26-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aaf26-132">OUTPUTS</span></span>

### <span data-ttu-id="aaf26-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="aaf26-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="aaf26-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="aaf26-134">NOTES</span></span>

## <span data-ttu-id="aaf26-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaf26-135">RELATED LINKS</span></span>
