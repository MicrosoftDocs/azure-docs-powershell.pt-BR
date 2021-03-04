---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 634a6a8e1e6b921703603ee7f2bfd345aa64608c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892998"
---
# <span data-ttu-id="d0173-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="d0173-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="d0173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0173-102">SYNOPSIS</span></span>
<span data-ttu-id="d0173-103">Cria uma nova Coluna de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d0173-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="d0173-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d0173-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0173-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d0173-105">DESCRIPTION</span></span>
<span data-ttu-id="d0173-106">O **New-AzCosmosDBCassandraColumn** cria uma nova Coluna de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d0173-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="d0173-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0173-107">EXAMPLES</span></span>

### <span data-ttu-id="d0173-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0173-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="d0173-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d0173-109">PARAMETERS</span></span>

### <span data-ttu-id="d0173-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0173-110">-DefaultProfile</span></span>
<span data-ttu-id="d0173-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0173-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0173-112">-Name</span><span class="sxs-lookup"><span data-stu-id="d0173-112">-Name</span></span>
<span data-ttu-id="d0173-113">Nome da Coluna de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d0173-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="d0173-114">-Type</span><span class="sxs-lookup"><span data-stu-id="d0173-114">-Type</span></span>
<span data-ttu-id="d0173-115">Tipo de Coluna de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d0173-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="d0173-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0173-116">CommonParameters</span></span>
<span data-ttu-id="d0173-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0173-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0173-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0173-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0173-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0173-119">INPUTS</span></span>

### <span data-ttu-id="d0173-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d0173-120">None</span></span>

## <span data-ttu-id="d0173-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d0173-121">OUTPUTS</span></span>

### <span data-ttu-id="d0173-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="d0173-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="d0173-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="d0173-123">NOTES</span></span>

## <span data-ttu-id="d0173-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0173-124">RELATED LINKS</span></span>
