---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601804"
---
# <span data-ttu-id="6256c-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="6256c-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="6256c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6256c-102">SYNOPSIS</span></span>
<span data-ttu-id="6256c-103">Retorna uma lista de todos os compartilhamentos de arquivos de malha em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="6256c-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="6256c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6256c-104">SYNTAX</span></span>

### <span data-ttu-id="6256c-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="6256c-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6256c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6256c-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6256c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="6256c-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6256c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6256c-108">DESCRIPTION</span></span>
<span data-ttu-id="6256c-109">Retorna uma lista de todos os compartilhamentos de arquivos de malha em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="6256c-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="6256c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6256c-110">EXAMPLES</span></span>

### <span data-ttu-id="6256c-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6256c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="6256c-112">Retorna uma lista de todos os compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6256c-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="6256c-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6256c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="6256c-114">Retorna um compartilhamento de arquivos com base no nome.</span><span class="sxs-lookup"><span data-stu-id="6256c-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="6256c-115">OS</span><span class="sxs-lookup"><span data-stu-id="6256c-115">PARAMETERS</span></span>

### <span data-ttu-id="6256c-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="6256c-116">-Filter</span></span>
<span data-ttu-id="6256c-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="6256c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6256c-118">-Local</span><span class="sxs-lookup"><span data-stu-id="6256c-118">-Location</span></span>
<span data-ttu-id="6256c-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6256c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6256c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6256c-120">-Name</span></span>
<span data-ttu-id="6256c-121">Nome do compartilhamento de arquivos do fabric.</span><span class="sxs-lookup"><span data-stu-id="6256c-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="6256c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6256c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6256c-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="6256c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6256c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6256c-124">-ResourceId</span></span>
<span data-ttu-id="6256c-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6256c-125">The resource id.</span></span>

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

### <span data-ttu-id="6256c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6256c-126">CommonParameters</span></span>
<span data-ttu-id="6256c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6256c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6256c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6256c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6256c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6256c-129">INPUTS</span></span>

## <span data-ttu-id="6256c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6256c-130">OUTPUTS</span></span>

### <span data-ttu-id="6256c-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="6256c-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="6256c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6256c-132">NOTES</span></span>

## <span data-ttu-id="6256c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6256c-133">RELATED LINKS</span></span>

