---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 419bddaaa121e052b486bf4bb5408fcae6160fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425900"
---
# <span data-ttu-id="5f280-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="5f280-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="5f280-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f280-102">SYNOPSIS</span></span>
<span data-ttu-id="5f280-103">Retorna uma lista de todos os farms de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f280-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="5f280-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f280-104">SYNTAX</span></span>

### <span data-ttu-id="5f280-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f280-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5f280-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5f280-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5f280-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="5f280-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5f280-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f280-108">DESCRIPTION</span></span>
<span data-ttu-id="5f280-109">Retorna uma lista de todos os farms de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f280-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="5f280-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f280-110">EXAMPLES</span></span>

### <span data-ttu-id="5f280-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f280-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="5f280-112">Obter a lista de todos os farms de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f280-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="5f280-113">OS</span><span class="sxs-lookup"><span data-stu-id="5f280-113">PARAMETERS</span></span>

### <span data-ttu-id="5f280-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f280-114">-Name</span></span>
<span data-ttu-id="5f280-115">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="5f280-115">Farm Id.</span></span>

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

### <span data-ttu-id="5f280-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f280-116">-ResourceGroupName</span></span>
<span data-ttu-id="5f280-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f280-117">Resource group name.</span></span>

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

### <span data-ttu-id="5f280-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f280-118">-ResourceId</span></span>
<span data-ttu-id="5f280-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="5f280-119">The resource id.</span></span>

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

### <span data-ttu-id="5f280-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="5f280-120">-Skip</span></span>
<span data-ttu-id="5f280-121">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5f280-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5f280-122">-Início</span><span class="sxs-lookup"><span data-stu-id="5f280-122">-Top</span></span>
<span data-ttu-id="5f280-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5f280-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5f280-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="5f280-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5f280-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f280-125">CommonParameters</span></span>
<span data-ttu-id="5f280-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f280-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f280-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f280-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f280-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f280-128">INPUTS</span></span>

## <span data-ttu-id="5f280-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f280-129">OUTPUTS</span></span>

### <span data-ttu-id="5f280-130">Microsoft. AzureStack. Management. Storage. admin. Models. farm</span><span class="sxs-lookup"><span data-stu-id="5f280-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="5f280-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f280-131">NOTES</span></span>

## <span data-ttu-id="5f280-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f280-132">RELATED LINKS</span></span>
