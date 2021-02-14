---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111030"
---
# <span data-ttu-id="bf407-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="bf407-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="bf407-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf407-102">SYNOPSIS</span></span>
<span data-ttu-id="bf407-103">Cria um novo objeto UniqueKeyPolicy do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="bf407-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="bf407-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf407-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf407-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf407-105">DESCRIPTION</span></span>
<span data-ttu-id="bf407-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="bf407-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="bf407-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bf407-107">EXAMPLES</span></span>

### <span data-ttu-id="bf407-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf407-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="bf407-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf407-109">PARAMETERS</span></span>

### <span data-ttu-id="bf407-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf407-110">-DefaultProfile</span></span>
<span data-ttu-id="bf407-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf407-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf407-112">-Caminho</span><span class="sxs-lookup"><span data-stu-id="bf407-112">-Path</span></span>
<span data-ttu-id="bf407-113">Matriz de cadeia de caracteres de valores de caminho</span><span class="sxs-lookup"><span data-stu-id="bf407-113">Array of string of path values</span></span>

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

### <span data-ttu-id="bf407-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf407-114">CommonParameters</span></span>
<span data-ttu-id="bf407-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf407-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf407-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf407-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf407-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="bf407-117">INPUTS</span></span>

### <span data-ttu-id="bf407-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bf407-118">None</span></span>

## <span data-ttu-id="bf407-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="bf407-119">OUTPUTS</span></span>

### <span data-ttu-id="bf407-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="bf407-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="bf407-121">Notas</span><span class="sxs-lookup"><span data-stu-id="bf407-121">NOTES</span></span>

## <span data-ttu-id="bf407-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf407-122">RELATED LINKS</span></span>
