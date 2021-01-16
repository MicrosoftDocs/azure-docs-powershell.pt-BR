---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259772"
---
# <span data-ttu-id="a7dbc-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7dbc-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="a7dbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dbc-103">Cria um novo objeto do tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="a7dbc-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="a7dbc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7dbc-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7dbc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7dbc-106">DESCRIPTION</span></span>
<span data-ttu-id="a7dbc-107">Objeto correspondente ao ConflictResolutionPolicy da API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="a7dbc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7dbc-108">EXAMPLES</span></span>

### <span data-ttu-id="a7dbc-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7dbc-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="a7dbc-110">OS</span><span class="sxs-lookup"><span data-stu-id="a7dbc-110">PARAMETERS</span></span>

### <span data-ttu-id="a7dbc-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="a7dbc-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="a7dbc-112">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="a7dbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dbc-113">-DefaultProfile</span></span>
<span data-ttu-id="a7dbc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dbc-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a7dbc-115">-Path</span></span>
<span data-ttu-id="a7dbc-116">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="a7dbc-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="a7dbc-117">-Type</span></span>
<span data-ttu-id="a7dbc-118">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="a7dbc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dbc-119">CommonParameters</span></span>
<span data-ttu-id="a7dbc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7dbc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dbc-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7dbc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dbc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7dbc-122">INPUTS</span></span>

### <span data-ttu-id="a7dbc-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a7dbc-123">None</span></span>

## <span data-ttu-id="a7dbc-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7dbc-124">OUTPUTS</span></span>

### <span data-ttu-id="a7dbc-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7dbc-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="a7dbc-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7dbc-126">NOTES</span></span>

## <span data-ttu-id="a7dbc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7dbc-127">RELATED LINKS</span></span>
