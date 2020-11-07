---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ebe9c71560f18ba9e4d7fb52514a4f5b7007bfb
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93786652"
---
# <span data-ttu-id="fb053-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="fb053-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="fb053-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb053-102">SYNOPSIS</span></span>
<span data-ttu-id="fb053-103">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fb053-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="fb053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb053-104">SYNTAX</span></span>

### <span data-ttu-id="fb053-105">Products_Download (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb053-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb053-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="fb053-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb053-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb053-107">DESCRIPTION</span></span>
<span data-ttu-id="fb053-108">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fb053-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="fb053-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb053-109">EXAMPLES</span></span>

### <span data-ttu-id="fb053-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fb053-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="fb053-111">Baixar um produto do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="fb053-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="fb053-112">OS</span><span class="sxs-lookup"><span data-stu-id="fb053-112">PARAMETERS</span></span>

### <span data-ttu-id="fb053-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="fb053-113">-ActivationName</span></span>
<span data-ttu-id="fb053-114">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="fb053-114">Name of the activation.</span></span>

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

### <span data-ttu-id="fb053-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb053-115">-AsJob</span></span>
<span data-ttu-id="fb053-116">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fb053-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fb053-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fb053-117">-Force</span></span>
<span data-ttu-id="fb053-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="fb053-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fb053-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb053-119">-Name</span></span>
<span data-ttu-id="fb053-120">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="fb053-120">Name of the product.</span></span>

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

### <span data-ttu-id="fb053-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb053-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb053-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="fb053-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="fb053-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb053-123">-ResourceId</span></span>
<span data-ttu-id="fb053-124">Identificador de recurso do produto Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="fb053-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="fb053-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb053-125">-Confirm</span></span>
<span data-ttu-id="fb053-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb053-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb053-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb053-127">-WhatIf</span></span>
<span data-ttu-id="fb053-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb053-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb053-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb053-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb053-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb053-130">CommonParameters</span></span>
<span data-ttu-id="fb053-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb053-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb053-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb053-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb053-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb053-133">INPUTS</span></span>

## <span data-ttu-id="fb053-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb053-134">OUTPUTS</span></span>

## <span data-ttu-id="fb053-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb053-135">NOTES</span></span>

## <span data-ttu-id="fb053-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb053-136">RELATED LINKS</span></span>

