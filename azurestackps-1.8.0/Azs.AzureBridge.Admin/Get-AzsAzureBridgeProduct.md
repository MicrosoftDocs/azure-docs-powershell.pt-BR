---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93786639"
---
# <span data-ttu-id="957ef-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="957ef-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="957ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="957ef-102">SYNOPSIS</span></span>
<span data-ttu-id="957ef-103">Retorna uma lista de produtos disponíveis para download do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="957ef-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="957ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="957ef-104">SYNTAX</span></span>

### <span data-ttu-id="957ef-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="957ef-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="957ef-106">Obter</span><span class="sxs-lookup"><span data-stu-id="957ef-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="957ef-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="957ef-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="957ef-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="957ef-108">DESCRIPTION</span></span>
<span data-ttu-id="957ef-109">Retorna uma lista de produtos disponíveis para download do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="957ef-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="957ef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="957ef-110">EXAMPLES</span></span>

### <span data-ttu-id="957ef-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="957ef-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="957ef-112">Obtenha uma lista de produtos disponíveis para download no Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="957ef-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="957ef-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="957ef-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="957ef-114">Obtenha uma informação do produto disponível para download pelo nome do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="957ef-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="957ef-115">OS</span><span class="sxs-lookup"><span data-stu-id="957ef-115">PARAMETERS</span></span>

### <span data-ttu-id="957ef-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="957ef-116">-Name</span></span>
<span data-ttu-id="957ef-117">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="957ef-117">Name of the product.</span></span>

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

### <span data-ttu-id="957ef-118">-Activationname</span><span class="sxs-lookup"><span data-stu-id="957ef-118">-ActivationName</span></span>
<span data-ttu-id="957ef-119">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="957ef-119">Name of the activation.</span></span>

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

### <span data-ttu-id="957ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="957ef-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="957ef-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="957ef-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="957ef-122">-ResourceId</span></span>
<span data-ttu-id="957ef-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="957ef-123">The resource id.</span></span>

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

### <span data-ttu-id="957ef-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="957ef-124">-Skip</span></span>
<span data-ttu-id="957ef-125">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="957ef-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="957ef-126">-Início</span><span class="sxs-lookup"><span data-stu-id="957ef-126">-Top</span></span>
<span data-ttu-id="957ef-127">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="957ef-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="957ef-128">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="957ef-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="957ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957ef-129">CommonParameters</span></span>
<span data-ttu-id="957ef-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="957ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957ef-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="957ef-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957ef-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="957ef-132">INPUTS</span></span>

## <span data-ttu-id="957ef-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="957ef-133">OUTPUTS</span></span>

### <span data-ttu-id="957ef-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="957ef-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="957ef-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="957ef-135">NOTES</span></span>

## <span data-ttu-id="957ef-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="957ef-136">RELATED LINKS</span></span>
