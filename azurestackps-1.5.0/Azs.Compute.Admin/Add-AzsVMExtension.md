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
ms.locfileid: "93425999"
---
# <span data-ttu-id="54c92-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="54c92-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="54c92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54c92-102">SYNOPSIS</span></span>
<span data-ttu-id="54c92-103">Crie uma nova imagem de extensão de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54c92-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="54c92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54c92-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54c92-105">DESCRIPTION</span></span>
<span data-ttu-id="54c92-106">Criar uma imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54c92-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="54c92-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54c92-107">EXAMPLES</span></span>

### <span data-ttu-id="54c92-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54c92-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="54c92-109">Adicionar uma nova extensão de imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="54c92-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="54c92-110">OS</span><span class="sxs-lookup"><span data-stu-id="54c92-110">PARAMETERS</span></span>

### <span data-ttu-id="54c92-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54c92-111">-AsJob</span></span>
<span data-ttu-id="54c92-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="54c92-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="54c92-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="54c92-113">-ComputeRole</span></span>
<span data-ttu-id="54c92-114">O tipo de função, IaaS ou PaaS, a extensão é compatível.</span><span class="sxs-lookup"><span data-stu-id="54c92-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="54c92-115">-Force</span><span class="sxs-lookup"><span data-stu-id="54c92-115">-Force</span></span>
<span data-ttu-id="54c92-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="54c92-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="54c92-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="54c92-117">-IsSystemExtension</span></span>
<span data-ttu-id="54c92-118">Indica se a extensão é para o sistema.</span><span class="sxs-lookup"><span data-stu-id="54c92-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="54c92-119">-Local</span><span class="sxs-lookup"><span data-stu-id="54c92-119">-Location</span></span>
<span data-ttu-id="54c92-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="54c92-120">Location of the resource.</span></span>

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

### <span data-ttu-id="54c92-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="54c92-121">-Publisher</span></span>
<span data-ttu-id="54c92-122">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="54c92-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="54c92-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="54c92-123">-SourceBlob</span></span>
<span data-ttu-id="54c92-124">URI para pacote de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54c92-124">URI to virtual machine extension package.</span></span>

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

### <span data-ttu-id="54c92-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="54c92-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="54c92-126">Verdadeiro se der suporte a várias extensões.</span><span class="sxs-lookup"><span data-stu-id="54c92-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="54c92-127">-Digite</span><span class="sxs-lookup"><span data-stu-id="54c92-127">-Type</span></span>
<span data-ttu-id="54c92-128">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="54c92-128">Type of extension.</span></span>

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

### <span data-ttu-id="54c92-129">-Versão</span><span class="sxs-lookup"><span data-stu-id="54c92-129">-Version</span></span>
<span data-ttu-id="54c92-130">A versão da extensão de imagem do computador vritual.</span><span class="sxs-lookup"><span data-stu-id="54c92-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="54c92-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="54c92-131">-VmOsType</span></span>
<span data-ttu-id="54c92-132">Destino do tipo de sistema operacional da máquina virtual necessária para implantar o manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="54c92-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="54c92-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="54c92-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="54c92-134">Valor que indica se a extensão está habilitada para suporte ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54c92-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="54c92-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54c92-135">-Confirm</span></span>
<span data-ttu-id="54c92-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c92-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c92-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c92-137">-WhatIf</span></span>
<span data-ttu-id="54c92-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54c92-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c92-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54c92-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c92-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c92-140">CommonParameters</span></span>
<span data-ttu-id="54c92-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c92-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c92-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c92-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c92-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54c92-143">INPUTS</span></span>

## <span data-ttu-id="54c92-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54c92-144">OUTPUTS</span></span>

### <span data-ttu-id="54c92-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="54c92-145">VmExtensionObject</span></span>

## <span data-ttu-id="54c92-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54c92-146">NOTES</span></span>

## <span data-ttu-id="54c92-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54c92-147">RELATED LINKS</span></span>
