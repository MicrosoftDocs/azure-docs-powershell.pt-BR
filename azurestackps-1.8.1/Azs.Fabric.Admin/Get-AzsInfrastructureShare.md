---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774972"
---
# <span data-ttu-id="b48e1-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="b48e1-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="b48e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b48e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b48e1-103">Retorna uma lista de todos os compartilhamentos de arquivos de malha em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="b48e1-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="b48e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b48e1-104">SYNTAX</span></span>

### <span data-ttu-id="b48e1-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b48e1-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b48e1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b48e1-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b48e1-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b48e1-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b48e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b48e1-108">DESCRIPTION</span></span>
<span data-ttu-id="b48e1-109">Retorna uma lista de todos os compartilhamentos de arquivos de malha em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="b48e1-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="b48e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b48e1-110">EXAMPLES</span></span>

### <span data-ttu-id="b48e1-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="b48e1-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="b48e1-112">Retorna uma lista de todos os compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b48e1-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="b48e1-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="b48e1-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="b48e1-114">Retorna um compartilhamento de arquivos com base no nome.</span><span class="sxs-lookup"><span data-stu-id="b48e1-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="b48e1-115">OS</span><span class="sxs-lookup"><span data-stu-id="b48e1-115">PARAMETERS</span></span>

### <span data-ttu-id="b48e1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b48e1-116">-Name</span></span>
<span data-ttu-id="b48e1-117">Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="b48e1-117">Fabric file share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48e1-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b48e1-118">-Location</span></span>
<span data-ttu-id="b48e1-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b48e1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b48e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="b48e1-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="b48e1-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b48e1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b48e1-122">-ResourceId</span></span>
<span data-ttu-id="b48e1-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b48e1-123">The resource id.</span></span>

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

### <span data-ttu-id="b48e1-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b48e1-124">-Filter</span></span>
<span data-ttu-id="b48e1-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b48e1-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b48e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48e1-126">CommonParameters</span></span>
<span data-ttu-id="b48e1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b48e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48e1-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b48e1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48e1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b48e1-129">INPUTS</span></span>

## <span data-ttu-id="b48e1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b48e1-130">OUTPUTS</span></span>

### <span data-ttu-id="b48e1-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="b48e1-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="b48e1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b48e1-132">NOTES</span></span>

## <span data-ttu-id="b48e1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b48e1-133">RELATED LINKS</span></span>
