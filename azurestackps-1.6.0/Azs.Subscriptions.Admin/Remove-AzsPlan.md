---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa4bd73f9300daf8ca17e3a11d884e06e9852234
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601722"
---
# <span data-ttu-id="723d1-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="723d1-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="723d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="723d1-102">SYNOPSIS</span></span>
<span data-ttu-id="723d1-103">Remove o plano especificado</span><span class="sxs-lookup"><span data-stu-id="723d1-103">Removes the specified plan</span></span>

## <span data-ttu-id="723d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="723d1-104">SYNTAX</span></span>

### <span data-ttu-id="723d1-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="723d1-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="723d1-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="723d1-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723d1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="723d1-107">DESCRIPTION</span></span>
<span data-ttu-id="723d1-108">Remove o plano especificado</span><span class="sxs-lookup"><span data-stu-id="723d1-108">Removes the specified plan</span></span>

## <span data-ttu-id="723d1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="723d1-109">EXAMPLES</span></span>

### <span data-ttu-id="723d1-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="723d1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="723d1-111">Remove o plano especificado</span><span class="sxs-lookup"><span data-stu-id="723d1-111">Removes the specified plan</span></span>

## <span data-ttu-id="723d1-112">OS</span><span class="sxs-lookup"><span data-stu-id="723d1-112">PARAMETERS</span></span>

### <span data-ttu-id="723d1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="723d1-113">-Force</span></span>
<span data-ttu-id="723d1-114">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="723d1-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="723d1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="723d1-115">-Name</span></span>
<span data-ttu-id="723d1-116">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="723d1-116">Name of the plan.</span></span>

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

### <span data-ttu-id="723d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="723d1-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="723d1-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="723d1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="723d1-119">-ResourceId</span></span>
<span data-ttu-id="723d1-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="723d1-120">The resource id.</span></span>

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

### <span data-ttu-id="723d1-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="723d1-121">-Confirm</span></span>
<span data-ttu-id="723d1-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="723d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723d1-123">-WhatIf</span></span>
<span data-ttu-id="723d1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="723d1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="723d1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="723d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="723d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723d1-126">CommonParameters</span></span>
<span data-ttu-id="723d1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723d1-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723d1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="723d1-129">INPUTS</span></span>

## <span data-ttu-id="723d1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="723d1-130">OUTPUTS</span></span>

## <span data-ttu-id="723d1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="723d1-131">NOTES</span></span>

## <span data-ttu-id="723d1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="723d1-132">RELATED LINKS</span></span>

