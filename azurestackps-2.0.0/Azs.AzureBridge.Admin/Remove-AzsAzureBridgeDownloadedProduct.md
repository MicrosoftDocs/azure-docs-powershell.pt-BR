---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d75764209b56ed0cc05d80e00581de3f982e435
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "93947329"
---
# <span data-ttu-id="8ac7f-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="8ac7f-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="8ac7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ac7f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac7f-103">Excluir um produto baixado do Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="8ac7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ac7f-104">SYNTAX</span></span>

### <span data-ttu-id="8ac7f-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ac7f-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac7f-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="8ac7f-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ac7f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ac7f-107">DESCRIPTION</span></span>
<span data-ttu-id="8ac7f-108">Excluir um produto baixado do Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="8ac7f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ac7f-109">EXAMPLES</span></span>

### <span data-ttu-id="8ac7f-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ac7f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="8ac7f-111">Excluir um produto baixado do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="8ac7f-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="8ac7f-112">OS</span><span class="sxs-lookup"><span data-stu-id="8ac7f-112">PARAMETERS</span></span>

### <span data-ttu-id="8ac7f-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="8ac7f-113">-ActivationName</span></span>
<span data-ttu-id="8ac7f-114">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac7f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ac7f-115">-AsJob</span></span>
<span data-ttu-id="8ac7f-116">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8ac7f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ac7f-117">-Force</span></span>
<span data-ttu-id="8ac7f-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8ac7f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ac7f-119">-Name</span></span>
<span data-ttu-id="8ac7f-120">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac7f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac7f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ac7f-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac7f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac7f-123">-ResourceId</span></span>
<span data-ttu-id="8ac7f-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-124">The resource id.</span></span>

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

### <span data-ttu-id="8ac7f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ac7f-125">-Confirm</span></span>
<span data-ttu-id="8ac7f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac7f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac7f-127">-WhatIf</span></span>
<span data-ttu-id="8ac7f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ac7f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac7f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac7f-130">CommonParameters</span></span>
<span data-ttu-id="8ac7f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac7f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac7f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac7f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac7f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ac7f-133">INPUTS</span></span>

## <span data-ttu-id="8ac7f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ac7f-134">OUTPUTS</span></span>

### <span data-ttu-id="8ac7f-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="8ac7f-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="8ac7f-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ac7f-136">NOTES</span></span>

## <span data-ttu-id="8ac7f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ac7f-137">RELATED LINKS</span></span>

