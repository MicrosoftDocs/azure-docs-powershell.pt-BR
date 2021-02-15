---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111935"
---
# <span data-ttu-id="8041a-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="8041a-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="8041a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8041a-102">SYNOPSIS</span></span>
<span data-ttu-id="8041a-103">Cria um objeto de informações de banco de dados específico para o cenário de sincronização a ser usado para uma tarefa de migração.</span><span class="sxs-lookup"><span data-stu-id="8041a-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="8041a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8041a-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8041a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8041a-105">DESCRIPTION</span></span>

<span data-ttu-id="8041a-106">O New-AzDataMigrationSyncSelectedDB cmdlet cria um objeto de informações de banco de dados específico para o cenário de sincronização que contém informações sobre bancos de dados de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="8041a-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="8041a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8041a-107">EXAMPLES</span></span>

### <span data-ttu-id="8041a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8041a-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="8041a-109">Este exemplo cria um objeto de metadados de banco de dados que descreve as configurações de migração $DatabaseName para o banco de dados $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="8041a-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="8041a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8041a-110">PARAMETERS</span></span>

### <span data-ttu-id="8041a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8041a-111">-DefaultProfile</span></span>
<span data-ttu-id="8041a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8041a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8041a-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="8041a-113">-MigrationSetting</span></span>
<span data-ttu-id="8041a-114">Configurações de migração que ajustam o comportamento de migração</span><span class="sxs-lookup"><span data-stu-id="8041a-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="8041a-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8041a-115">-SchemaName</span></span>
<span data-ttu-id="8041a-116">Nome do esquema a ser migrado</span><span class="sxs-lookup"><span data-stu-id="8041a-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="8041a-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8041a-117">-SourceDatabaseName</span></span>
<span data-ttu-id="8041a-118">O nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="8041a-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8041a-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="8041a-119">-SourceSetting</span></span>
<span data-ttu-id="8041a-120">Configurações de origem para ajustar o comportamento de migração do ponto de extremidade de origem</span><span class="sxs-lookup"><span data-stu-id="8041a-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="8041a-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="8041a-121">-TableMap</span></span>
<span data-ttu-id="8041a-122">Mapeamento de origem para tabelas de destino</span><span class="sxs-lookup"><span data-stu-id="8041a-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8041a-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8041a-123">-TargetDatabaseName</span></span>
<span data-ttu-id="8041a-124">O nome do banco de dados de destino</span><span class="sxs-lookup"><span data-stu-id="8041a-124">The name of the target database</span></span>

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

### <span data-ttu-id="8041a-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="8041a-125">-TargetSetting</span></span>
<span data-ttu-id="8041a-126">Configurações de destino para ajustar o comportamento de migração do ponto de extremidade de destino</span><span class="sxs-lookup"><span data-stu-id="8041a-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="8041a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8041a-127">CommonParameters</span></span>
<span data-ttu-id="8041a-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8041a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8041a-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8041a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8041a-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="8041a-130">INPUTS</span></span>

### <span data-ttu-id="8041a-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8041a-131">None</span></span>

## <span data-ttu-id="8041a-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="8041a-132">OUTPUTS</span></span>

### <span data-ttu-id="8041a-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="8041a-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="8041a-134">Notas</span><span class="sxs-lookup"><span data-stu-id="8041a-134">NOTES</span></span>

## <span data-ttu-id="8041a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8041a-135">RELATED LINKS</span></span>
