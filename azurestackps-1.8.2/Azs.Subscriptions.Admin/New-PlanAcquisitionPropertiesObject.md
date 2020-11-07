---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946701"
---
# <span data-ttu-id="d0989-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="d0989-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="d0989-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0989-102">SYNOPSIS</span></span>
<span data-ttu-id="d0989-103">Representa a aquisição de um plano de complemento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d0989-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="d0989-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0989-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0989-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0989-105">DESCRIPTION</span></span>
<span data-ttu-id="d0989-106">Representa a aquisição de um plano de complemento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d0989-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="d0989-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0989-107">EXAMPLES</span></span>

### <span data-ttu-id="d0989-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0989-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d0989-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="d0989-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d0989-110">OS</span><span class="sxs-lookup"><span data-stu-id="d0989-110">PARAMETERS</span></span>

### <span data-ttu-id="d0989-111">-Acquisitionid</span><span class="sxs-lookup"><span data-stu-id="d0989-111">-AcquisitionId</span></span>
<span data-ttu-id="d0989-112">Identificador de aquisição.</span><span class="sxs-lookup"><span data-stu-id="d0989-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0989-113">-Acquisitiontime</span><span class="sxs-lookup"><span data-stu-id="d0989-113">-AcquisitionTime</span></span>
<span data-ttu-id="d0989-114">Tempo de aquisição.</span><span class="sxs-lookup"><span data-stu-id="d0989-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0989-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="d0989-115">-ExternalReferenceId</span></span>
<span data-ttu-id="d0989-116">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="d0989-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0989-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d0989-117">-Id</span></span>
<span data-ttu-id="d0989-118">Identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="d0989-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0989-119">-PlanID</span><span class="sxs-lookup"><span data-stu-id="d0989-119">-PlanId</span></span>
<span data-ttu-id="d0989-120">Identificador do plano no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="d0989-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0989-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="d0989-121">-ProvisioningState</span></span>
<span data-ttu-id="d0989-122">Estado do provisionamento.</span><span class="sxs-lookup"><span data-stu-id="d0989-122">State of the provisioning.</span></span>

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

### <span data-ttu-id="d0989-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0989-123">CommonParameters</span></span>
<span data-ttu-id="d0989-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0989-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0989-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0989-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0989-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0989-126">INPUTS</span></span>

## <span data-ttu-id="d0989-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0989-127">OUTPUTS</span></span>

## <span data-ttu-id="d0989-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0989-128">NOTES</span></span>

## <span data-ttu-id="d0989-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0989-129">RELATED LINKS</span></span>

