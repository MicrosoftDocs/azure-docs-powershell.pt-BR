---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775051"
---
# <span data-ttu-id="ca8d7-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="ca8d7-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="ca8d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8d7-103">Retorna uma lista de todos os farms de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="ca8d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca8d7-104">SYNTAX</span></span>

### <span data-ttu-id="ca8d7-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca8d7-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ca8d7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ca8d7-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ca8d7-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="ca8d7-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ca8d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca8d7-108">DESCRIPTION</span></span>
<span data-ttu-id="ca8d7-109">Retorna uma lista de todos os farms de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="ca8d7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca8d7-110">EXAMPLES</span></span>

### <span data-ttu-id="ca8d7-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ca8d7-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="ca8d7-112">Obter a lista de todos os farms de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="ca8d7-113">OS</span><span class="sxs-lookup"><span data-stu-id="ca8d7-113">PARAMETERS</span></span>

### <span data-ttu-id="ca8d7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca8d7-114">-Name</span></span>
<span data-ttu-id="ca8d7-115">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8d7-116">-ResourceGroupName</span></span>
<span data-ttu-id="ca8d7-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-117">Resource group name.</span></span>

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

### <span data-ttu-id="ca8d7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca8d7-118">-ResourceId</span></span>
<span data-ttu-id="ca8d7-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d7-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="ca8d7-120">-Skip</span></span>
<span data-ttu-id="ca8d7-121">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d7-122">-Início</span><span class="sxs-lookup"><span data-stu-id="ca8d7-122">-Top</span></span>
<span data-ttu-id="ca8d7-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ca8d7-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8d7-125">CommonParameters</span></span>
<span data-ttu-id="ca8d7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8d7-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8d7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8d7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca8d7-128">INPUTS</span></span>

## <span data-ttu-id="ca8d7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca8d7-129">OUTPUTS</span></span>

### <span data-ttu-id="ca8d7-130">Microsoft. AzureStack. Management. Storage. admin. Models. farm</span><span class="sxs-lookup"><span data-stu-id="ca8d7-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="ca8d7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca8d7-131">NOTES</span></span>

## <span data-ttu-id="ca8d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca8d7-132">RELATED LINKS</span></span>
