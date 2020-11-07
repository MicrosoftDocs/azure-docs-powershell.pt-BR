---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774577"
---
# <span data-ttu-id="e88be-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="e88be-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="e88be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e88be-102">SYNOPSIS</span></span>
<span data-ttu-id="e88be-103">Remove o plano especificado</span><span class="sxs-lookup"><span data-stu-id="e88be-103">Removes the specified plan</span></span>

## <span data-ttu-id="e88be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e88be-104">SYNTAX</span></span>

### <span data-ttu-id="e88be-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="e88be-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88be-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="e88be-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88be-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e88be-107">DESCRIPTION</span></span>
<span data-ttu-id="e88be-108">Remove o plano especificado</span><span class="sxs-lookup"><span data-stu-id="e88be-108">Removes the specified plan</span></span>

## <span data-ttu-id="e88be-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e88be-109">EXAMPLES</span></span>

### <span data-ttu-id="e88be-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e88be-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="e88be-111">Remove o plano especificado</span><span class="sxs-lookup"><span data-stu-id="e88be-111">Removes the specified plan</span></span>

## <span data-ttu-id="e88be-112">OS</span><span class="sxs-lookup"><span data-stu-id="e88be-112">PARAMETERS</span></span>

### <span data-ttu-id="e88be-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e88be-113">-Force</span></span>
<span data-ttu-id="e88be-114">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="e88be-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e88be-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e88be-115">-Name</span></span>
<span data-ttu-id="e88be-116">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="e88be-116">Name of the plan.</span></span>

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

### <span data-ttu-id="e88be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88be-117">-ResourceGroupName</span></span>
<span data-ttu-id="e88be-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="e88be-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e88be-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e88be-119">-ResourceId</span></span>
<span data-ttu-id="e88be-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e88be-120">The resource id.</span></span>

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

### <span data-ttu-id="e88be-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e88be-121">-Confirm</span></span>
<span data-ttu-id="e88be-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e88be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88be-123">-WhatIf</span></span>
<span data-ttu-id="e88be-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e88be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88be-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e88be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88be-126">CommonParameters</span></span>
<span data-ttu-id="e88be-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88be-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88be-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88be-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e88be-129">INPUTS</span></span>

## <span data-ttu-id="e88be-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e88be-130">OUTPUTS</span></span>

## <span data-ttu-id="e88be-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e88be-131">NOTES</span></span>

## <span data-ttu-id="e88be-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e88be-132">RELATED LINKS</span></span>

