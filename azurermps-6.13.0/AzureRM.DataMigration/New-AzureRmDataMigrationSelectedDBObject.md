---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
ms.openlocfilehash: d8303dadef33944addf63323e57727ef85acce6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602110"
---
# <span data-ttu-id="4fdea-101">New-AzureRmDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="4fdea-101">New-AzureRmDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="4fdea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fdea-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdea-103">Cria um objeto de entrada de banco de dados que contém informações sobre bancos de dados de origem e de destino para migração.</span><span class="sxs-lookup"><span data-stu-id="4fdea-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fdea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fdea-104">SYNTAX</span></span>

### <span data-ttu-id="4fdea-105">MigrateSqlServerSqlDb (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fdea-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdea-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4fdea-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fdea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fdea-107">DESCRIPTION</span></span>
<span data-ttu-id="4fdea-108">O cmdlet New-AzureRmDataMigrationSelectedDB cria um objeto de informações de banco de dados que contém informações sobre bancos de dados de origem e de destino, bem como os mapeamentos de tabela, para migração.</span><span class="sxs-lookup"><span data-stu-id="4fdea-108">The New-AzureRmDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="4fdea-109">Esse cmdlet pode ser usado como um parâmetro com o cmdlet New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="4fdea-109">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="4fdea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fdea-110">EXAMPLES</span></span>

### <span data-ttu-id="4fdea-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fdea-111">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```


### <span data-ttu-id="4fdea-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4fdea-112">Example 2</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```


## <span data-ttu-id="4fdea-113">OS</span><span class="sxs-lookup"><span data-stu-id="4fdea-113">PARAMETERS</span></span>

### <span data-ttu-id="4fdea-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="4fdea-114">-BackupFileShare</span></span>
<span data-ttu-id="4fdea-115">Compartilhamento de arquivos onde deve ser feito o backup dos arquivos de banco de dados do servidor de origem para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4fdea-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="4fdea-116">Use essa configuração para substituir informações de compartilhamento de arquivos para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4fdea-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="4fdea-117">Use o nome de domínio totalmente qualificado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4fdea-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="4fdea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdea-118">-DefaultProfile</span></span>
<span data-ttu-id="4fdea-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fdea-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="4fdea-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="4fdea-121">Definir o banco de dados como ReadOnly antes da migração</span><span class="sxs-lookup"><span data-stu-id="4fdea-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="4fdea-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="4fdea-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="4fdea-123">Defina o tipo de migração como SQL Server para migração do SQL DB.</span><span class="sxs-lookup"><span data-stu-id="4fdea-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="4fdea-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4fdea-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="4fdea-125">Defina o tipo de migração como SQL Server para a migração MI do SQL DB.</span><span class="sxs-lookup"><span data-stu-id="4fdea-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="4fdea-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4fdea-126">-SourceDatabaseName</span></span>
<span data-ttu-id="4fdea-127">O nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="4fdea-127">The name of the source database.</span></span>

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

### <span data-ttu-id="4fdea-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="4fdea-128">-TableMap</span></span>
<span data-ttu-id="4fdea-129">mapeamento de origem para tabelas de destino</span><span class="sxs-lookup"><span data-stu-id="4fdea-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="4fdea-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4fdea-130">-TargetDatabaseName</span></span>
<span data-ttu-id="4fdea-131">O nome do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="4fdea-131">The name of the target database.</span></span>

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

### <span data-ttu-id="4fdea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdea-132">CommonParameters</span></span>
<span data-ttu-id="4fdea-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdea-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fdea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdea-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fdea-135">INPUTS</span></span>

### <span data-ttu-id="4fdea-136">Microsoft. Azure. Management. datamigration. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="4fdea-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="4fdea-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fdea-137">OUTPUTS</span></span>

### <span data-ttu-id="4fdea-138">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="4fdea-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="4fdea-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fdea-139">NOTES</span></span>

## <span data-ttu-id="4fdea-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fdea-140">RELATED LINKS</span></span>
