---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: c6e417ade1e411eaaa0b86f8f69ac6c17f228e91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891386"
---
# <span data-ttu-id="1bcdd-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="1bcdd-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="1bcdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bcdd-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcdd-103">Cria um objeto de entrada de banco de dados que contém informações sobre bancos de dados de origem e destino para migração.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="1bcdd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1bcdd-104">SYNTAX</span></span>

### <span data-ttu-id="1bcdd-105">MigrateSqlServerSqlDb (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1bcdd-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bcdd-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="1bcdd-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bcdd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1bcdd-107">DESCRIPTION</span></span>
<span data-ttu-id="1bcdd-108">O New-AzDataMigrationSelectedDB cmdlet cria um objeto de informações de banco de dados que contém informações sobre bancos de dados de origem e destino, bem como os mapeamentos de tabela, para migração.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="1bcdd-109">Esse cmdlet pode ser usado como um parâmetro com o cmdlet New-AzDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="1bcdd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bcdd-110">EXAMPLES</span></span>

### <span data-ttu-id="1bcdd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bcdd-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="1bcdd-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1bcdd-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="1bcdd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1bcdd-113">PARAMETERS</span></span>

### <span data-ttu-id="1bcdd-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="1bcdd-114">-BackupFileShare</span></span>
<span data-ttu-id="1bcdd-115">Compartilhamento de arquivos onde os arquivos de banco de dados do servidor de origem desse banco de dados devem ser backup.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="1bcdd-116">Use essa configuração para substituir informações de compartilhamento de arquivos para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="1bcdd-117">Use o nome de domínio totalmente qualificado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bcdd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcdd-118">-DefaultProfile</span></span>
<span data-ttu-id="1bcdd-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bcdd-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="1bcdd-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="1bcdd-121">Definir Database como readonly antes da migração</span><span class="sxs-lookup"><span data-stu-id="1bcdd-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bcdd-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="1bcdd-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="1bcdd-123">De definir o tipo de migração como SQL Server para SQL DB Migração.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bcdd-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="1bcdd-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="1bcdd-125">De definir o tipo de migração como SQL Server para SQL DE DB MI Migração.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bcdd-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1bcdd-126">-SourceDatabaseName</span></span>
<span data-ttu-id="1bcdd-127">O nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-127">The name of the source database.</span></span>

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

### <span data-ttu-id="1bcdd-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="1bcdd-128">-TableMap</span></span>
<span data-ttu-id="1bcdd-129">mapeamento de origem para tabelas de destino</span><span class="sxs-lookup"><span data-stu-id="1bcdd-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bcdd-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1bcdd-130">-TargetDatabaseName</span></span>
<span data-ttu-id="1bcdd-131">O nome do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-131">The name of the target database.</span></span>

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

### <span data-ttu-id="1bcdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcdd-132">CommonParameters</span></span>
<span data-ttu-id="1bcdd-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bcdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcdd-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bcdd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcdd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bcdd-135">INPUTS</span></span>

### <span data-ttu-id="1bcdd-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="1bcdd-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="1bcdd-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1bcdd-137">OUTPUTS</span></span>

### <span data-ttu-id="1bcdd-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="1bcdd-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="1bcdd-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="1bcdd-139">NOTES</span></span>

## <span data-ttu-id="1bcdd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bcdd-140">RELATED LINKS</span></span>
