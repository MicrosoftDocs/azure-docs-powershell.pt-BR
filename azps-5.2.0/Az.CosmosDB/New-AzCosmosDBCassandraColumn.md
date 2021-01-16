---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258097"
---
# <span data-ttu-id="00a9c-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="00a9c-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="00a9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="00a9c-103">Cria uma nova coluna CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="00a9c-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="00a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00a9c-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00a9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="00a9c-106">O **New-AzCosmosDBCassandraColumn** cria uma nova coluna Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="00a9c-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="00a9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="00a9c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00a9c-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="00a9c-109">OS</span><span class="sxs-lookup"><span data-stu-id="00a9c-109">PARAMETERS</span></span>

### <span data-ttu-id="00a9c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a9c-110">-DefaultProfile</span></span>
<span data-ttu-id="00a9c-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00a9c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a9c-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="00a9c-112">-Name</span></span>
<span data-ttu-id="00a9c-113">Nome da coluna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="00a9c-113">Name of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a9c-114">-Digite</span><span class="sxs-lookup"><span data-stu-id="00a9c-114">-Type</span></span>
<span data-ttu-id="00a9c-115">Tipo de coluna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="00a9c-115">Type of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a9c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a9c-116">CommonParameters</span></span>
<span data-ttu-id="00a9c-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a9c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a9c-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00a9c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a9c-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00a9c-119">INPUTS</span></span>

### <span data-ttu-id="00a9c-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="00a9c-120">None</span></span>

## <span data-ttu-id="00a9c-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00a9c-121">OUTPUTS</span></span>

### <span data-ttu-id="00a9c-122">Microsoft. Azure. Commands. CosmosDB. Models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="00a9c-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="00a9c-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00a9c-123">NOTES</span></span>

## <span data-ttu-id="00a9c-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00a9c-124">RELATED LINKS</span></span>
