---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "93947341"
---
# <span data-ttu-id="c1ccd-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="c1ccd-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="c1ccd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ccd-103">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="c1ccd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1ccd-104">SYNTAX</span></span>

### <span data-ttu-id="c1ccd-105">Products_Download (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1ccd-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ccd-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="c1ccd-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ccd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1ccd-107">DESCRIPTION</span></span>
<span data-ttu-id="c1ccd-108">Baixa um produto do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="c1ccd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1ccd-109">EXAMPLES</span></span>

### <span data-ttu-id="c1ccd-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1ccd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="c1ccd-111">Baixar um produto do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="c1ccd-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="c1ccd-112">OS</span><span class="sxs-lookup"><span data-stu-id="c1ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="c1ccd-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="c1ccd-113">-ActivationName</span></span>
<span data-ttu-id="c1ccd-114">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ccd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1ccd-115">-AsJob</span></span>
<span data-ttu-id="c1ccd-116">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c1ccd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c1ccd-117">-Force</span></span>
<span data-ttu-id="c1ccd-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c1ccd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1ccd-119">-Name</span></span>
<span data-ttu-id="c1ccd-120">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ccd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ccd-121">-ResourceGroupName</span></span>
<span data-ttu-id="c1ccd-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ccd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1ccd-123">-ResourceId</span></span>
<span data-ttu-id="c1ccd-124">Identificador de recurso do produto Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-124">Resource identifier for azure bridge product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ccd-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c1ccd-125">-Confirm</span></span>
<span data-ttu-id="c1ccd-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ccd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ccd-127">-WhatIf</span></span>
<span data-ttu-id="c1ccd-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ccd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ccd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ccd-130">CommonParameters</span></span>
<span data-ttu-id="c1ccd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ccd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ccd-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ccd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ccd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1ccd-133">INPUTS</span></span>

## <span data-ttu-id="c1ccd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1ccd-134">OUTPUTS</span></span>

## <span data-ttu-id="c1ccd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1ccd-135">NOTES</span></span>

## <span data-ttu-id="c1ccd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1ccd-136">RELATED LINKS</span></span>

