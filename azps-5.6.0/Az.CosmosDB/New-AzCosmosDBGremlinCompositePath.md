---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: c88cde11d277a4a2e0473d41f83e1b62e13216bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892651"
---
# <span data-ttu-id="29d92-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="29d92-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="29d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d92-102">SYNOPSIS</span></span>
<span data-ttu-id="29d92-103">Cria um novo objeto do tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="29d92-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="29d92-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="29d92-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="29d92-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29d92-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d92-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29d92-106">DESCRIPTION</span></span>
<span data-ttu-id="29d92-107">Objeto correspondente ao CompositePath da API de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="29d92-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="29d92-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29d92-108">EXAMPLES</span></span>

### <span data-ttu-id="29d92-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29d92-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="29d92-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29d92-110">PARAMETERS</span></span>

### <span data-ttu-id="29d92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d92-111">-DefaultProfile</span></span>
<span data-ttu-id="29d92-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29d92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d92-113">-Order</span><span class="sxs-lookup"><span data-stu-id="29d92-113">-Order</span></span>
<span data-ttu-id="29d92-114">Obtém ou define a ordem de classificação para caminhos compostos.</span><span class="sxs-lookup"><span data-stu-id="29d92-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="29d92-115">Os valores possíveis incluem: 'Ascending', 'Descending'</span><span class="sxs-lookup"><span data-stu-id="29d92-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="29d92-116">-Path</span><span class="sxs-lookup"><span data-stu-id="29d92-116">-Path</span></span>
<span data-ttu-id="29d92-117">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="29d92-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="29d92-118">Os caminhos de índice geralmente começam com raiz e terminam com caractere curinga (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="29d92-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="29d92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d92-119">CommonParameters</span></span>
<span data-ttu-id="29d92-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d92-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29d92-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d92-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29d92-122">INPUTS</span></span>

### <span data-ttu-id="29d92-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="29d92-123">None</span></span>

## <span data-ttu-id="29d92-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29d92-124">OUTPUTS</span></span>

### <span data-ttu-id="29d92-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="29d92-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="29d92-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="29d92-126">NOTES</span></span>

## <span data-ttu-id="29d92-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29d92-127">RELATED LINKS</span></span>
