---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115090"
---
# <span data-ttu-id="b5792-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b5792-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="b5792-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5792-102">SYNOPSIS</span></span>
<span data-ttu-id="b5792-103">Cria um novo objeto CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="b5792-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="b5792-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5792-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5792-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5792-105">DESCRIPTION</span></span>
<span data-ttu-id="b5792-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="b5792-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="b5792-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5792-107">EXAMPLES</span></span>

### <span data-ttu-id="b5792-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5792-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="b5792-109">OS</span><span class="sxs-lookup"><span data-stu-id="b5792-109">PARAMETERS</span></span>

### <span data-ttu-id="b5792-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5792-110">-DefaultProfile</span></span>
<span data-ttu-id="b5792-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5792-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5792-112">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b5792-112">-Path</span></span>
<span data-ttu-id="b5792-113">Matriz de cadeia de caracteres de valores de caminho</span><span class="sxs-lookup"><span data-stu-id="b5792-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5792-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5792-114">CommonParameters</span></span>
<span data-ttu-id="b5792-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5792-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5792-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5792-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5792-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5792-117">INPUTS</span></span>

### <span data-ttu-id="b5792-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b5792-118">None</span></span>

## <span data-ttu-id="b5792-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5792-119">OUTPUTS</span></span>

### <span data-ttu-id="b5792-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b5792-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="b5792-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5792-121">NOTES</span></span>

## <span data-ttu-id="b5792-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5792-122">RELATED LINKS</span></span>
