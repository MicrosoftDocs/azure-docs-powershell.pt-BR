---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773925"
---
# <span data-ttu-id="6400f-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="6400f-101">Get-AzsDisk</span></span>

## <span data-ttu-id="6400f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6400f-102">SYNOPSIS</span></span>
<span data-ttu-id="6400f-103">Retorna a lista de discos gerenciados que podem ser migrados no compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="6400f-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="6400f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6400f-104">SYNTAX</span></span>

### <span data-ttu-id="6400f-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="6400f-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="6400f-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="6400f-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="6400f-107">Obter</span><span class="sxs-lookup"><span data-stu-id="6400f-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="6400f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6400f-108">DESCRIPTION</span></span>
<span data-ttu-id="6400f-109">Retorna uma lista de discos.</span><span class="sxs-lookup"><span data-stu-id="6400f-109">Returns a list of disks.</span></span>

## <span data-ttu-id="6400f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6400f-110">EXAMPLES</span></span>

### <span data-ttu-id="6400f-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6400f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="6400f-112">Retorna uma lista de discos gerenciados no local local.</span><span class="sxs-lookup"><span data-stu-id="6400f-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="6400f-113">Por padrão, ele vai usar os primeiros 100 discos</span><span class="sxs-lookup"><span data-stu-id="6400f-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="6400f-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6400f-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="6400f-115">Obter um disco gerenciado específico.</span><span class="sxs-lookup"><span data-stu-id="6400f-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="6400f-116">OS</span><span class="sxs-lookup"><span data-stu-id="6400f-116">PARAMETERS</span></span>

### <span data-ttu-id="6400f-117">-Contagem</span><span class="sxs-lookup"><span data-stu-id="6400f-117">-Count</span></span>
<span data-ttu-id="6400f-118">O número máximo de discos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="6400f-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6400f-119">-Local</span><span class="sxs-lookup"><span data-stu-id="6400f-119">-Location</span></span>
<span data-ttu-id="6400f-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6400f-120">Location of the resource.</span></span>

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

### <span data-ttu-id="6400f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6400f-121">-Name</span></span>
<span data-ttu-id="6400f-122">A GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="6400f-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6400f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6400f-123">-ResourceId</span></span>
<span data-ttu-id="6400f-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6400f-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6400f-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="6400f-125">-SharePath</span></span>
<span data-ttu-id="6400f-126">O compartilhamento de origem ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="6400f-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="6400f-127">-Início</span><span class="sxs-lookup"><span data-stu-id="6400f-127">-Start</span></span>
<span data-ttu-id="6400f-128">O índice inicial de discos na consulta.</span><span class="sxs-lookup"><span data-stu-id="6400f-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6400f-129">-Status</span><span class="sxs-lookup"><span data-stu-id="6400f-129">-Status</span></span>
<span data-ttu-id="6400f-130">Os parâmetros do estado do disco.</span><span class="sxs-lookup"><span data-stu-id="6400f-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="6400f-131">-Usersubscriptionid</span><span class="sxs-lookup"><span data-stu-id="6400f-131">-UserSubscriptionId</span></span>
<span data-ttu-id="6400f-132">ID da assinatura de locatário à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="6400f-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="6400f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6400f-133">CommonParameters</span></span>
<span data-ttu-id="6400f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6400f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6400f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6400f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6400f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6400f-136">INPUTS</span></span>

## <span data-ttu-id="6400f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6400f-137">OUTPUTS</span></span>

### <span data-ttu-id="6400f-138">Microsoft. AzureStack. Management. COMPUTE. admin. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="6400f-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="6400f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6400f-139">NOTES</span></span>

## <span data-ttu-id="6400f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6400f-140">RELATED LINKS</span></span>

