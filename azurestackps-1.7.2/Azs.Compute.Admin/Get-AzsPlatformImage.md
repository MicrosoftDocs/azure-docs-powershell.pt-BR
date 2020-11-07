---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773922"
---
# <span data-ttu-id="dbd91-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="dbd91-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="dbd91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbd91-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd91-103">Retorna as imagens da máquina virtual carregadas no repositório de imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="dbd91-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="dbd91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbd91-104">SYNTAX</span></span>

### <span data-ttu-id="dbd91-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="dbd91-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbd91-106">Obter</span><span class="sxs-lookup"><span data-stu-id="dbd91-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbd91-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="dbd91-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="dbd91-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbd91-108">DESCRIPTION</span></span>
<span data-ttu-id="dbd91-109">Retorna imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="dbd91-109">Returns platform images.</span></span>

## <span data-ttu-id="dbd91-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbd91-110">EXAMPLES</span></span>

### <span data-ttu-id="dbd91-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dbd91-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="dbd91-112">Retorna as imagens da máquina virtual carregadas no repositório de imagens da plataforma no local local.</span><span class="sxs-lookup"><span data-stu-id="dbd91-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="dbd91-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dbd91-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="dbd91-114">Obter uma imagem de plataforma específica.</span><span class="sxs-lookup"><span data-stu-id="dbd91-114">Get a specific platform image.</span></span>

## <span data-ttu-id="dbd91-115">OS</span><span class="sxs-lookup"><span data-stu-id="dbd91-115">PARAMETERS</span></span>

### <span data-ttu-id="dbd91-116">-Local</span><span class="sxs-lookup"><span data-stu-id="dbd91-116">-Location</span></span>
<span data-ttu-id="dbd91-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="dbd91-117">Location of the resource.</span></span>

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

### <span data-ttu-id="dbd91-118">-Oferta</span><span class="sxs-lookup"><span data-stu-id="dbd91-118">-Offer</span></span>
<span data-ttu-id="dbd91-119">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="dbd91-119">Name of the offer.</span></span>

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

### <span data-ttu-id="dbd91-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="dbd91-120">-Publisher</span></span>
<span data-ttu-id="dbd91-121">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="dbd91-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="dbd91-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd91-122">-ResourceId</span></span>
<span data-ttu-id="dbd91-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="dbd91-123">The resource id.</span></span>

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

### <span data-ttu-id="dbd91-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="dbd91-124">-Sku</span></span>
<span data-ttu-id="dbd91-125">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="dbd91-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="dbd91-126">-Versão</span><span class="sxs-lookup"><span data-stu-id="dbd91-126">-Version</span></span>
<span data-ttu-id="dbd91-127">A versão da imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="dbd91-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="dbd91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd91-128">CommonParameters</span></span>
<span data-ttu-id="dbd91-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd91-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd91-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd91-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbd91-131">INPUTS</span></span>

## <span data-ttu-id="dbd91-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbd91-132">OUTPUTS</span></span>

### <span data-ttu-id="dbd91-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="dbd91-133">PlatformImageObject</span></span>

## <span data-ttu-id="dbd91-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbd91-134">NOTES</span></span>

## <span data-ttu-id="dbd91-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbd91-135">RELATED LINKS</span></span>

