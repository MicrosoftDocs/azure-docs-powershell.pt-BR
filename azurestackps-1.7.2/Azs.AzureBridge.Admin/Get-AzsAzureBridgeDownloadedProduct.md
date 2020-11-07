---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93786655"
---
# <span data-ttu-id="d9986-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="d9986-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="d9986-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9986-102">SYNOPSIS</span></span>
<span data-ttu-id="d9986-103">Retorna uma lista de produtos baixados do Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="d9986-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="d9986-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9986-104">SYNTAX</span></span>

### <span data-ttu-id="d9986-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9986-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d9986-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d9986-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d9986-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="d9986-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d9986-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9986-108">DESCRIPTION</span></span>
<span data-ttu-id="d9986-109">Retorna uma lista de produtos baixados do Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="d9986-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="d9986-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9986-110">EXAMPLES</span></span>

### <span data-ttu-id="d9986-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9986-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="d9986-112">Obter uma lista de produtos baixados do Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="d9986-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="d9986-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9986-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="d9986-114">Obter um produto do Azure Bridge baixado por nome</span><span class="sxs-lookup"><span data-stu-id="d9986-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="d9986-115">OS</span><span class="sxs-lookup"><span data-stu-id="d9986-115">PARAMETERS</span></span>

### <span data-ttu-id="d9986-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="d9986-116">-ActivationName</span></span>
<span data-ttu-id="d9986-117">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="d9986-117">Name of the activation.</span></span>

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

### <span data-ttu-id="d9986-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9986-118">-Name</span></span>
<span data-ttu-id="d9986-119">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="d9986-119">Name of the product.</span></span>

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

### <span data-ttu-id="d9986-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9986-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9986-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="d9986-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d9986-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9986-122">-ResourceId</span></span>
<span data-ttu-id="d9986-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d9986-123">The resource id.</span></span>

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

### <span data-ttu-id="d9986-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="d9986-124">-Skip</span></span>
<span data-ttu-id="d9986-125">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d9986-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d9986-126">-Início</span><span class="sxs-lookup"><span data-stu-id="d9986-126">-Top</span></span>
<span data-ttu-id="d9986-127">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d9986-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d9986-128">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d9986-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d9986-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9986-129">CommonParameters</span></span>
<span data-ttu-id="d9986-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9986-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9986-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9986-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9986-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9986-132">INPUTS</span></span>

## <span data-ttu-id="d9986-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9986-133">OUTPUTS</span></span>

### <span data-ttu-id="d9986-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="d9986-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="d9986-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9986-135">NOTES</span></span>

## <span data-ttu-id="d9986-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9986-136">RELATED LINKS</span></span>

