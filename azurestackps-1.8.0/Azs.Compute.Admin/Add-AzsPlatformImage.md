---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774550"
---
# <span data-ttu-id="ecea5-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ecea5-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="ecea5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecea5-102">SYNOPSIS</span></span>
<span data-ttu-id="ecea5-103">Adicionar uma imagem de plataforma da máquina virtual a partir de uma determinada configuração de imagem.</span><span class="sxs-lookup"><span data-stu-id="ecea5-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="ecea5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecea5-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecea5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecea5-105">DESCRIPTION</span></span>
<span data-ttu-id="ecea5-106">Adicionar uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="ecea5-106">Add a platform image.</span></span>

## <span data-ttu-id="ecea5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecea5-107">EXAMPLES</span></span>

### <span data-ttu-id="ecea5-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecea5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="ecea5-109">Adicionar uma nova imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="ecea5-109">Add a new platform image.</span></span>

## <span data-ttu-id="ecea5-110">OS</span><span class="sxs-lookup"><span data-stu-id="ecea5-110">PARAMETERS</span></span>

### <span data-ttu-id="ecea5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecea5-111">-AsJob</span></span>
<span data-ttu-id="ecea5-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecea5-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ecea5-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="ecea5-113">-BillingPartNumber</span></span>
<span data-ttu-id="ecea5-114">O número da peça é usado para cobrar pelos custos do software.</span><span class="sxs-lookup"><span data-stu-id="ecea5-114">The part number is used to bill for software costs.</span></span>

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

### <span data-ttu-id="ecea5-115">-Datadisks</span><span class="sxs-lookup"><span data-stu-id="ecea5-115">-DataDisks</span></span>
<span data-ttu-id="ecea5-116">Discos de dados usados pela imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="ecea5-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecea5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ecea5-117">-Force</span></span>
<span data-ttu-id="ecea5-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ecea5-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ecea5-119">-Local</span><span class="sxs-lookup"><span data-stu-id="ecea5-119">-Location</span></span>
<span data-ttu-id="ecea5-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="ecea5-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecea5-121">-Oferta</span><span class="sxs-lookup"><span data-stu-id="ecea5-121">-Offer</span></span>
<span data-ttu-id="ecea5-122">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="ecea5-122">Name of the offer.</span></span>

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

### <span data-ttu-id="ecea5-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="ecea5-123">-OsType</span></span>
<span data-ttu-id="ecea5-124">Tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ecea5-124">Operating system type.</span></span>

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

### <span data-ttu-id="ecea5-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="ecea5-125">-OsUri</span></span>
<span data-ttu-id="ecea5-126">Local do disco.</span><span class="sxs-lookup"><span data-stu-id="ecea5-126">Location of the disk.</span></span>

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

### <span data-ttu-id="ecea5-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ecea5-127">-Publisher</span></span>
<span data-ttu-id="ecea5-128">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="ecea5-128">Name of the publisher.</span></span>

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

### <span data-ttu-id="ecea5-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="ecea5-129">-Sku</span></span>
<span data-ttu-id="ecea5-130">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="ecea5-130">Name of the SKU.</span></span>

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

### <span data-ttu-id="ecea5-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="ecea5-131">-Version</span></span>
<span data-ttu-id="ecea5-132">A versão da imagem da plataforma da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ecea5-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecea5-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecea5-133">-Confirm</span></span>
<span data-ttu-id="ecea5-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecea5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecea5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecea5-135">-WhatIf</span></span>
<span data-ttu-id="ecea5-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecea5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecea5-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecea5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecea5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecea5-138">CommonParameters</span></span>
<span data-ttu-id="ecea5-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecea5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecea5-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecea5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecea5-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecea5-141">INPUTS</span></span>

## <span data-ttu-id="ecea5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecea5-142">OUTPUTS</span></span>

### <span data-ttu-id="ecea5-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="ecea5-143">PlatformImageObject</span></span>

## <span data-ttu-id="ecea5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecea5-144">NOTES</span></span>

## <span data-ttu-id="ecea5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecea5-145">RELATED LINKS</span></span>

