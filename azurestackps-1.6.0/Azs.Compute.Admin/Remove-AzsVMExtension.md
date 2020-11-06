---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425626"
---
# <span data-ttu-id="af21a-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="af21a-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="af21a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af21a-102">SYNOPSIS</span></span>
<span data-ttu-id="af21a-103">Exclui uma imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="af21a-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="af21a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af21a-104">SYNTAX</span></span>

### <span data-ttu-id="af21a-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="af21a-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af21a-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="af21a-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af21a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af21a-107">DESCRIPTION</span></span>
<span data-ttu-id="af21a-108">Exclui a imagem de extensão da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="af21a-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="af21a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af21a-109">EXAMPLES</span></span>

### <span data-ttu-id="af21a-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="af21a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="af21a-111">Remover uma extensão de imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="af21a-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="af21a-112">OS</span><span class="sxs-lookup"><span data-stu-id="af21a-112">PARAMETERS</span></span>

### <span data-ttu-id="af21a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="af21a-113">-Force</span></span>
<span data-ttu-id="af21a-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="af21a-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="af21a-115">-Local</span><span class="sxs-lookup"><span data-stu-id="af21a-115">-Location</span></span>
<span data-ttu-id="af21a-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="af21a-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af21a-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="af21a-117">-Publisher</span></span>
<span data-ttu-id="af21a-118">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="af21a-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="af21a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af21a-119">-ResourceId</span></span>
<span data-ttu-id="af21a-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="af21a-120">The resource id.</span></span>

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

### <span data-ttu-id="af21a-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="af21a-121">-Type</span></span>
<span data-ttu-id="af21a-122">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="af21a-122">Type of extension.</span></span>

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

### <span data-ttu-id="af21a-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="af21a-123">-Version</span></span>
<span data-ttu-id="af21a-124">A versão da imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="af21a-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="af21a-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af21a-125">-Confirm</span></span>
<span data-ttu-id="af21a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af21a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af21a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af21a-127">-WhatIf</span></span>
<span data-ttu-id="af21a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af21a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af21a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af21a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af21a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af21a-130">CommonParameters</span></span>
<span data-ttu-id="af21a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af21a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af21a-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af21a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af21a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af21a-133">INPUTS</span></span>

## <span data-ttu-id="af21a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af21a-134">OUTPUTS</span></span>

## <span data-ttu-id="af21a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af21a-135">NOTES</span></span>

## <span data-ttu-id="af21a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af21a-136">RELATED LINKS</span></span>

