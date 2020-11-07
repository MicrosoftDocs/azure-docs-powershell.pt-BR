---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774728"
---
# <span data-ttu-id="c35ef-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="c35ef-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="c35ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c35ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c35ef-103">Obter a lista de locais de atualização.</span><span class="sxs-lookup"><span data-stu-id="c35ef-103">Get the list of update locations.</span></span>

## <span data-ttu-id="c35ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c35ef-104">SYNTAX</span></span>

### <span data-ttu-id="c35ef-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="c35ef-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c35ef-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c35ef-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c35ef-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="c35ef-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c35ef-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c35ef-108">DESCRIPTION</span></span>
<span data-ttu-id="c35ef-109">Obter a lista de locais de atualização.</span><span class="sxs-lookup"><span data-stu-id="c35ef-109">Get the list of update locations.</span></span> <span data-ttu-id="c35ef-110">Os locais retornados podem ser usados para obter as atualizações disponíveis em um local específico usando Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="c35ef-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="c35ef-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c35ef-111">EXAMPLES</span></span>

### <span data-ttu-id="c35ef-112">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="c35ef-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="c35ef-113">Obter a lista de locais de atualização.</span><span class="sxs-lookup"><span data-stu-id="c35ef-113">Get the list of update locations.</span></span>

## <span data-ttu-id="c35ef-114">OS</span><span class="sxs-lookup"><span data-stu-id="c35ef-114">PARAMETERS</span></span>

### <span data-ttu-id="c35ef-115">-Local</span><span class="sxs-lookup"><span data-stu-id="c35ef-115">-Location</span></span>
<span data-ttu-id="c35ef-116">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="c35ef-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="c35ef-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="c35ef-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35ef-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c35ef-119">-ResourceId</span></span>
<span data-ttu-id="c35ef-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c35ef-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c35ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35ef-121">CommonParameters</span></span>
<span data-ttu-id="c35ef-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c35ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35ef-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c35ef-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35ef-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c35ef-124">INPUTS</span></span>

## <span data-ttu-id="c35ef-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c35ef-125">OUTPUTS</span></span>

### <span data-ttu-id="c35ef-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="c35ef-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="c35ef-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c35ef-127">NOTES</span></span>

## <span data-ttu-id="c35ef-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c35ef-128">RELATED LINKS</span></span>