---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775137"
---
# <span data-ttu-id="45492-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="45492-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="45492-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45492-102">SYNOPSIS</span></span>
<span data-ttu-id="45492-103">Obtenha a lista de ofertas como administrador.</span><span class="sxs-lookup"><span data-stu-id="45492-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="45492-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45492-104">SYNTAX</span></span>

### <span data-ttu-id="45492-105">ListAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="45492-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="45492-106">Obter</span><span class="sxs-lookup"><span data-stu-id="45492-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="45492-107">Programação</span><span class="sxs-lookup"><span data-stu-id="45492-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="45492-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="45492-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="45492-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45492-109">DESCRIPTION</span></span>
<span data-ttu-id="45492-110">Obter a lista de ofertas.</span><span class="sxs-lookup"><span data-stu-id="45492-110">Get the list of offers.</span></span>

## <span data-ttu-id="45492-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45492-111">EXAMPLES</span></span>

### <span data-ttu-id="45492-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45492-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="45492-113">Obtenha a lista de ofertas como administrador.</span><span class="sxs-lookup"><span data-stu-id="45492-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="45492-114">OS</span><span class="sxs-lookup"><span data-stu-id="45492-114">PARAMETERS</span></span>

### <span data-ttu-id="45492-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="45492-115">-Name</span></span>
<span data-ttu-id="45492-116">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="45492-116">Name of an offer.</span></span>

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

### <span data-ttu-id="45492-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45492-117">-ResourceGroupName</span></span>
<span data-ttu-id="45492-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="45492-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45492-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45492-119">-ResourceId</span></span>
<span data-ttu-id="45492-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="45492-120">The resource id.</span></span>

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

### <span data-ttu-id="45492-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="45492-121">-Skip</span></span>
<span data-ttu-id="45492-122">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="45492-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45492-123">-Início</span><span class="sxs-lookup"><span data-stu-id="45492-123">-Top</span></span>
<span data-ttu-id="45492-124">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="45492-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45492-125">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="45492-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45492-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45492-126">CommonParameters</span></span>
<span data-ttu-id="45492-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45492-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45492-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45492-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45492-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45492-129">INPUTS</span></span>

## <span data-ttu-id="45492-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45492-130">OUTPUTS</span></span>

### <span data-ttu-id="45492-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="45492-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="45492-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45492-132">NOTES</span></span>

## <span data-ttu-id="45492-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45492-133">RELATED LINKS</span></span>

