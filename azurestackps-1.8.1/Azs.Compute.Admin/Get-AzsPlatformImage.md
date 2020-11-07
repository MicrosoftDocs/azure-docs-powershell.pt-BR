---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775007"
---
# <span data-ttu-id="fc075-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="fc075-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="fc075-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc075-102">SYNOPSIS</span></span>
<span data-ttu-id="fc075-103">Retorna as imagens da máquina virtual carregadas no repositório de imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="fc075-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="fc075-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc075-104">SYNTAX</span></span>

### <span data-ttu-id="fc075-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc075-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc075-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fc075-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc075-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="fc075-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fc075-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc075-108">DESCRIPTION</span></span>
<span data-ttu-id="fc075-109">Retorna imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="fc075-109">Returns platform images.</span></span>

## <span data-ttu-id="fc075-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc075-110">EXAMPLES</span></span>

### <span data-ttu-id="fc075-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc075-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="fc075-112">Retorna as imagens da máquina virtual carregadas no repositório de imagens da plataforma no local local.</span><span class="sxs-lookup"><span data-stu-id="fc075-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="fc075-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc075-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="fc075-114">Obter uma imagem de plataforma específica.</span><span class="sxs-lookup"><span data-stu-id="fc075-114">Get a specific platform image.</span></span>

## <span data-ttu-id="fc075-115">OS</span><span class="sxs-lookup"><span data-stu-id="fc075-115">PARAMETERS</span></span>

### <span data-ttu-id="fc075-116">-Local</span><span class="sxs-lookup"><span data-stu-id="fc075-116">-Location</span></span>
<span data-ttu-id="fc075-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="fc075-117">Location of the resource.</span></span>

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

### <span data-ttu-id="fc075-118">-Oferta</span><span class="sxs-lookup"><span data-stu-id="fc075-118">-Offer</span></span>
<span data-ttu-id="fc075-119">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="fc075-119">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="fc075-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fc075-120">-Publisher</span></span>
<span data-ttu-id="fc075-121">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fc075-121">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="fc075-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc075-122">-ResourceId</span></span>
<span data-ttu-id="fc075-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="fc075-123">The resource id.</span></span>

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

### <span data-ttu-id="fc075-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="fc075-124">-Sku</span></span>
<span data-ttu-id="fc075-125">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="fc075-125">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="fc075-126">-Versão</span><span class="sxs-lookup"><span data-stu-id="fc075-126">-Version</span></span>
<span data-ttu-id="fc075-127">A versão da imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="fc075-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="fc075-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc075-128">CommonParameters</span></span>
<span data-ttu-id="fc075-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc075-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc075-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc075-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc075-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc075-131">INPUTS</span></span>

## <span data-ttu-id="fc075-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc075-132">OUTPUTS</span></span>

### <span data-ttu-id="fc075-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="fc075-133">PlatformImageObject</span></span>

## <span data-ttu-id="fc075-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc075-134">NOTES</span></span>

## <span data-ttu-id="fc075-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc075-135">RELATED LINKS</span></span>

