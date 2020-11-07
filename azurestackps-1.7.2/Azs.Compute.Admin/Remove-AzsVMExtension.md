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
ms.locfileid: "93774507"
---
# <span data-ttu-id="53ee8-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="53ee8-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="53ee8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="53ee8-103">Exclui uma imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="53ee8-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="53ee8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ee8-104">SYNTAX</span></span>

### <span data-ttu-id="53ee8-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="53ee8-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53ee8-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="53ee8-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53ee8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53ee8-107">DESCRIPTION</span></span>
<span data-ttu-id="53ee8-108">Exclui a imagem de extensão da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="53ee8-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="53ee8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53ee8-109">EXAMPLES</span></span>

### <span data-ttu-id="53ee8-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="53ee8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="53ee8-111">Remover uma extensão de imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="53ee8-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="53ee8-112">OS</span><span class="sxs-lookup"><span data-stu-id="53ee8-112">PARAMETERS</span></span>

### <span data-ttu-id="53ee8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="53ee8-113">-Force</span></span>
<span data-ttu-id="53ee8-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="53ee8-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="53ee8-115">-Local</span><span class="sxs-lookup"><span data-stu-id="53ee8-115">-Location</span></span>
<span data-ttu-id="53ee8-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="53ee8-116">Location of the resource.</span></span>

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

### <span data-ttu-id="53ee8-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="53ee8-117">-Publisher</span></span>
<span data-ttu-id="53ee8-118">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="53ee8-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="53ee8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53ee8-119">-ResourceId</span></span>
<span data-ttu-id="53ee8-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="53ee8-120">The resource id.</span></span>

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

### <span data-ttu-id="53ee8-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="53ee8-121">-Type</span></span>
<span data-ttu-id="53ee8-122">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="53ee8-122">Type of extension.</span></span>

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

### <span data-ttu-id="53ee8-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="53ee8-123">-Version</span></span>
<span data-ttu-id="53ee8-124">A versão da imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="53ee8-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="53ee8-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53ee8-125">-Confirm</span></span>
<span data-ttu-id="53ee8-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53ee8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53ee8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53ee8-127">-WhatIf</span></span>
<span data-ttu-id="53ee8-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53ee8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53ee8-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53ee8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53ee8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ee8-130">CommonParameters</span></span>
<span data-ttu-id="53ee8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ee8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ee8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ee8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ee8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53ee8-133">INPUTS</span></span>

## <span data-ttu-id="53ee8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53ee8-134">OUTPUTS</span></span>

## <span data-ttu-id="53ee8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53ee8-135">NOTES</span></span>

## <span data-ttu-id="53ee8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53ee8-136">RELATED LINKS</span></span>

