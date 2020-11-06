---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: ef66de2b12cf0ea723540c392a296d2d1c482505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427753"
---
# <span data-ttu-id="da8ff-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="da8ff-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="da8ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="da8ff-103">Retorna informações sobre o esquema de sincronização de um banco de dados de membro ou de um banco de dados Hub.</span><span class="sxs-lookup"><span data-stu-id="da8ff-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da8ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da8ff-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da8ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da8ff-105">DESCRIPTION</span></span>
<span data-ttu-id="da8ff-106">O cmdlet **Get-AzureRmSqlSyncSchema** retorna informações sobre o esquema de sincronização de um banco de dados de membro ou um banco de dados Hub.</span><span class="sxs-lookup"><span data-stu-id="da8ff-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="da8ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da8ff-107">EXAMPLES</span></span>

### <span data-ttu-id="da8ff-108">Exemplo 1,1: obter o esquema de sincronização para um banco de dados Hub</span><span class="sxs-lookup"><span data-stu-id="da8ff-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="da8ff-109">Esse comando obtém o esquema de sincronização para o banco de dados de Hub no grupo de sincronização syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="da8ff-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="da8ff-110">Exemplo 1,2: obter o esquema de sincronização para um banco de dados Hub e expandir tabelas</span><span class="sxs-lookup"><span data-stu-id="da8ff-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="da8ff-111">Esse comando obtém o esquema de sincronização para o banco de dados de Hub no grupo de sincronização syncGroup01 e expanda a propriedade Tables.</span><span class="sxs-lookup"><span data-stu-id="da8ff-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="da8ff-112">Exemplo 2: obter o esquema de sincronização para um banco de dados membro</span><span class="sxs-lookup"><span data-stu-id="da8ff-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="da8ff-113">Esse comando obtém o esquema de sincronização para o banco de dados membro na syncMember01 do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="da8ff-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="da8ff-114">OS</span><span class="sxs-lookup"><span data-stu-id="da8ff-114">PARAMETERS</span></span>

### <span data-ttu-id="da8ff-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da8ff-115">-DatabaseName</span></span>
<span data-ttu-id="da8ff-116">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="da8ff-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="da8ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da8ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="da8ff-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da8ff-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="da8ff-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="da8ff-119">-ServerName</span></span>
<span data-ttu-id="da8ff-120">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da8ff-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="da8ff-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="da8ff-121">-SyncGroupName</span></span>
<span data-ttu-id="da8ff-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="da8ff-122">The sync group name.</span></span>

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

### <span data-ttu-id="da8ff-123">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="da8ff-123">-SyncMemberName</span></span>
<span data-ttu-id="da8ff-124">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="da8ff-124">The sync member name.</span></span>

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

### <span data-ttu-id="da8ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8ff-125">-DefaultProfile</span></span>
<span data-ttu-id="da8ff-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da8ff-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da8ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8ff-127">CommonParameters</span></span>
<span data-ttu-id="da8ff-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da8ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8ff-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da8ff-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8ff-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da8ff-130">INPUTS</span></span>

## <span data-ttu-id="da8ff-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da8ff-131">OUTPUTS</span></span>

### <span data-ttu-id="da8ff-132">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="da8ff-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="da8ff-133">Tabelas: Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncFullSchemaTableModel</span><span class="sxs-lookup"><span data-stu-id="da8ff-133">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="da8ff-134">Columns: Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncFullSchemaColumnModel</span><span class="sxs-lookup"><span data-stu-id="da8ff-134">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="da8ff-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da8ff-135">NOTES</span></span>

## <span data-ttu-id="da8ff-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da8ff-136">RELATED LINKS</span></span>

