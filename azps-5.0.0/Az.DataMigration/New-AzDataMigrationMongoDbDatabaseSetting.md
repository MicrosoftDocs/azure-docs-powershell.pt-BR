---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280763"
---
# <span data-ttu-id="afa74-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="afa74-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="afa74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afa74-102">SYNOPSIS</span></span>
<span data-ttu-id="afa74-103">Cria uma configuração de banco de dados para migração para a migração do mongoDb</span><span class="sxs-lookup"><span data-stu-id="afa74-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="afa74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afa74-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="afa74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afa74-105">DESCRIPTION</span></span>
<span data-ttu-id="afa74-106">O cmdlet New-AzDataMigrationMongoDbDatabaseSetting cria o objeto de configuração de migração que especifica a taxa de transferência e o comportamento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="afa74-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="afa74-107">A saída é um par chave de valor com nome da coleção e valor da configuração, que pode ser usado na invocação da tarefa de migração.</span><span class="sxs-lookup"><span data-stu-id="afa74-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="afa74-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afa74-108">EXAMPLES</span></span>

### <span data-ttu-id="afa74-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afa74-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="afa74-110">OS</span><span class="sxs-lookup"><span data-stu-id="afa74-110">PARAMETERS</span></span>

### <span data-ttu-id="afa74-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="afa74-111">-Name</span></span>
<span data-ttu-id="afa74-112">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="afa74-112">Name of the database</span></span>

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
### <span data-ttu-id="afa74-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="afa74-113">-TargetRequestUnit</span></span>
<span data-ttu-id="afa74-114">O valor de unidade de solicitação de nível de banco de dados dedicado.</span><span class="sxs-lookup"><span data-stu-id="afa74-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="afa74-115">Se não for definido, essa coleção usará o banco de dados compartilhado RU.</span><span class="sxs-lookup"><span data-stu-id="afa74-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="afa74-116">-Coletas</span><span class="sxs-lookup"><span data-stu-id="afa74-116">-Collections</span></span>
<span data-ttu-id="afa74-117">A matriz de objetos de configuração de coleção MongoDb retornada por New-AzureRmDmsMongoDbDatabaseSetting chamada.</span><span class="sxs-lookup"><span data-stu-id="afa74-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="afa74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa74-118">CommonParameters</span></span>
<span data-ttu-id="afa74-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa74-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa74-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa74-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afa74-121">INPUTS</span></span>

### <span data-ttu-id="afa74-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="afa74-122">None</span></span>

## <span data-ttu-id="afa74-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afa74-123">OUTPUTS</span></span>

### <span data-ttu-id="afa74-124">Microsoft. Azure. Commands. datamigration. Models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="afa74-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="afa74-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afa74-125">NOTES</span></span>

## <span data-ttu-id="afa74-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afa74-126">RELATED LINKS</span></span>
