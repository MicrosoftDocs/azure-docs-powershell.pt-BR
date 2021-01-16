---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257405"
---
# <span data-ttu-id="a09fc-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="a09fc-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="a09fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a09fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a09fc-103">Retorna informações sobre o esquema de sincronização de um banco de dados de membro ou de um banco de dados Hub.</span><span class="sxs-lookup"><span data-stu-id="a09fc-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="a09fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a09fc-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a09fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a09fc-105">DESCRIPTION</span></span>
<span data-ttu-id="a09fc-106">O cmdlet **Get-AzSqlSyncSchema** retorna informações sobre o esquema de sincronização de um banco de dados de membro ou um banco de dados Hub.</span><span class="sxs-lookup"><span data-stu-id="a09fc-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="a09fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a09fc-107">EXAMPLES</span></span>

### <span data-ttu-id="a09fc-108">Exemplo 1: obter o esquema de sincronização para um banco de dados Hub</span><span class="sxs-lookup"><span data-stu-id="a09fc-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="a09fc-109">Esse comando obtém o esquema de sincronização para o banco de dados de Hub no grupo de sincronização syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="a09fc-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="a09fc-110">Exemplo 2: obter o esquema de sincronização para um banco de dados Hub e expandir tabelas</span><span class="sxs-lookup"><span data-stu-id="a09fc-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
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

<span data-ttu-id="a09fc-111">Esse comando obtém o esquema de sincronização para o banco de dados de Hub no grupo de sincronização syncGroup01 e expanda a propriedade Tables.</span><span class="sxs-lookup"><span data-stu-id="a09fc-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="a09fc-112">Exemplo 3: obter o esquema de sincronização para um banco de dados membro</span><span class="sxs-lookup"><span data-stu-id="a09fc-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="a09fc-113">Esse comando obtém o esquema de sincronização para o banco de dados membro na syncMember01 do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a09fc-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="a09fc-114">OS</span><span class="sxs-lookup"><span data-stu-id="a09fc-114">PARAMETERS</span></span>

### <span data-ttu-id="a09fc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a09fc-115">-DatabaseName</span></span>
<span data-ttu-id="a09fc-116">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a09fc-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a09fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09fc-117">-DefaultProfile</span></span>
<span data-ttu-id="a09fc-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a09fc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a09fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="a09fc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a09fc-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a09fc-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a09fc-121">-ServerName</span></span>
<span data-ttu-id="a09fc-122">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a09fc-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a09fc-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a09fc-123">-SyncGroupName</span></span>
<span data-ttu-id="a09fc-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a09fc-124">The sync group name.</span></span>

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

### <span data-ttu-id="a09fc-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="a09fc-125">-SyncMemberName</span></span>
<span data-ttu-id="a09fc-126">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a09fc-126">The sync member name.</span></span>

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

### <span data-ttu-id="a09fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09fc-127">CommonParameters</span></span>
<span data-ttu-id="a09fc-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09fc-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a09fc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09fc-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a09fc-130">INPUTS</span></span>

### <span data-ttu-id="a09fc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a09fc-131">System.String</span></span>

## <span data-ttu-id="a09fc-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a09fc-132">OUTPUTS</span></span>

### <span data-ttu-id="a09fc-133">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="a09fc-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="a09fc-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a09fc-134">NOTES</span></span>

## <span data-ttu-id="a09fc-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a09fc-135">RELATED LINKS</span></span>
