---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772761"
---
# <span data-ttu-id="a6088-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="a6088-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="a6088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6088-102">SYNOPSIS</span></span>
<span data-ttu-id="a6088-103">Contém o nome do plano desejado para vincular ou desvinculado de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="a6088-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="a6088-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6088-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="a6088-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6088-105">DESCRIPTION</span></span>
<span data-ttu-id="a6088-106">Contém o nome do plano desejado para vincular ou desvinculado de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="a6088-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="a6088-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6088-107">EXAMPLES</span></span>

### <span data-ttu-id="a6088-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6088-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="a6088-109">Crie um novo objeto de definição de plano para o plano especificado com o limite de aquisição de 500.</span><span class="sxs-lookup"><span data-stu-id="a6088-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="a6088-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6088-110">PARAMETERS</span></span>

### <span data-ttu-id="a6088-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="a6088-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="a6088-112">Número máximo de instâncias que podem ser adquiridas por uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6088-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="a6088-113">Se não for especificado, o valor presumido será 1.</span><span class="sxs-lookup"><span data-stu-id="a6088-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6088-114">-PlanID</span><span class="sxs-lookup"><span data-stu-id="a6088-114">-PlanId</span></span>
<span data-ttu-id="a6088-115">Identificador do plano.</span><span class="sxs-lookup"><span data-stu-id="a6088-115">Plan identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6088-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6088-116">CommonParameters</span></span>
<span data-ttu-id="a6088-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6088-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6088-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6088-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6088-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6088-119">INPUTS</span></span>

## <span data-ttu-id="a6088-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6088-120">OUTPUTS</span></span>

## <span data-ttu-id="a6088-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6088-121">NOTES</span></span>

## <span data-ttu-id="a6088-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6088-122">RELATED LINKS</span></span>

