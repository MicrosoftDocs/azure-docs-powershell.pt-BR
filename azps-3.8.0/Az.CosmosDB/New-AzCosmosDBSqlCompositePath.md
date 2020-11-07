---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943644"
---
# <span data-ttu-id="8cd95-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="8cd95-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="8cd95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cd95-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd95-103">Cria um novo objeto do tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="8cd95-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="8cd95-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="8cd95-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="8cd95-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cd95-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cd95-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cd95-106">DESCRIPTION</span></span>
<span data-ttu-id="8cd95-107">Objeto correspondente ao CompositePath da API SQL.</span><span class="sxs-lookup"><span data-stu-id="8cd95-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="8cd95-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cd95-108">EXAMPLES</span></span>

### <span data-ttu-id="8cd95-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cd95-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="8cd95-110">OS</span><span class="sxs-lookup"><span data-stu-id="8cd95-110">PARAMETERS</span></span>

### <span data-ttu-id="8cd95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd95-111">-DefaultProfile</span></span>
<span data-ttu-id="8cd95-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd95-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cd95-113">-Pedido</span><span class="sxs-lookup"><span data-stu-id="8cd95-113">-Order</span></span>
<span data-ttu-id="8cd95-114">Obtém ou define a ordem de classificação para caminhos compostos.</span><span class="sxs-lookup"><span data-stu-id="8cd95-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="8cd95-115">Os valores possíveis incluem: ' crescente ', ' decrescente '</span><span class="sxs-lookup"><span data-stu-id="8cd95-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="8cd95-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8cd95-116">-Path</span></span>
<span data-ttu-id="8cd95-117">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="8cd95-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="8cd95-118">Os caminhos de índice geralmente começam com root e end com curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="8cd95-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="8cd95-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd95-119">CommonParameters</span></span>
<span data-ttu-id="8cd95-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd95-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd95-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cd95-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd95-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cd95-122">INPUTS</span></span>

### <span data-ttu-id="8cd95-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8cd95-123">None</span></span>

## <span data-ttu-id="8cd95-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cd95-124">OUTPUTS</span></span>

### <span data-ttu-id="8cd95-125">Microsoft. Azure. Commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="8cd95-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="8cd95-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cd95-126">NOTES</span></span>

## <span data-ttu-id="8cd95-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cd95-127">RELATED LINKS</span></span>
