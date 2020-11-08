---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2020
ms.locfileid: "94115133"
---
# <span data-ttu-id="92c8c-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="92c8c-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="92c8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="92c8c-103">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="92c8c-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="92c8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92c8c-104">SYNTAX</span></span>

### <span data-ttu-id="92c8c-105">Products_Download (padrão)</span><span class="sxs-lookup"><span data-stu-id="92c8c-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c8c-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="92c8c-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92c8c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92c8c-107">DESCRIPTION</span></span>
<span data-ttu-id="92c8c-108">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="92c8c-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="92c8c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92c8c-109">EXAMPLES</span></span>

### <span data-ttu-id="92c8c-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="92c8c-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="92c8c-111">Baixar um produto do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="92c8c-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="92c8c-112">OS</span><span class="sxs-lookup"><span data-stu-id="92c8c-112">PARAMETERS</span></span>

### <span data-ttu-id="92c8c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="92c8c-113">-Name</span></span>
<span data-ttu-id="92c8c-114">Nome do produto</span><span class="sxs-lookup"><span data-stu-id="92c8c-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-115">-Activationname</span><span class="sxs-lookup"><span data-stu-id="92c8c-115">-ActivationName</span></span>
<span data-ttu-id="92c8c-116">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="92c8c-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="92c8c-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="92c8c-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92c8c-119">-ResourceId</span></span>
<span data-ttu-id="92c8c-120">Identificador de recurso do produto Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="92c8c-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="92c8c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92c8c-121">-AsJob</span></span>
<span data-ttu-id="92c8c-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="92c8c-122">Run asynchronous as a job and return the job object.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="92c8c-123">-Force</span></span>
<span data-ttu-id="92c8c-124">Parâmetro de opção que não pede confirmação</span><span class="sxs-lookup"><span data-stu-id="92c8c-124">Switch parameter not to ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c8c-125">-WhatIf</span></span>
<span data-ttu-id="92c8c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92c8c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c8c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92c8c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="92c8c-128">-Confirm</span></span>
<span data-ttu-id="92c8c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c8c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c8c-130">CommonParameters</span></span>
<span data-ttu-id="92c8c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c8c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c8c-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c8c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c8c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92c8c-133">INPUTS</span></span>

## <span data-ttu-id="92c8c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92c8c-134">OUTPUTS</span></span>

## <span data-ttu-id="92c8c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92c8c-135">NOTES</span></span>

## <span data-ttu-id="92c8c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92c8c-136">RELATED LINKS</span></span>
