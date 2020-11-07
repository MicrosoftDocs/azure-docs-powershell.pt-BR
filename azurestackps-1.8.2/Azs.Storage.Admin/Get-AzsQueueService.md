---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d6bd071f4e1d61fdf2d682459dbe8baa57b5276
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946898"
---
# <span data-ttu-id="c3bdd-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="c3bdd-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="c3bdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bdd-103">Retorna o serviço da fila.</span><span class="sxs-lookup"><span data-stu-id="c3bdd-103">Returns the queue service.</span></span>

## <span data-ttu-id="c3bdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3bdd-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="c3bdd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="c3bdd-106">Retorna o serviço da fila.</span><span class="sxs-lookup"><span data-stu-id="c3bdd-106">Returns the queue service.</span></span>

## <span data-ttu-id="c3bdd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="c3bdd-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="c3bdd-108">EXAMPLE 1</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="c3bdd-109">Obter o serviço da fila.</span><span class="sxs-lookup"><span data-stu-id="c3bdd-109">Get the queue service.</span></span>

## <span data-ttu-id="c3bdd-110">OS</span><span class="sxs-lookup"><span data-stu-id="c3bdd-110">PARAMETERS</span></span>

### <span data-ttu-id="c3bdd-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="c3bdd-111">-FarmName</span></span>
<span data-ttu-id="c3bdd-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="c3bdd-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3bdd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3bdd-113">-ResourceGroupName</span></span>
<span data-ttu-id="c3bdd-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c3bdd-114">Resource group name.</span></span>

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

### <span data-ttu-id="c3bdd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bdd-115">CommonParameters</span></span>
<span data-ttu-id="c3bdd-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3bdd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3bdd-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3bdd-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bdd-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3bdd-118">INPUTS</span></span>

## <span data-ttu-id="c3bdd-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3bdd-119">OUTPUTS</span></span>

### <span data-ttu-id="c3bdd-120">Microsoft. AzureStack. Management. Storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="c3bdd-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="c3bdd-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3bdd-121">NOTES</span></span>

## <span data-ttu-id="c3bdd-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3bdd-122">RELATED LINKS</span></span>
