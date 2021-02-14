---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110984"
---
# <span data-ttu-id="ccd08-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="ccd08-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="ccd08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccd08-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd08-103">Cria um objeto de entrada de banco de dados que contém informações sobre bancos de dados de origem e destino para migração.</span><span class="sxs-lookup"><span data-stu-id="ccd08-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="ccd08-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccd08-104">SYNTAX</span></span>

### <span data-ttu-id="ccd08-105">MigrateSqlServerSqlDb (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ccd08-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccd08-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="ccd08-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccd08-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccd08-107">DESCRIPTION</span></span>
<span data-ttu-id="ccd08-108">O New-AzDataMigrationSelectedDB cmdlet cria um objeto de informações de banco de dados que contém informações sobre bancos de dados de origem e destino, bem como os mapeamentos de tabela, para migração.</span><span class="sxs-lookup"><span data-stu-id="ccd08-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="ccd08-109">Esse cmdlet pode ser usado como um parâmetro com New-AzDataMigrationTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccd08-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="ccd08-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccd08-110">EXAMPLES</span></span>

### <span data-ttu-id="ccd08-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ccd08-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="ccd08-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ccd08-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="ccd08-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccd08-113">PARAMETERS</span></span>

### <span data-ttu-id="ccd08-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="ccd08-114">-BackupFileShare</span></span>
<span data-ttu-id="ccd08-115">Compartilhamento de arquivos onde os arquivos de banco de dados do servidor de origem desse banco de dados devem ser backup.</span><span class="sxs-lookup"><span data-stu-id="ccd08-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="ccd08-116">Use essa configuração para substituir informações de compartilhamento de arquivos para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ccd08-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="ccd08-117">Use o nome de domínio totalmente qualificado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ccd08-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="ccd08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd08-118">-DefaultProfile</span></span>
<span data-ttu-id="ccd08-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccd08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccd08-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="ccd08-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="ccd08-121">Definir o Banco de Dados como readonly antes da migração</span><span class="sxs-lookup"><span data-stu-id="ccd08-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="ccd08-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="ccd08-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="ccd08-123">Definir o tipo de migração para o SQL Server como SQL DB Migration.</span><span class="sxs-lookup"><span data-stu-id="ccd08-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="ccd08-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="ccd08-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="ccd08-125">Definir o tipo de migração para o SQL Server como SQL DB MI Migration.</span><span class="sxs-lookup"><span data-stu-id="ccd08-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="ccd08-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccd08-126">-SourceDatabaseName</span></span>
<span data-ttu-id="ccd08-127">O nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="ccd08-127">The name of the source database.</span></span>

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

### <span data-ttu-id="ccd08-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="ccd08-128">-TableMap</span></span>
<span data-ttu-id="ccd08-129">mapeamento de origem para tabelas de destino</span><span class="sxs-lookup"><span data-stu-id="ccd08-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="ccd08-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccd08-130">-TargetDatabaseName</span></span>
<span data-ttu-id="ccd08-131">O nome do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="ccd08-131">The name of the target database.</span></span>

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

### <span data-ttu-id="ccd08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd08-132">CommonParameters</span></span>
<span data-ttu-id="ccd08-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccd08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd08-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd08-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd08-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="ccd08-135">INPUTS</span></span>

### <span data-ttu-id="ccd08-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="ccd08-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="ccd08-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="ccd08-137">OUTPUTS</span></span>

### <span data-ttu-id="ccd08-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="ccd08-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="ccd08-139">Notas</span><span class="sxs-lookup"><span data-stu-id="ccd08-139">NOTES</span></span>

## <span data-ttu-id="ccd08-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccd08-140">RELATED LINKS</span></span>
