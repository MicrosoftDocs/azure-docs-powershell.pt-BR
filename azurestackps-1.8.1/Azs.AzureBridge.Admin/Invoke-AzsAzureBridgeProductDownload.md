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
ms.locfileid: "93786666"
---
# <span data-ttu-id="2e92e-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="2e92e-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="2e92e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e92e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e92e-103">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2e92e-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="2e92e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e92e-104">SYNTAX</span></span>

### <span data-ttu-id="2e92e-105">Products_Download (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e92e-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e92e-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="2e92e-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e92e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e92e-107">DESCRIPTION</span></span>
<span data-ttu-id="2e92e-108">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2e92e-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="2e92e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e92e-109">EXAMPLES</span></span>

### <span data-ttu-id="2e92e-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="2e92e-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="2e92e-111">Baixar um produto do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="2e92e-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="2e92e-112">OS</span><span class="sxs-lookup"><span data-stu-id="2e92e-112">PARAMETERS</span></span>

### <span data-ttu-id="2e92e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e92e-113">-Name</span></span>
<span data-ttu-id="2e92e-114">Nome do produto</span><span class="sxs-lookup"><span data-stu-id="2e92e-114">Name of the product</span></span>

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

### <span data-ttu-id="2e92e-115">-Activationname</span><span class="sxs-lookup"><span data-stu-id="2e92e-115">-ActivationName</span></span>
<span data-ttu-id="2e92e-116">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="2e92e-116">Name of the activation.</span></span>

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

### <span data-ttu-id="2e92e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e92e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e92e-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="2e92e-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2e92e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e92e-119">-ResourceId</span></span>
<span data-ttu-id="2e92e-120">Identificador de recurso do produto Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="2e92e-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="2e92e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e92e-121">-AsJob</span></span>
<span data-ttu-id="2e92e-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2e92e-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="2e92e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2e92e-123">-Force</span></span>
<span data-ttu-id="2e92e-124">Parâmetro de opção que não pede confirmação</span><span class="sxs-lookup"><span data-stu-id="2e92e-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="2e92e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e92e-125">-WhatIf</span></span>
<span data-ttu-id="2e92e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e92e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e92e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e92e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e92e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e92e-128">-Confirm</span></span>
<span data-ttu-id="2e92e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e92e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e92e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e92e-130">CommonParameters</span></span>
<span data-ttu-id="2e92e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e92e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e92e-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e92e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e92e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e92e-133">INPUTS</span></span>

## <span data-ttu-id="2e92e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e92e-134">OUTPUTS</span></span>

## <span data-ttu-id="2e92e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e92e-135">NOTES</span></span>

## <span data-ttu-id="2e92e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e92e-136">RELATED LINKS</span></span>
