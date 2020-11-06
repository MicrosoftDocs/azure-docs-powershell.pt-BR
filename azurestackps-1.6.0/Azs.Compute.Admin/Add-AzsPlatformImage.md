---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426185"
---
# <span data-ttu-id="7c9dd-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="7c9dd-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="7c9dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9dd-103">Adicionar uma imagem de plataforma da máquina virtual a partir de uma determinada configuração de imagem.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="7c9dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c9dd-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c9dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7c9dd-106">Adicionar uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-106">Add a platform image.</span></span>

## <span data-ttu-id="7c9dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c9dd-107">EXAMPLES</span></span>

### <span data-ttu-id="7c9dd-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c9dd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="7c9dd-109">Adicionar uma nova imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-109">Add a new platform image.</span></span>

## <span data-ttu-id="7c9dd-110">OS</span><span class="sxs-lookup"><span data-stu-id="7c9dd-110">PARAMETERS</span></span>

### <span data-ttu-id="7c9dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c9dd-111">-AsJob</span></span>
<span data-ttu-id="7c9dd-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7c9dd-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="7c9dd-113">-BillingPartNumber</span></span>
<span data-ttu-id="7c9dd-114">O número da peça é usado para cobrar pelos custos do software.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-114">The part number is used to bill for software costs.</span></span>

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

### <span data-ttu-id="7c9dd-115">-Datadisks</span><span class="sxs-lookup"><span data-stu-id="7c9dd-115">-DataDisks</span></span>
<span data-ttu-id="7c9dd-116">Discos de dados usados pela imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-116">Data disks used by the platform image.</span></span>

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

### <span data-ttu-id="7c9dd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7c9dd-117">-Force</span></span>
<span data-ttu-id="7c9dd-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7c9dd-119">-Local</span><span class="sxs-lookup"><span data-stu-id="7c9dd-119">-Location</span></span>
<span data-ttu-id="7c9dd-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-120">Location of the resource.</span></span>

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

### <span data-ttu-id="7c9dd-121">-Oferta</span><span class="sxs-lookup"><span data-stu-id="7c9dd-121">-Offer</span></span>
<span data-ttu-id="7c9dd-122">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-122">Name of the offer.</span></span>

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

### <span data-ttu-id="7c9dd-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="7c9dd-123">-OsType</span></span>
<span data-ttu-id="7c9dd-124">Tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-124">Operating system type.</span></span>

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

### <span data-ttu-id="7c9dd-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="7c9dd-125">-OsUri</span></span>
<span data-ttu-id="7c9dd-126">Local do disco.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-126">Location of the disk.</span></span>

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

### <span data-ttu-id="7c9dd-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7c9dd-127">-Publisher</span></span>
<span data-ttu-id="7c9dd-128">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-128">Name of the publisher.</span></span>

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

### <span data-ttu-id="7c9dd-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="7c9dd-129">-Sku</span></span>
<span data-ttu-id="7c9dd-130">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-130">Name of the SKU.</span></span>

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

### <span data-ttu-id="7c9dd-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="7c9dd-131">-Version</span></span>
<span data-ttu-id="7c9dd-132">A versão da imagem da plataforma da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-132">The version of the virtual machine platform image.</span></span>

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

### <span data-ttu-id="7c9dd-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c9dd-133">-Confirm</span></span>
<span data-ttu-id="7c9dd-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c9dd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9dd-135">-WhatIf</span></span>
<span data-ttu-id="7c9dd-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c9dd-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c9dd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9dd-138">CommonParameters</span></span>
<span data-ttu-id="7c9dd-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c9dd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9dd-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c9dd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9dd-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c9dd-141">INPUTS</span></span>

## <span data-ttu-id="7c9dd-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c9dd-142">OUTPUTS</span></span>

### <span data-ttu-id="7c9dd-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="7c9dd-143">PlatformImageObject</span></span>

## <span data-ttu-id="7c9dd-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c9dd-144">NOTES</span></span>

## <span data-ttu-id="7c9dd-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c9dd-145">RELATED LINKS</span></span>

