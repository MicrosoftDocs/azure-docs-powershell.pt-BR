---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774189"
---
# <span data-ttu-id="c596e-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c596e-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="c596e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c596e-102">SYNOPSIS</span></span>
<span data-ttu-id="c596e-103">Retorna o avaialbility do tipo de recurso e do nome de recurso de assinaturas especificado</span><span class="sxs-lookup"><span data-stu-id="c596e-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="c596e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c596e-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="c596e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c596e-105">DESCRIPTION</span></span>
<span data-ttu-id="c596e-106">Retorna o avaialbility do tipo de recurso e do nome de recurso de assinaturas especificado</span><span class="sxs-lookup"><span data-stu-id="c596e-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="c596e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c596e-107">EXAMPLES</span></span>

### <span data-ttu-id="c596e-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c596e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="c596e-109">Retorna o avaialbility do tipo de recurso e do nome de recurso de assinaturas especificado</span><span class="sxs-lookup"><span data-stu-id="c596e-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="c596e-110">OS</span><span class="sxs-lookup"><span data-stu-id="c596e-110">PARAMETERS</span></span>

### <span data-ttu-id="c596e-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="c596e-111">-Name</span></span>
<span data-ttu-id="c596e-112">O nome do recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c596e-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596e-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c596e-113">-ResourceType</span></span>
<span data-ttu-id="c596e-114">O tipo de recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c596e-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c596e-115">CommonParameters</span></span>
<span data-ttu-id="c596e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c596e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c596e-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c596e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c596e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c596e-118">INPUTS</span></span>

## <span data-ttu-id="c596e-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c596e-119">OUTPUTS</span></span>

### <span data-ttu-id="c596e-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c596e-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="c596e-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c596e-121">NOTES</span></span>

## <span data-ttu-id="c596e-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c596e-122">RELATED LINKS</span></span>

