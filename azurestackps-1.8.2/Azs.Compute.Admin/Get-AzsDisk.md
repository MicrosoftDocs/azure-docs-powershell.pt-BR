---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946689"
---
# <span data-ttu-id="1e5b9-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="1e5b9-101">Get-AzsDisk</span></span>

## <span data-ttu-id="1e5b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5b9-103">Retorna a lista de discos gerenciados que podem ser migrados no compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1e5b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e5b9-104">SYNTAX</span></span>

### <span data-ttu-id="1e5b9-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e5b9-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="1e5b9-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="1e5b9-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="1e5b9-107">Obter</span><span class="sxs-lookup"><span data-stu-id="1e5b9-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="1e5b9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e5b9-108">DESCRIPTION</span></span>
<span data-ttu-id="1e5b9-109">Retorna uma lista de discos.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-109">Returns a list of disks.</span></span>

## <span data-ttu-id="1e5b9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e5b9-110">EXAMPLES</span></span>

### <span data-ttu-id="1e5b9-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e5b9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="1e5b9-112">Retorna uma lista de discos gerenciados no local local.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="1e5b9-113">Por padrão, ele vai usar os primeiros 100 discos</span><span class="sxs-lookup"><span data-stu-id="1e5b9-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="1e5b9-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e5b9-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="1e5b9-115">Obter um disco gerenciado específico.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="1e5b9-116">OS</span><span class="sxs-lookup"><span data-stu-id="1e5b9-116">PARAMETERS</span></span>

### <span data-ttu-id="1e5b9-117">-Contagem</span><span class="sxs-lookup"><span data-stu-id="1e5b9-117">-Count</span></span>
<span data-ttu-id="1e5b9-118">O número máximo de discos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-118">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="1e5b9-119">-Local</span><span class="sxs-lookup"><span data-stu-id="1e5b9-119">-Location</span></span>
<span data-ttu-id="1e5b9-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-120">Location of the resource.</span></span>

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

### <span data-ttu-id="1e5b9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e5b9-121">-Name</span></span>
<span data-ttu-id="1e5b9-122">A GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-122">The disk guid as identity.</span></span>

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

### <span data-ttu-id="1e5b9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5b9-123">-ResourceId</span></span>
<span data-ttu-id="1e5b9-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-124">The resource id.</span></span>

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

### <span data-ttu-id="1e5b9-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="1e5b9-125">-SharePath</span></span>
<span data-ttu-id="1e5b9-126">O compartilhamento de origem ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="1e5b9-127">-Início</span><span class="sxs-lookup"><span data-stu-id="1e5b9-127">-Start</span></span>
<span data-ttu-id="1e5b9-128">O índice inicial de discos na consulta.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-128">The start index of disks in query.</span></span>

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

### <span data-ttu-id="1e5b9-129">-Status</span><span class="sxs-lookup"><span data-stu-id="1e5b9-129">-Status</span></span>
<span data-ttu-id="1e5b9-130">Os parâmetros do estado do disco.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="1e5b9-131">-Usersubscriptionid</span><span class="sxs-lookup"><span data-stu-id="1e5b9-131">-UserSubscriptionId</span></span>
<span data-ttu-id="1e5b9-132">ID da assinatura de locatário à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="1e5b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5b9-133">CommonParameters</span></span>
<span data-ttu-id="1e5b9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5b9-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5b9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5b9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e5b9-136">INPUTS</span></span>

## <span data-ttu-id="1e5b9-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e5b9-137">OUTPUTS</span></span>

### <span data-ttu-id="1e5b9-138">Microsoft. AzureStack. Management. COMPUTE. admin. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="1e5b9-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="1e5b9-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e5b9-139">NOTES</span></span>

## <span data-ttu-id="1e5b9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e5b9-140">RELATED LINKS</span></span>

