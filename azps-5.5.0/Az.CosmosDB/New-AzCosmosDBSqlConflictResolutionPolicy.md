---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116457"
---
# <span data-ttu-id="4f392-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f392-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="4f392-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f392-102">SYNOPSIS</span></span>
<span data-ttu-id="4f392-103">Cria um novo objeto do tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4f392-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="4f392-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="4f392-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="4f392-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f392-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f392-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f392-106">DESCRIPTION</span></span>
<span data-ttu-id="4f392-107">Objeto correspondente ao ConflictResolutionPolicy da SQL API.</span><span class="sxs-lookup"><span data-stu-id="4f392-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="4f392-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f392-108">EXAMPLES</span></span>

### <span data-ttu-id="4f392-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f392-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="4f392-110">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="4f392-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="4f392-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f392-111">PARAMETERS</span></span>

### <span data-ttu-id="4f392-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="4f392-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="4f392-113">A ser fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="4f392-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="4f392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f392-114">-DefaultProfile</span></span>
<span data-ttu-id="4f392-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f392-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f392-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4f392-116">-Path</span></span>
<span data-ttu-id="4f392-117">A ser fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="4f392-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="4f392-118">-Tipo</span><span class="sxs-lookup"><span data-stu-id="4f392-118">-Type</span></span>
<span data-ttu-id="4f392-119">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="4f392-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="4f392-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f392-120">CommonParameters</span></span>
<span data-ttu-id="4f392-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f392-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f392-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f392-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f392-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f392-123">INPUTS</span></span>

### <span data-ttu-id="4f392-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4f392-124">None</span></span>

## <span data-ttu-id="4f392-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f392-125">OUTPUTS</span></span>

### <span data-ttu-id="4f392-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f392-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="4f392-127">Notas</span><span class="sxs-lookup"><span data-stu-id="4f392-127">NOTES</span></span>

## <span data-ttu-id="4f392-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f392-128">RELATED LINKS</span></span>
