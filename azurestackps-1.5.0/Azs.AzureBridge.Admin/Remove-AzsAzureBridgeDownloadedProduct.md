---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93611176"
---
# <span data-ttu-id="41334-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="41334-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="41334-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41334-102">SYNOPSIS</span></span>
<span data-ttu-id="41334-103">Excluir um produto baixado do Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="41334-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="41334-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41334-104">SYNTAX</span></span>

### <span data-ttu-id="41334-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="41334-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41334-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="41334-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41334-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41334-107">DESCRIPTION</span></span>
<span data-ttu-id="41334-108">Excluir um produto baixado do Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="41334-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="41334-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41334-109">EXAMPLES</span></span>

### <span data-ttu-id="41334-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41334-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="41334-111">Excluir um produto baixado do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="41334-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="41334-112">OS</span><span class="sxs-lookup"><span data-stu-id="41334-112">PARAMETERS</span></span>

### <span data-ttu-id="41334-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="41334-113">-ActivationName</span></span>
<span data-ttu-id="41334-114">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="41334-114">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41334-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41334-115">-AsJob</span></span>
<span data-ttu-id="41334-116">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="41334-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="41334-117">-Force</span><span class="sxs-lookup"><span data-stu-id="41334-117">-Force</span></span>
<span data-ttu-id="41334-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="41334-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="41334-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="41334-119">-Name</span></span>
<span data-ttu-id="41334-120">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="41334-120">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41334-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41334-121">-ResourceGroupName</span></span>
<span data-ttu-id="41334-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="41334-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41334-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41334-123">-ResourceId</span></span>
<span data-ttu-id="41334-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="41334-124">The resource id.</span></span>

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

### <span data-ttu-id="41334-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41334-125">-Confirm</span></span>
<span data-ttu-id="41334-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41334-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41334-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41334-127">-WhatIf</span></span>
<span data-ttu-id="41334-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41334-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41334-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41334-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41334-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41334-130">CommonParameters</span></span>
<span data-ttu-id="41334-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41334-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41334-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41334-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41334-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41334-133">INPUTS</span></span>

## <span data-ttu-id="41334-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41334-134">OUTPUTS</span></span>

### <span data-ttu-id="41334-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="41334-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="41334-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41334-136">NOTES</span></span>

## <span data-ttu-id="41334-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41334-137">RELATED LINKS</span></span>

