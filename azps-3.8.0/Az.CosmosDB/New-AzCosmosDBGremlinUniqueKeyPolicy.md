---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943645"
---
# <span data-ttu-id="9af5a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="9af5a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="9af5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9af5a-102">SYNOPSIS</span></span>
<span data-ttu-id="9af5a-103">Cria um novo objeto CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="9af5a-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="9af5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9af5a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9af5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9af5a-105">DESCRIPTION</span></span>
<span data-ttu-id="9af5a-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="9af5a-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="9af5a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9af5a-107">EXAMPLES</span></span>

### <span data-ttu-id="9af5a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9af5a-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="9af5a-109">OS</span><span class="sxs-lookup"><span data-stu-id="9af5a-109">PARAMETERS</span></span>

### <span data-ttu-id="9af5a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af5a-110">-DefaultProfile</span></span>
<span data-ttu-id="9af5a-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9af5a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af5a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="9af5a-112">-UniqueKey</span></span>
<span data-ttu-id="9af5a-113">Matriz de objetos do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="9af5a-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af5a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af5a-114">CommonParameters</span></span>
<span data-ttu-id="9af5a-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af5a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af5a-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9af5a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af5a-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9af5a-117">INPUTS</span></span>

### <span data-ttu-id="9af5a-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9af5a-118">None</span></span>

## <span data-ttu-id="9af5a-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9af5a-119">OUTPUTS</span></span>

### <span data-ttu-id="9af5a-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="9af5a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="9af5a-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9af5a-121">NOTES</span></span>

## <span data-ttu-id="9af5a-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9af5a-122">RELATED LINKS</span></span>
