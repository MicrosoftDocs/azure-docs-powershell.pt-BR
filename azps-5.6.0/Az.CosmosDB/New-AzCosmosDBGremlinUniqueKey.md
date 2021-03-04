---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891492"
---
# <span data-ttu-id="7488d-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="7488d-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="7488d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7488d-102">SYNOPSIS</span></span>
<span data-ttu-id="7488d-103">Cria um novo objeto UniqueKeyPolicy do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7488d-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="7488d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7488d-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7488d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7488d-105">DESCRIPTION</span></span>
<span data-ttu-id="7488d-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="7488d-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="7488d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7488d-107">EXAMPLES</span></span>

### <span data-ttu-id="7488d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7488d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="7488d-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7488d-109">PARAMETERS</span></span>

### <span data-ttu-id="7488d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7488d-110">-DefaultProfile</span></span>
<span data-ttu-id="7488d-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7488d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7488d-112">-Path</span><span class="sxs-lookup"><span data-stu-id="7488d-112">-Path</span></span>
<span data-ttu-id="7488d-113">Matriz de cadeia de caracteres de valores de caminho</span><span class="sxs-lookup"><span data-stu-id="7488d-113">Array of string of path values</span></span>

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

### <span data-ttu-id="7488d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7488d-114">CommonParameters</span></span>
<span data-ttu-id="7488d-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7488d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7488d-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7488d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7488d-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7488d-117">INPUTS</span></span>

### <span data-ttu-id="7488d-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7488d-118">None</span></span>

## <span data-ttu-id="7488d-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7488d-119">OUTPUTS</span></span>

### <span data-ttu-id="7488d-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="7488d-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="7488d-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="7488d-121">NOTES</span></span>

## <span data-ttu-id="7488d-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7488d-122">RELATED LINKS</span></span>
