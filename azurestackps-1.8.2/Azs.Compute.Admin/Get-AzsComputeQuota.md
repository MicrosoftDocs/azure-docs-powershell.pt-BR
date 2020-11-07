---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946696"
---
# <span data-ttu-id="75569-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="75569-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="75569-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75569-102">SYNOPSIS</span></span>
<span data-ttu-id="75569-103">Retorna as cotas que especificam os limites de cota para objetos de computação.</span><span class="sxs-lookup"><span data-stu-id="75569-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="75569-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75569-104">SYNTAX</span></span>

### <span data-ttu-id="75569-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="75569-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="75569-106">Obter</span><span class="sxs-lookup"><span data-stu-id="75569-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="75569-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="75569-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="75569-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75569-108">DESCRIPTION</span></span>
<span data-ttu-id="75569-109">Obter uma lista de cotas existentes.</span><span class="sxs-lookup"><span data-stu-id="75569-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="75569-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75569-110">EXAMPLES</span></span>

### <span data-ttu-id="75569-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75569-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="75569-112">Obter todas as cotas de computação no local especificado.</span><span class="sxs-lookup"><span data-stu-id="75569-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="75569-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="75569-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="75569-114">Obtenha uma cota de computação específica.</span><span class="sxs-lookup"><span data-stu-id="75569-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="75569-115">OS</span><span class="sxs-lookup"><span data-stu-id="75569-115">PARAMETERS</span></span>

### <span data-ttu-id="75569-116">-Local</span><span class="sxs-lookup"><span data-stu-id="75569-116">-Location</span></span>
<span data-ttu-id="75569-117">{{Descrição do local de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="75569-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="75569-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="75569-118">-Name</span></span>
<span data-ttu-id="75569-119">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="75569-119">Name of the quota.</span></span>

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

### <span data-ttu-id="75569-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75569-120">-ResourceId</span></span>
<span data-ttu-id="75569-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="75569-121">The resource id.</span></span>

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

### <span data-ttu-id="75569-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75569-122">CommonParameters</span></span>
<span data-ttu-id="75569-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75569-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75569-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75569-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75569-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75569-125">INPUTS</span></span>

## <span data-ttu-id="75569-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75569-126">OUTPUTS</span></span>

### <span data-ttu-id="75569-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="75569-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="75569-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75569-128">NOTES</span></span>

## <span data-ttu-id="75569-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75569-129">RELATED LINKS</span></span>

