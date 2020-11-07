---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946913"
---
# <span data-ttu-id="3cbe6-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="3cbe6-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="3cbe6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbe6-103">Retorna uma lista de compartilhamentos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3cbe6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cbe6-104">SYNTAX</span></span>

### <span data-ttu-id="3cbe6-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3cbe6-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3cbe6-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3cbe6-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3cbe6-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="3cbe6-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3cbe6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cbe6-108">DESCRIPTION</span></span>
<span data-ttu-id="3cbe6-109">Retorna uma lista de compartilhamentos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3cbe6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cbe6-110">EXAMPLES</span></span>

### <span data-ttu-id="3cbe6-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="3cbe6-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="3cbe6-112">Obter a lista de compartilhamentos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="3cbe6-113">OS</span><span class="sxs-lookup"><span data-stu-id="3cbe6-113">PARAMETERS</span></span>

### <span data-ttu-id="3cbe6-114">-Farmname</span><span class="sxs-lookup"><span data-stu-id="3cbe6-114">-FarmName</span></span>
<span data-ttu-id="3cbe6-115">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbe6-116">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3cbe6-116">-ShareName</span></span>
<span data-ttu-id="3cbe6-117">Nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbe6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbe6-118">-ResourceGroupName</span></span>
<span data-ttu-id="3cbe6-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-119">Resource group name.</span></span>

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

### <span data-ttu-id="3cbe6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbe6-120">-ResourceId</span></span>
<span data-ttu-id="3cbe6-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-121">The resource id.</span></span>

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

### <span data-ttu-id="3cbe6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbe6-122">CommonParameters</span></span>
<span data-ttu-id="3cbe6-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cbe6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbe6-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cbe6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbe6-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cbe6-125">INPUTS</span></span>

## <span data-ttu-id="3cbe6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cbe6-126">OUTPUTS</span></span>

### <span data-ttu-id="3cbe6-127">Microsoft. AzureStack. Management. Storage. admin. Models. share</span><span class="sxs-lookup"><span data-stu-id="3cbe6-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="3cbe6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cbe6-128">NOTES</span></span>

## <span data-ttu-id="3cbe6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cbe6-129">RELATED LINKS</span></span>
