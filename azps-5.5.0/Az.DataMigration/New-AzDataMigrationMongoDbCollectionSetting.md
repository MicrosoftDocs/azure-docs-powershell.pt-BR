---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111941"
---
# <span data-ttu-id="135f6-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="135f6-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="135f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="135f6-102">SYNOPSIS</span></span>
<span data-ttu-id="135f6-103">Cria configuração de coleção para migração de acordo com a migração mongoDb</span><span class="sxs-lookup"><span data-stu-id="135f6-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="135f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="135f6-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="135f6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="135f6-105">DESCRIPTION</span></span>
<span data-ttu-id="135f6-106">O New-AzDataMigrationMongoDbCollectionSetting cmdlet cria o objeto de configuração de migração que especifica o comportamento de produtividade e exclusão.</span><span class="sxs-lookup"><span data-stu-id="135f6-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="135f6-107">A saída do cmdlet é o par de valores-chave com o nome da coleção e o valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="135f6-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="135f6-108">A saída é usada na montagem das configurações de nível de banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="135f6-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="135f6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="135f6-109">EXAMPLES</span></span>

### <span data-ttu-id="135f6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="135f6-110">Example 1</span></span>
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

## <span data-ttu-id="135f6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="135f6-111">PARAMETERS</span></span>

### <span data-ttu-id="135f6-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="135f6-112">-Name</span></span>
<span data-ttu-id="135f6-113">Nome da coleção</span><span class="sxs-lookup"><span data-stu-id="135f6-113">Name of the collection</span></span>

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

### <span data-ttu-id="135f6-114">-SkeyKey</span><span class="sxs-lookup"><span data-stu-id="135f6-114">-ShardKey</span></span>
<span data-ttu-id="135f6-115">A lista de vírgulas separadas das teclas de estilhaço.</span><span class="sxs-lookup"><span data-stu-id="135f6-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="135f6-116">Para o destino mongoDb, você pode especificar a ordem de chave estilhaço de "SkeyKeyName:Order", em que a ordem é 1, -1 ou vazia para o hashed, por exemplo, "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="135f6-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="135f6-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="135f6-117">-TargetRequestUnit</span></span>
<span data-ttu-id="135f6-118">O valor de unidade da solicitação de coleção dedicada.</span><span class="sxs-lookup"><span data-stu-id="135f6-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="135f6-119">Se não estiver definida, essa coleção usará o RU de banco de dados compartilhado.</span><span class="sxs-lookup"><span data-stu-id="135f6-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="135f6-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="135f6-120">-CanDelete</span></span>
<span data-ttu-id="135f6-121">Se os dados de destino devem ser excluídos, se a opção estiver definida, eles serão limpos na migração</span><span class="sxs-lookup"><span data-stu-id="135f6-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="135f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135f6-122">CommonParameters</span></span>
<span data-ttu-id="135f6-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135f6-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="135f6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135f6-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="135f6-125">INPUTS</span></span>

### <span data-ttu-id="135f6-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="135f6-126">None</span></span>

## <span data-ttu-id="135f6-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="135f6-127">OUTPUTS</span></span>

### <span data-ttu-id="135f6-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="135f6-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="135f6-129">Notas</span><span class="sxs-lookup"><span data-stu-id="135f6-129">NOTES</span></span>

## <span data-ttu-id="135f6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="135f6-130">RELATED LINKS</span></span>
