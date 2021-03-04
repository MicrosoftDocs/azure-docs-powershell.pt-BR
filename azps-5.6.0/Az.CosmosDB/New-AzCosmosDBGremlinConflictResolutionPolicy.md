---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892648"
---
# <span data-ttu-id="3f0d7-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f0d7-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="3f0d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0d7-103">Cria um novo objeto do tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="3f0d7-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="3f0d7-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3f0d7-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f0d7-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3f0d7-106">DESCRIPTION</span></span>
<span data-ttu-id="3f0d7-107">Objeto correspondente a ConflictResolutionPolicy da API de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="3f0d7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f0d7-108">EXAMPLES</span></span>

### <span data-ttu-id="3f0d7-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f0d7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="3f0d7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3f0d7-110">PARAMETERS</span></span>

### <span data-ttu-id="3f0d7-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="3f0d7-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="3f0d7-112">Para ser fornecido quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="3f0d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0d7-113">-DefaultProfile</span></span>
<span data-ttu-id="3f0d7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f0d7-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3f0d7-115">-Path</span></span>
<span data-ttu-id="3f0d7-116">Para ser fornecido quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="3f0d7-117">-Type</span><span class="sxs-lookup"><span data-stu-id="3f0d7-117">-Type</span></span>
<span data-ttu-id="3f0d7-118">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="3f0d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0d7-119">CommonParameters</span></span>
<span data-ttu-id="3f0d7-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f0d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0d7-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f0d7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0d7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f0d7-122">INPUTS</span></span>

### <span data-ttu-id="3f0d7-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3f0d7-123">None</span></span>

## <span data-ttu-id="3f0d7-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3f0d7-124">OUTPUTS</span></span>

### <span data-ttu-id="3f0d7-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f0d7-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="3f0d7-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="3f0d7-126">NOTES</span></span>

## <span data-ttu-id="3f0d7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f0d7-127">RELATED LINKS</span></span>
