---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: aeb4c89ec4928118c5ebad05fe3c3602d88420ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601035"
---
# <span data-ttu-id="a34eb-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="a34eb-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="a34eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a34eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a34eb-103">Cria uma configuração de coleção para a migração de acordo com a migração do mongoDb</span><span class="sxs-lookup"><span data-stu-id="a34eb-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="a34eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a34eb-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="a34eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a34eb-105">DESCRIPTION</span></span>
<span data-ttu-id="a34eb-106">O cmdlet New-AzDataMigrationMongoDbCollectionSetting cria o objeto de configuração de migração que especifica a taxa de transferência e o comportamento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="a34eb-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="a34eb-107">A saída o cmdlet é par chave-valor com nome da coleção e valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="a34eb-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="a34eb-108">A saída é usada para montar as configurações do nível de banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="a34eb-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="a34eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a34eb-109">EXAMPLES</span></span>

### <span data-ttu-id="a34eb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a34eb-110">Example 1</span></span>
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

## <span data-ttu-id="a34eb-111">OS</span><span class="sxs-lookup"><span data-stu-id="a34eb-111">PARAMETERS</span></span>

### <span data-ttu-id="a34eb-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="a34eb-112">-Name</span></span>
<span data-ttu-id="a34eb-113">Nome da coleção</span><span class="sxs-lookup"><span data-stu-id="a34eb-113">Name of the collection</span></span>

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

### <span data-ttu-id="a34eb-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="a34eb-114">-ShardKey</span></span>
<span data-ttu-id="a34eb-115">A lista separada por vírgula das chaves de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="a34eb-115">The comma seperated list of the shard keys.</span></span> <span data-ttu-id="a34eb-116">Para o destino do mongoDb, você pode especificar a ordem da chave de fragmentos de "ShardKeyName: Order", em que o pedido é 1,-1 ou vazio para hash, por exemplo, "_id, email:-1".</span><span class="sxs-lookup"><span data-stu-id="a34eb-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="a34eb-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="a34eb-117">-TargetRequestUnit</span></span>
<span data-ttu-id="a34eb-118">O valor da unidade de solicitação de coleção dedicada.</span><span class="sxs-lookup"><span data-stu-id="a34eb-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="a34eb-119">Se não for definido, essa coleção usará o banco de dados compartilhado RU.</span><span class="sxs-lookup"><span data-stu-id="a34eb-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="a34eb-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="a34eb-120">-CanDelete</span></span>
<span data-ttu-id="a34eb-121">Se os dados de destino devem ser excluídos, se a opção for definida, ele será limpo na migração</span><span class="sxs-lookup"><span data-stu-id="a34eb-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="a34eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34eb-122">CommonParameters</span></span>
<span data-ttu-id="a34eb-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a34eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34eb-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34eb-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a34eb-125">INPUTS</span></span>

### <span data-ttu-id="a34eb-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a34eb-126">None</span></span>

## <span data-ttu-id="a34eb-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a34eb-127">OUTPUTS</span></span>

### <span data-ttu-id="a34eb-128">Microsoft. Azure. Commands. datamigration. Models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="a34eb-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="a34eb-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a34eb-129">NOTES</span></span>

## <span data-ttu-id="a34eb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a34eb-130">RELATED LINKS</span></span>
