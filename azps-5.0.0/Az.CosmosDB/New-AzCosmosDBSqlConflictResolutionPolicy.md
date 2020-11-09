---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281306"
---
# <span data-ttu-id="35bf2-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="35bf2-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="35bf2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="35bf2-103">Cria um novo objeto do tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="35bf2-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="35bf2-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="35bf2-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="35bf2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35bf2-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35bf2-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35bf2-106">DESCRIPTION</span></span>
<span data-ttu-id="35bf2-107">Objeto correspondente ao ConflictResolutionPolicy da API SQL.</span><span class="sxs-lookup"><span data-stu-id="35bf2-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="35bf2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35bf2-108">EXAMPLES</span></span>

### <span data-ttu-id="35bf2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35bf2-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="35bf2-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="35bf2-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="35bf2-111">OS</span><span class="sxs-lookup"><span data-stu-id="35bf2-111">PARAMETERS</span></span>

### <span data-ttu-id="35bf2-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="35bf2-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="35bf2-113">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="35bf2-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="35bf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35bf2-114">-DefaultProfile</span></span>
<span data-ttu-id="35bf2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35bf2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35bf2-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="35bf2-116">-Path</span></span>
<span data-ttu-id="35bf2-117">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="35bf2-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="35bf2-118">-Digite</span><span class="sxs-lookup"><span data-stu-id="35bf2-118">-Type</span></span>
<span data-ttu-id="35bf2-119">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="35bf2-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="35bf2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35bf2-120">CommonParameters</span></span>
<span data-ttu-id="35bf2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35bf2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35bf2-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35bf2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35bf2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35bf2-123">INPUTS</span></span>

### <span data-ttu-id="35bf2-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="35bf2-124">None</span></span>

## <span data-ttu-id="35bf2-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35bf2-125">OUTPUTS</span></span>

### <span data-ttu-id="35bf2-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="35bf2-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="35bf2-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35bf2-127">NOTES</span></span>

## <span data-ttu-id="35bf2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35bf2-128">RELATED LINKS</span></span>
