---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115853"
---
# <span data-ttu-id="52c08-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="52c08-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="52c08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52c08-102">SYNOPSIS</span></span>
<span data-ttu-id="52c08-103">Cria configuração de banco de dados para migração para a migração mongoDb</span><span class="sxs-lookup"><span data-stu-id="52c08-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="52c08-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52c08-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="52c08-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="52c08-105">DESCRIPTION</span></span>
<span data-ttu-id="52c08-106">O New-AzDataMigrationMongoDbDatabaseSetting cmdlet cria o objeto de configuração de migração que especifica o comportamento de produtividade e exclusão.</span><span class="sxs-lookup"><span data-stu-id="52c08-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="52c08-107">A saída é um par de valores-chave com o nome da coleção e o valor da configuração, que pode ser usado para invocar a tarefa de migração.</span><span class="sxs-lookup"><span data-stu-id="52c08-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="52c08-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52c08-108">EXAMPLES</span></span>

### <span data-ttu-id="52c08-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52c08-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="52c08-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52c08-110">PARAMETERS</span></span>

### <span data-ttu-id="52c08-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="52c08-111">-Name</span></span>
<span data-ttu-id="52c08-112">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="52c08-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="52c08-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="52c08-113">-TargetRequestUnit</span></span>
<span data-ttu-id="52c08-114">O valor de unidade de solicitação de nível de banco de dados dedicado.</span><span class="sxs-lookup"><span data-stu-id="52c08-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="52c08-115">Se não estiver definida, essa coleção usará o RU de banco de dados compartilhado.</span><span class="sxs-lookup"><span data-stu-id="52c08-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c08-116">-Coleções</span><span class="sxs-lookup"><span data-stu-id="52c08-116">-Collections</span></span>
<span data-ttu-id="52c08-117">A matriz de objetos de configuração da coleção MongoDb retornados New-AzureRmDmsMongoDbDatabaseSetting chamada.</span><span class="sxs-lookup"><span data-stu-id="52c08-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c08-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c08-118">CommonParameters</span></span>
<span data-ttu-id="52c08-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c08-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c08-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52c08-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c08-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="52c08-121">INPUTS</span></span>

### <span data-ttu-id="52c08-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="52c08-122">None</span></span>

## <span data-ttu-id="52c08-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="52c08-123">OUTPUTS</span></span>

### <span data-ttu-id="52c08-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="52c08-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="52c08-125">Notas</span><span class="sxs-lookup"><span data-stu-id="52c08-125">NOTES</span></span>

## <span data-ttu-id="52c08-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52c08-126">RELATED LINKS</span></span>
