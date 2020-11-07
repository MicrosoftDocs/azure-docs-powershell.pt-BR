---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774991"
---
# <span data-ttu-id="03c45-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="03c45-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="03c45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03c45-102">SYNOPSIS</span></span>
<span data-ttu-id="03c45-103">Exclui uma imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03c45-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="03c45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03c45-104">SYNTAX</span></span>

### <span data-ttu-id="03c45-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="03c45-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c45-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="03c45-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c45-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03c45-107">DESCRIPTION</span></span>
<span data-ttu-id="03c45-108">Exclui a imagem de extensão da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="03c45-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="03c45-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03c45-109">EXAMPLES</span></span>

### <span data-ttu-id="03c45-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03c45-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="03c45-111">Remover uma extensão de imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="03c45-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="03c45-112">OS</span><span class="sxs-lookup"><span data-stu-id="03c45-112">PARAMETERS</span></span>

### <span data-ttu-id="03c45-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03c45-113">-Force</span></span>
<span data-ttu-id="03c45-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="03c45-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="03c45-115">-Local</span><span class="sxs-lookup"><span data-stu-id="03c45-115">-Location</span></span>
<span data-ttu-id="03c45-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="03c45-116">Location of the resource.</span></span>

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

### <span data-ttu-id="03c45-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="03c45-117">-Publisher</span></span>
<span data-ttu-id="03c45-118">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="03c45-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="03c45-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03c45-119">-ResourceId</span></span>
<span data-ttu-id="03c45-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="03c45-120">The resource id.</span></span>

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

### <span data-ttu-id="03c45-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="03c45-121">-Type</span></span>
<span data-ttu-id="03c45-122">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="03c45-122">Type of extension.</span></span>

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

### <span data-ttu-id="03c45-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="03c45-123">-Version</span></span>
<span data-ttu-id="03c45-124">A versão da imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03c45-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="03c45-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03c45-125">-Confirm</span></span>
<span data-ttu-id="03c45-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c45-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c45-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c45-127">-WhatIf</span></span>
<span data-ttu-id="03c45-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03c45-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c45-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03c45-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c45-130">CommonParameters</span></span>
<span data-ttu-id="03c45-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c45-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c45-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c45-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03c45-133">INPUTS</span></span>

## <span data-ttu-id="03c45-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03c45-134">OUTPUTS</span></span>

## <span data-ttu-id="03c45-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03c45-135">NOTES</span></span>

## <span data-ttu-id="03c45-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03c45-136">RELATED LINKS</span></span>

