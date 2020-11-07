---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774861"
---
# <span data-ttu-id="1b4cc-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="1b4cc-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="1b4cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4cc-103">Retorna o serviço da fila.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-103">Returns the queue service.</span></span>

## <span data-ttu-id="1b4cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b4cc-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="1b4cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b4cc-105">DESCRIPTION</span></span>
<span data-ttu-id="1b4cc-106">Retorna o serviço da fila.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-106">Returns the queue service.</span></span>

## <span data-ttu-id="1b4cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b4cc-107">EXAMPLES</span></span>

### <span data-ttu-id="1b4cc-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1b4cc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="1b4cc-109">Obter o serviço da fila.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-109">Get the queue service.</span></span>

## <span data-ttu-id="1b4cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="1b4cc-110">PARAMETERS</span></span>

### <span data-ttu-id="1b4cc-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="1b4cc-111">-FarmName</span></span>
<span data-ttu-id="1b4cc-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-112">Farm Id.</span></span>

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

### <span data-ttu-id="1b4cc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4cc-113">-ResourceGroupName</span></span>
<span data-ttu-id="1b4cc-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-114">Resource group name.</span></span>

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

### <span data-ttu-id="1b4cc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4cc-115">CommonParameters</span></span>
<span data-ttu-id="1b4cc-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b4cc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4cc-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4cc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4cc-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b4cc-118">INPUTS</span></span>

## <span data-ttu-id="1b4cc-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b4cc-119">OUTPUTS</span></span>

### <span data-ttu-id="1b4cc-120">Microsoft. AzureStack. Management. Storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="1b4cc-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="1b4cc-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b4cc-121">NOTES</span></span>

## <span data-ttu-id="1b4cc-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b4cc-122">RELATED LINKS</span></span>

