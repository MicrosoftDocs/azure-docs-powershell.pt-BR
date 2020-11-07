---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774752"
---
# <span data-ttu-id="d3437-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="d3437-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="d3437-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3437-102">SYNOPSIS</span></span>
<span data-ttu-id="d3437-103">Representa a aquisição de um plano de complemento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3437-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="d3437-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3437-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3437-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3437-105">DESCRIPTION</span></span>
<span data-ttu-id="d3437-106">Representa a aquisição de um plano de complemento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3437-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="d3437-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3437-107">EXAMPLES</span></span>

### <span data-ttu-id="d3437-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3437-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d3437-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="d3437-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d3437-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3437-110">PARAMETERS</span></span>

### <span data-ttu-id="d3437-111">-Acquisitionid</span><span class="sxs-lookup"><span data-stu-id="d3437-111">-AcquisitionId</span></span>
<span data-ttu-id="d3437-112">Identificador de aquisição.</span><span class="sxs-lookup"><span data-stu-id="d3437-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="d3437-113">-Acquisitiontime</span><span class="sxs-lookup"><span data-stu-id="d3437-113">-AcquisitionTime</span></span>
<span data-ttu-id="d3437-114">Tempo de aquisição.</span><span class="sxs-lookup"><span data-stu-id="d3437-114">Acquisition time.</span></span>

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

### <span data-ttu-id="d3437-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="d3437-115">-ExternalReferenceId</span></span>
<span data-ttu-id="d3437-116">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="d3437-116">External reference identifier.</span></span>

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

### <span data-ttu-id="d3437-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d3437-117">-Id</span></span>
<span data-ttu-id="d3437-118">Identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="d3437-118">Identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="d3437-119">-PlanID</span><span class="sxs-lookup"><span data-stu-id="d3437-119">-PlanId</span></span>
<span data-ttu-id="d3437-120">Identificador do plano no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="d3437-120">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="d3437-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="d3437-121">-ProvisioningState</span></span>
<span data-ttu-id="d3437-122">Estado do provisionamento.</span><span class="sxs-lookup"><span data-stu-id="d3437-122">State of the provisioning.</span></span>

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

### <span data-ttu-id="d3437-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3437-123">CommonParameters</span></span>
<span data-ttu-id="d3437-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3437-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3437-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3437-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3437-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3437-126">INPUTS</span></span>

## <span data-ttu-id="d3437-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3437-127">OUTPUTS</span></span>

## <span data-ttu-id="d3437-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3437-128">NOTES</span></span>

## <span data-ttu-id="d3437-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3437-129">RELATED LINKS</span></span>

