---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 817a4c8469d1d3652dade426857f88f9249f82b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887207"
---
# <span data-ttu-id="f7735-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="f7735-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="f7735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7735-102">SYNOPSIS</span></span>
<span data-ttu-id="f7735-103">Cria a configuração de coleção para migração de acordo com a migração mongoDb</span><span class="sxs-lookup"><span data-stu-id="f7735-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="f7735-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7735-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="f7735-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7735-105">DESCRIPTION</span></span>
<span data-ttu-id="f7735-106">O New-AzDataMigrationMongoDbCollectionSetting cmdlet cria o objeto de configuração de migração que especifica o comportamento de transferência e exclusão.</span><span class="sxs-lookup"><span data-stu-id="f7735-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="f7735-107">A saída do cmdlet é o par de valores-chave com o nome da coleção e o valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="f7735-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="f7735-108">A saída é usada na montagem das configurações de nível do banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="f7735-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="f7735-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7735-109">EXAMPLES</span></span>

### <span data-ttu-id="f7735-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7735-110">Example 1</span></span>
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

## <span data-ttu-id="f7735-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7735-111">PARAMETERS</span></span>

### <span data-ttu-id="f7735-112">-Name</span><span class="sxs-lookup"><span data-stu-id="f7735-112">-Name</span></span>
<span data-ttu-id="f7735-113">Nome da coleção</span><span class="sxs-lookup"><span data-stu-id="f7735-113">Name of the collection</span></span>

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

### <span data-ttu-id="f7735-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="f7735-114">-ShardKey</span></span>
<span data-ttu-id="f7735-115">A lista separada por vírgulas das chaves de fragmento.</span><span class="sxs-lookup"><span data-stu-id="f7735-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="f7735-116">Para destino mongoDb, você pode especificar a ordem de chave de fragmento de "ShardKeyName:Order", onde a ordem é 1, -1 ou vazia para hashed, por exemplo "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="f7735-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="f7735-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="f7735-117">-TargetRequestUnit</span></span>
<span data-ttu-id="f7735-118">O valor da unidade de solicitação de coleção dedicada.</span><span class="sxs-lookup"><span data-stu-id="f7735-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="f7735-119">Se não for definida, essa coleção usará o RU de banco de dados compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f7735-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="f7735-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="f7735-120">-CanDelete</span></span>
<span data-ttu-id="f7735-121">Se os dados de destino devem ser excluídos, se a opção estiver definida, eles serão limpos na migração</span><span class="sxs-lookup"><span data-stu-id="f7735-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="f7735-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7735-122">CommonParameters</span></span>
<span data-ttu-id="f7735-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7735-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7735-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7735-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7735-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7735-125">INPUTS</span></span>

### <span data-ttu-id="f7735-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f7735-126">None</span></span>

## <span data-ttu-id="f7735-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7735-127">OUTPUTS</span></span>

### <span data-ttu-id="f7735-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="f7735-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="f7735-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7735-129">NOTES</span></span>

## <span data-ttu-id="f7735-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7735-130">RELATED LINKS</span></span>
