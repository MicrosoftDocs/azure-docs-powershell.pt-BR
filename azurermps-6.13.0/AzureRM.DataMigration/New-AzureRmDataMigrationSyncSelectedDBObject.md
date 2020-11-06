---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: fc400c9eeb64acfa081d5a60a5e65089f415817b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610081"
---
# <span data-ttu-id="7569c-101">New-AzureRmDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="7569c-101">New-AzureRmDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="7569c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7569c-102">SYNOPSIS</span></span>
<span data-ttu-id="7569c-103">Cria um objeto de informações de banco de dados específico para o cenário de sincronização a ser usado para uma tarefa de migração.</span><span class="sxs-lookup"><span data-stu-id="7569c-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7569c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7569c-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String>
 -TableMap <Hashtable> [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>]
 [-TargetSetting <Hashtable>] -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7569c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7569c-105">DESCRIPTION</span></span>

<span data-ttu-id="7569c-106">O cmdlet New-AzureRmDataMigrationSyncSelectedDB cria um objeto de informações de banco de dados específico para o cenário de sincronização, que contém informações sobre bancos de dados de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="7569c-106">The New-AzureRmDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="7569c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7569c-107">EXAMPLES</span></span>

### <span data-ttu-id="7569c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7569c-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzureRmDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="7569c-109">Este exemplo cria um objeto de metadados de banco de dados descrevendo as configurações de migração de $DatabaseName para o banco de dados $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="7569c-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="7569c-110">OS</span><span class="sxs-lookup"><span data-stu-id="7569c-110">PARAMETERS</span></span>

### <span data-ttu-id="7569c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7569c-111">-DefaultProfile</span></span>
<span data-ttu-id="7569c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7569c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7569c-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="7569c-113">-MigrationSetting</span></span>
<span data-ttu-id="7569c-114">Configurações de migração que ajustam o comportamento de migração</span><span class="sxs-lookup"><span data-stu-id="7569c-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="7569c-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7569c-115">-SchemaName</span></span>
<span data-ttu-id="7569c-116">Nome do esquema a ser migrado</span><span class="sxs-lookup"><span data-stu-id="7569c-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="7569c-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7569c-117">-SourceDatabaseName</span></span>
<span data-ttu-id="7569c-118">O nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="7569c-118">The name of the source database.</span></span>

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

### <span data-ttu-id="7569c-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="7569c-119">-SourceSetting</span></span>
<span data-ttu-id="7569c-120">Configurações de origem para ajustar o comportamento de migração de ponto de extremidade de origem</span><span class="sxs-lookup"><span data-stu-id="7569c-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="7569c-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="7569c-121">-TableMap</span></span>
<span data-ttu-id="7569c-122">Mapeamento de origem para tabelas de destino</span><span class="sxs-lookup"><span data-stu-id="7569c-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="7569c-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7569c-123">-TargetDatabaseName</span></span>
<span data-ttu-id="7569c-124">O nome do banco de dados de destino</span><span class="sxs-lookup"><span data-stu-id="7569c-124">The name of the target database</span></span>

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

### <span data-ttu-id="7569c-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="7569c-125">-TargetSetting</span></span>
<span data-ttu-id="7569c-126">Configurações de destino para ajustar o comportamento de migração de ponto de extremidade de destino</span><span class="sxs-lookup"><span data-stu-id="7569c-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="7569c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7569c-127">CommonParameters</span></span>
<span data-ttu-id="7569c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7569c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7569c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7569c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7569c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7569c-130">INPUTS</span></span>

### <span data-ttu-id="7569c-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7569c-131">None</span></span>

## <span data-ttu-id="7569c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7569c-132">OUTPUTS</span></span>

### <span data-ttu-id="7569c-133">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="7569c-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="7569c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7569c-134">NOTES</span></span>

## <span data-ttu-id="7569c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7569c-135">RELATED LINKS</span></span>
