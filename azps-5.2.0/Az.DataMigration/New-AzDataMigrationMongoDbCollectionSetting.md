---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260662"
---
# <span data-ttu-id="1275c-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="1275c-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="1275c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1275c-102">SYNOPSIS</span></span>
<span data-ttu-id="1275c-103">Cria uma configuração de coleção para a migração de acordo com a migração do mongoDb</span><span class="sxs-lookup"><span data-stu-id="1275c-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="1275c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1275c-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="1275c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1275c-105">DESCRIPTION</span></span>
<span data-ttu-id="1275c-106">O cmdlet New-AzDataMigrationMongoDbCollectionSetting cria o objeto de configuração de migração que especifica a taxa de transferência e o comportamento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="1275c-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="1275c-107">A saída o cmdlet é par chave-valor com nome da coleção e valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="1275c-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="1275c-108">A saída é usada para montar as configurações do nível de banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="1275c-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="1275c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1275c-109">EXAMPLES</span></span>

### <span data-ttu-id="1275c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1275c-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="1275c-111">OS</span><span class="sxs-lookup"><span data-stu-id="1275c-111">PARAMETERS</span></span>

### <span data-ttu-id="1275c-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="1275c-112">-Name</span></span>
<span data-ttu-id="1275c-113">Nome da coleção</span><span class="sxs-lookup"><span data-stu-id="1275c-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1275c-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="1275c-114">-ShardKey</span></span>
<span data-ttu-id="1275c-115">A lista separada por vírgula das chaves de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="1275c-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="1275c-116">Para o destino do mongoDb, você pode especificar a ordem da chave de fragmentos de "ShardKeyName: Order", em que o pedido é 1,-1 ou vazio para hash, por exemplo, "_id, email:-1".</span><span class="sxs-lookup"><span data-stu-id="1275c-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1275c-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="1275c-117">-TargetRequestUnit</span></span>
<span data-ttu-id="1275c-118">O valor da unidade de solicitação de coleção dedicada.</span><span class="sxs-lookup"><span data-stu-id="1275c-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="1275c-119">Se não for definido, essa coleção usará o banco de dados compartilhado RU.</span><span class="sxs-lookup"><span data-stu-id="1275c-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="1275c-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="1275c-120">-CanDelete</span></span>
<span data-ttu-id="1275c-121">Se os dados de destino devem ser excluídos, se a opção for definida, ele será limpo na migração</span><span class="sxs-lookup"><span data-stu-id="1275c-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="1275c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1275c-122">CommonParameters</span></span>
<span data-ttu-id="1275c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1275c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1275c-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1275c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1275c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1275c-125">INPUTS</span></span>

### <span data-ttu-id="1275c-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1275c-126">None</span></span>

## <span data-ttu-id="1275c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1275c-127">OUTPUTS</span></span>

### <span data-ttu-id="1275c-128">Microsoft. Azure. Commands. datamigration. Models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="1275c-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="1275c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1275c-129">NOTES</span></span>

## <span data-ttu-id="1275c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1275c-130">RELATED LINKS</span></span>
