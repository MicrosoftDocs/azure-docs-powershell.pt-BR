---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773921"
---
# <span data-ttu-id="aea65-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="aea65-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="aea65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aea65-102">SYNOPSIS</span></span>
<span data-ttu-id="aea65-103">Retorna as extensões de imagem de máquina virtual disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="aea65-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="aea65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aea65-104">SYNTAX</span></span>

### <span data-ttu-id="aea65-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="aea65-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="aea65-106">Obter</span><span class="sxs-lookup"><span data-stu-id="aea65-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="aea65-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="aea65-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="aea65-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aea65-108">DESCRIPTION</span></span>
<span data-ttu-id="aea65-109">Retorna extensões de imagem de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aea65-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="aea65-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aea65-110">EXAMPLES</span></span>

### <span data-ttu-id="aea65-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aea65-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="aea65-112">Obter todas as extensões de VM em um local.</span><span class="sxs-lookup"><span data-stu-id="aea65-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="aea65-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aea65-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="aea65-114">Obter extensão de VM específica.</span><span class="sxs-lookup"><span data-stu-id="aea65-114">Get specific VM extension.</span></span>

## <span data-ttu-id="aea65-115">OS</span><span class="sxs-lookup"><span data-stu-id="aea65-115">PARAMETERS</span></span>

### <span data-ttu-id="aea65-116">-Local</span><span class="sxs-lookup"><span data-stu-id="aea65-116">-Location</span></span>
<span data-ttu-id="aea65-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="aea65-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea65-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="aea65-118">-Publisher</span></span>
<span data-ttu-id="aea65-119">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="aea65-119">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea65-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aea65-120">-ResourceId</span></span>
<span data-ttu-id="aea65-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="aea65-121">The resource id.</span></span>

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

### <span data-ttu-id="aea65-122">-Digite</span><span class="sxs-lookup"><span data-stu-id="aea65-122">-Type</span></span>
<span data-ttu-id="aea65-123">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="aea65-123">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea65-124">-Versão</span><span class="sxs-lookup"><span data-stu-id="aea65-124">-Version</span></span>
<span data-ttu-id="aea65-125">A versão da extensão de imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aea65-125">The version of the virtual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea65-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea65-126">CommonParameters</span></span>
<span data-ttu-id="aea65-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea65-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea65-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea65-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea65-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aea65-129">INPUTS</span></span>

## <span data-ttu-id="aea65-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aea65-130">OUTPUTS</span></span>

### <span data-ttu-id="aea65-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="aea65-131">VmExtensionObject</span></span>

## <span data-ttu-id="aea65-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aea65-132">NOTES</span></span>

## <span data-ttu-id="aea65-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aea65-133">RELATED LINKS</span></span>

