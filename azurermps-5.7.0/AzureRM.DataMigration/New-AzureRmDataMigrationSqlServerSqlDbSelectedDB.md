---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429808"
---
# <span data-ttu-id="cf68f-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="cf68f-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="cf68f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf68f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf68f-103">Cria um objeto MigrateSqlServerSqlDbDatabaseInput que contém informações sobre bancos de dados de origem e de destino para migração.</span><span class="sxs-lookup"><span data-stu-id="cf68f-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf68f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf68f-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="cf68f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf68f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf68f-106">O cmdlet New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cria um objeto MigrateSqlServerSqlDbDatabaseInput que contém informações sobre bancos de dados de origem e de destino, bem como os mapeamentos de tabela, para migração.</span><span class="sxs-lookup"><span data-stu-id="cf68f-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="cf68f-107">Esse cmdlet pode ser usado como um parâmetro com o cmdlet New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="cf68f-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="cf68f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf68f-108">EXAMPLES</span></span>

### <span data-ttu-id="cf68f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf68f-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="cf68f-110">O exemplo acima cria o objeto MigrateSqlServerSqlDbDatabaseInput para migrar o banco de dados **AdventureWorks2016** para um banco de dados do SQL Azure com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="cf68f-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="cf68f-111">OS</span><span class="sxs-lookup"><span data-stu-id="cf68f-111">PARAMETERS</span></span>

### <span data-ttu-id="cf68f-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf68f-112">-Confirm</span></span>
<span data-ttu-id="cf68f-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf68f-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf68f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf68f-114">-DefaultProfile</span></span>
<span data-ttu-id="cf68f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf68f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf68f-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="cf68f-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="cf68f-117">Definir o banco de dados como ReadOnly antes da migração</span><span class="sxs-lookup"><span data-stu-id="cf68f-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf68f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf68f-118">-Name</span></span>
<span data-ttu-id="cf68f-119">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cf68f-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf68f-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="cf68f-120">-TableMap</span></span>
<span data-ttu-id="cf68f-121">mapeamento de origem para tabelas de destino</span><span class="sxs-lookup"><span data-stu-id="cf68f-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf68f-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf68f-122">-TargetDatabaseName</span></span>
<span data-ttu-id="cf68f-123">O nome do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="cf68f-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="cf68f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf68f-124">INPUTS</span></span>

### <span data-ttu-id="cf68f-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cf68f-125">None</span></span>


## <span data-ttu-id="cf68f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf68f-126">OUTPUTS</span></span>

### <span data-ttu-id="cf68f-127">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="cf68f-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="cf68f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf68f-128">NOTES</span></span>

## <span data-ttu-id="cf68f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf68f-129">RELATED LINKS</span></span>


