---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774905"
---
# <span data-ttu-id="12b1a-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="12b1a-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="12b1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="12b1a-103">Representa a aquisição de um plano de complemento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="12b1a-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="12b1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12b1a-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="12b1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="12b1a-106">Representa a aquisição de um plano de complemento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="12b1a-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="12b1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="12b1a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12b1a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="12b1a-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="12b1a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="12b1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="12b1a-110">PARAMETERS</span></span>

### <span data-ttu-id="12b1a-111">-Acquisitionid</span><span class="sxs-lookup"><span data-stu-id="12b1a-111">-AcquisitionId</span></span>
<span data-ttu-id="12b1a-112">Identificador de aquisição.</span><span class="sxs-lookup"><span data-stu-id="12b1a-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="12b1a-113">-Acquisitiontime</span><span class="sxs-lookup"><span data-stu-id="12b1a-113">-AcquisitionTime</span></span>
<span data-ttu-id="12b1a-114">Tempo de aquisição.</span><span class="sxs-lookup"><span data-stu-id="12b1a-114">Acquisition time.</span></span>

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

### <span data-ttu-id="12b1a-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="12b1a-115">-ExternalReferenceId</span></span>
<span data-ttu-id="12b1a-116">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="12b1a-116">External reference identifier.</span></span>

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

### <span data-ttu-id="12b1a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="12b1a-117">-Id</span></span>
<span data-ttu-id="12b1a-118">Identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="12b1a-118">Identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="12b1a-119">-PlanID</span><span class="sxs-lookup"><span data-stu-id="12b1a-119">-PlanId</span></span>
<span data-ttu-id="12b1a-120">Identificador do plano no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="12b1a-120">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="12b1a-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="12b1a-121">-ProvisioningState</span></span>
<span data-ttu-id="12b1a-122">Estado do provisionamento.</span><span class="sxs-lookup"><span data-stu-id="12b1a-122">State of the provisioning.</span></span>

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

### <span data-ttu-id="12b1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b1a-123">CommonParameters</span></span>
<span data-ttu-id="12b1a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b1a-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b1a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b1a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12b1a-126">INPUTS</span></span>

## <span data-ttu-id="12b1a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12b1a-127">OUTPUTS</span></span>

## <span data-ttu-id="12b1a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12b1a-128">NOTES</span></span>

## <span data-ttu-id="12b1a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12b1a-129">RELATED LINKS</span></span>

