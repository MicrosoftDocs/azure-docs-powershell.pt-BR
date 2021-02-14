---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111042"
---
# <span data-ttu-id="e8bba-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="e8bba-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="e8bba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bba-103">Cria uma nova Chave Cluster De Cluster do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e8bba-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="e8bba-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8bba-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8bba-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8bba-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bba-106">O **New-AzCosmosDBCasslusãoClusterKey** cria uma nova Chave de Cluster de Cluster DoSterDB.</span><span class="sxs-lookup"><span data-stu-id="e8bba-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="e8bba-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e8bba-107">EXAMPLES</span></span>

### <span data-ttu-id="e8bba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8bba-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="e8bba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8bba-109">PARAMETERS</span></span>

### <span data-ttu-id="e8bba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bba-110">-DefaultProfile</span></span>
<span data-ttu-id="e8bba-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bba-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8bba-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8bba-112">-Name</span></span>
<span data-ttu-id="e8bba-113">Nome da Chave Cluster de Cluster de Brasília.</span><span class="sxs-lookup"><span data-stu-id="e8bba-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="e8bba-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e8bba-114">-OrderBy</span></span>
<span data-ttu-id="e8bba-115">Ordenação da tecla Cluster de Guida.</span><span class="sxs-lookup"><span data-stu-id="e8bba-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="e8bba-116">Os valores possíveis incluem: 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="e8bba-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="e8bba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bba-117">CommonParameters</span></span>
<span data-ttu-id="e8bba-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bba-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8bba-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bba-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="e8bba-120">INPUTS</span></span>

### <span data-ttu-id="e8bba-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e8bba-121">None</span></span>

## <span data-ttu-id="e8bba-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="e8bba-122">OUTPUTS</span></span>

### <span data-ttu-id="e8bba-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="e8bba-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="e8bba-124">Notas</span><span class="sxs-lookup"><span data-stu-id="e8bba-124">NOTES</span></span>

## <span data-ttu-id="e8bba-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8bba-125">RELATED LINKS</span></span>
