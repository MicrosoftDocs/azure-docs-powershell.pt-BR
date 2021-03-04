---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: 6fa95473091afe991eac90ad87d7321b8401a8be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891208"
---
# <span data-ttu-id="aec0b-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="aec0b-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="aec0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec0b-102">SYNOPSIS</span></span>
<span data-ttu-id="aec0b-103">Cria um objeto de informações de banco de dados específico para o cenário de sincronização a ser usado para uma tarefa de migração.</span><span class="sxs-lookup"><span data-stu-id="aec0b-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="aec0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aec0b-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aec0b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aec0b-105">DESCRIPTION</span></span>

<span data-ttu-id="aec0b-106">O New-AzDataMigrationSyncSelectedDB cmdlet cria um objeto de informações de banco de dados específico para o cenário de sincronização que contém informações sobre bancos de dados de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="aec0b-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="aec0b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aec0b-107">EXAMPLES</span></span>

### <span data-ttu-id="aec0b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aec0b-108">Example 1</span></span>
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

<span data-ttu-id="aec0b-109">Este exemplo cria um objeto de metadados de banco de dados que descreve as configurações de migração para $DatabaseName para o banco de dados $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="aec0b-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="aec0b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aec0b-110">PARAMETERS</span></span>

### <span data-ttu-id="aec0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec0b-111">-DefaultProfile</span></span>
<span data-ttu-id="aec0b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aec0b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec0b-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="aec0b-113">-MigrationSetting</span></span>
<span data-ttu-id="aec0b-114">Configurações de migração que ajustam o comportamento de migração</span><span class="sxs-lookup"><span data-stu-id="aec0b-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="aec0b-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="aec0b-115">-SchemaName</span></span>
<span data-ttu-id="aec0b-116">Nome do esquema a ser migrado</span><span class="sxs-lookup"><span data-stu-id="aec0b-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="aec0b-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="aec0b-117">-SourceDatabaseName</span></span>
<span data-ttu-id="aec0b-118">O nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="aec0b-118">The name of the source database.</span></span>

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

### <span data-ttu-id="aec0b-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="aec0b-119">-SourceSetting</span></span>
<span data-ttu-id="aec0b-120">Configurações de origem para ajustar o comportamento de migração do ponto de extremidade de origem</span><span class="sxs-lookup"><span data-stu-id="aec0b-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="aec0b-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="aec0b-121">-TableMap</span></span>
<span data-ttu-id="aec0b-122">Mapeamento de tabelas de origem para destino</span><span class="sxs-lookup"><span data-stu-id="aec0b-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="aec0b-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="aec0b-123">-TargetDatabaseName</span></span>
<span data-ttu-id="aec0b-124">O nome do banco de dados de destino</span><span class="sxs-lookup"><span data-stu-id="aec0b-124">The name of the target database</span></span>

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

### <span data-ttu-id="aec0b-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="aec0b-125">-TargetSetting</span></span>
<span data-ttu-id="aec0b-126">Configurações de destino para ajustar o comportamento de migração do ponto de extremidade de destino</span><span class="sxs-lookup"><span data-stu-id="aec0b-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="aec0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec0b-127">CommonParameters</span></span>
<span data-ttu-id="aec0b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec0b-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec0b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec0b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aec0b-130">INPUTS</span></span>

### <span data-ttu-id="aec0b-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aec0b-131">None</span></span>

## <span data-ttu-id="aec0b-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aec0b-132">OUTPUTS</span></span>

### <span data-ttu-id="aec0b-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="aec0b-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="aec0b-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="aec0b-134">NOTES</span></span>

## <span data-ttu-id="aec0b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aec0b-135">RELATED LINKS</span></span>
