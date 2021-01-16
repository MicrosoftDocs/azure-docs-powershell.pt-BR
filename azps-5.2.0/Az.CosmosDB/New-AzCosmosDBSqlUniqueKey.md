---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263618"
---
# <span data-ttu-id="d95b8-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="d95b8-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="d95b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d95b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d95b8-103">Cria um novo objeto CosmosDB SQL UniqueKey.</span><span class="sxs-lookup"><span data-stu-id="d95b8-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="d95b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d95b8-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d95b8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d95b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d95b8-106">O cmdlet **New-AzCosmosDBSqlUniqueKey** cria um novo objeto do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="d95b8-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="d95b8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d95b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d95b8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d95b8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="d95b8-109">OS</span><span class="sxs-lookup"><span data-stu-id="d95b8-109">PARAMETERS</span></span>

### <span data-ttu-id="d95b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95b8-110">-DefaultProfile</span></span>
<span data-ttu-id="d95b8-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d95b8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d95b8-112">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d95b8-112">-Path</span></span>
<span data-ttu-id="d95b8-113">Matriz de cadeia de caracteres de valores de caminho</span><span class="sxs-lookup"><span data-stu-id="d95b8-113">Array of string of path values</span></span>

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

### <span data-ttu-id="d95b8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95b8-114">CommonParameters</span></span>
<span data-ttu-id="d95b8-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95b8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95b8-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d95b8-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95b8-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d95b8-117">INPUTS</span></span>

### <span data-ttu-id="d95b8-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d95b8-118">None</span></span>

## <span data-ttu-id="d95b8-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d95b8-119">OUTPUTS</span></span>

### <span data-ttu-id="d95b8-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="d95b8-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="d95b8-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d95b8-121">NOTES</span></span>

## <span data-ttu-id="d95b8-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d95b8-122">RELATED LINKS</span></span>
