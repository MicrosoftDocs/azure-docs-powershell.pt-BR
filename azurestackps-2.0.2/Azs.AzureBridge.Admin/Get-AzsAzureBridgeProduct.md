---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edcc9bea35e1675b42a04c2b4e804c48ba052742
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "93947321"
---
# <span data-ttu-id="46fff-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="46fff-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="46fff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46fff-102">SYNOPSIS</span></span>
<span data-ttu-id="46fff-103">Retorna uma lista de produtos disponíveis para download do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="46fff-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="46fff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46fff-104">SYNTAX</span></span>

### <span data-ttu-id="46fff-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="46fff-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="46fff-106">Obter</span><span class="sxs-lookup"><span data-stu-id="46fff-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="46fff-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="46fff-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="46fff-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46fff-108">DESCRIPTION</span></span>
<span data-ttu-id="46fff-109">Retorna uma lista de produtos disponíveis para download do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="46fff-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="46fff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46fff-110">EXAMPLES</span></span>

### <span data-ttu-id="46fff-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46fff-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="46fff-112">Obtenha uma lista de produtos disponíveis para download no Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="46fff-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="46fff-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="46fff-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="46fff-114">Obtenha uma informação do produto disponível para download pelo nome do Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="46fff-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="46fff-115">OS</span><span class="sxs-lookup"><span data-stu-id="46fff-115">PARAMETERS</span></span>

### <span data-ttu-id="46fff-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="46fff-116">-ActivationName</span></span>
<span data-ttu-id="46fff-117">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="46fff-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fff-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="46fff-118">-Name</span></span>
<span data-ttu-id="46fff-119">Nome do produto.</span><span class="sxs-lookup"><span data-stu-id="46fff-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46fff-120">-ResourceGroupName</span></span>
<span data-ttu-id="46fff-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="46fff-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46fff-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46fff-122">-ResourceId</span></span>
<span data-ttu-id="46fff-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="46fff-123">The resource id.</span></span>

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

### <span data-ttu-id="46fff-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="46fff-124">-Skip</span></span>
<span data-ttu-id="46fff-125">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="46fff-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="46fff-126">-Início</span><span class="sxs-lookup"><span data-stu-id="46fff-126">-Top</span></span>
<span data-ttu-id="46fff-127">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="46fff-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="46fff-128">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="46fff-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="46fff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fff-129">CommonParameters</span></span>
<span data-ttu-id="46fff-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46fff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fff-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46fff-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fff-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46fff-132">INPUTS</span></span>

## <span data-ttu-id="46fff-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46fff-133">OUTPUTS</span></span>

### <span data-ttu-id="46fff-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="46fff-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="46fff-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46fff-135">NOTES</span></span>

## <span data-ttu-id="46fff-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46fff-136">RELATED LINKS</span></span>

