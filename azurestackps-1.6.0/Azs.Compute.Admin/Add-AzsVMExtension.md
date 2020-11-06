---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42181271e9295212f256cfc519e8ecc32eeae048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426184"
---
# <span data-ttu-id="def22-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="def22-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="def22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="def22-102">SYNOPSIS</span></span>
<span data-ttu-id="def22-103">Crie uma nova imagem de extensão de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="def22-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="def22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="def22-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="def22-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="def22-105">DESCRIPTION</span></span>
<span data-ttu-id="def22-106">Criar uma imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="def22-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="def22-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="def22-107">EXAMPLES</span></span>

### <span data-ttu-id="def22-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="def22-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="def22-109">Adicionar uma nova extensão de imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="def22-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="def22-110">OS</span><span class="sxs-lookup"><span data-stu-id="def22-110">PARAMETERS</span></span>

### <span data-ttu-id="def22-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="def22-111">-AsJob</span></span>
<span data-ttu-id="def22-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="def22-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="def22-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="def22-113">-ComputeRole</span></span>
<span data-ttu-id="def22-114">O tipo de função, IaaS ou PaaS, a extensão é compatível.</span><span class="sxs-lookup"><span data-stu-id="def22-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-115">-Force</span><span class="sxs-lookup"><span data-stu-id="def22-115">-Force</span></span>
<span data-ttu-id="def22-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="def22-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="def22-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="def22-117">-IsSystemExtension</span></span>
<span data-ttu-id="def22-118">Indica se a extensão é para o sistema.</span><span class="sxs-lookup"><span data-stu-id="def22-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="def22-119">-Local</span><span class="sxs-lookup"><span data-stu-id="def22-119">-Location</span></span>
<span data-ttu-id="def22-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="def22-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="def22-121">-Publisher</span></span>
<span data-ttu-id="def22-122">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="def22-122">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="def22-123">-SourceBlob</span></span>
<span data-ttu-id="def22-124">URI para pacote de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="def22-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="def22-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="def22-126">Verdadeiro se der suporte a várias extensões.</span><span class="sxs-lookup"><span data-stu-id="def22-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="def22-127">-Digite</span><span class="sxs-lookup"><span data-stu-id="def22-127">-Type</span></span>
<span data-ttu-id="def22-128">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="def22-128">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-129">-Versão</span><span class="sxs-lookup"><span data-stu-id="def22-129">-Version</span></span>
<span data-ttu-id="def22-130">A versão da extensão de imagem do computador vritual.</span><span class="sxs-lookup"><span data-stu-id="def22-130">The version of the vritual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="def22-131">-VmOsType</span></span>
<span data-ttu-id="def22-132">Destino do tipo de sistema operacional da máquina virtual necessária para implantar o manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="def22-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def22-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="def22-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="def22-134">Valor que indica se a extensão está habilitada para suporte ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="def22-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="def22-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="def22-135">-Confirm</span></span>
<span data-ttu-id="def22-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def22-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def22-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def22-137">-WhatIf</span></span>
<span data-ttu-id="def22-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="def22-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def22-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="def22-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def22-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def22-140">CommonParameters</span></span>
<span data-ttu-id="def22-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def22-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def22-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def22-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def22-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="def22-143">INPUTS</span></span>

## <span data-ttu-id="def22-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="def22-144">OUTPUTS</span></span>

### <span data-ttu-id="def22-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="def22-145">VmExtensionObject</span></span>

## <span data-ttu-id="def22-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="def22-146">NOTES</span></span>

## <span data-ttu-id="def22-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="def22-147">RELATED LINKS</span></span>

