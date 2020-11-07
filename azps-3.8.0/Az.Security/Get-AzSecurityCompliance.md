---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityCompliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
ms.openlocfilehash: 201af68ba8d888c9c62168f1b3791a2897498027
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941599"
---
# <span data-ttu-id="c90b6-101">Get-AzSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="c90b6-101">Get-AzSecurityCompliance</span></span>

## <span data-ttu-id="c90b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c90b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c90b6-103">Obter a conformidade de segurança de uma assinatura ao longo do tempo</span><span class="sxs-lookup"><span data-stu-id="c90b6-103">Get the security compliance of a subscription over time</span></span>

## <span data-ttu-id="c90b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c90b6-104">SYNTAX</span></span>

### <span data-ttu-id="c90b6-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="c90b6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c90b6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c90b6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c90b6-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="c90b6-107">ResourceId</span></span>
```
Get-AzSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c90b6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c90b6-108">DESCRIPTION</span></span>
<span data-ttu-id="c90b6-109">Obtém a conformidade de segurança de uma assinatura com base na taxa atual de recursos saudáveis e não seguros nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="c90b6-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="c90b6-110">A conformidade de segurança é calculada todos os dias e o histórico é salvo.</span><span class="sxs-lookup"><span data-stu-id="c90b6-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="c90b6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c90b6-111">EXAMPLES</span></span>

### <span data-ttu-id="c90b6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c90b6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="c90b6-113">Obtém a conformidade de segurança de uma assinatura durante os últimos 14 dias</span><span class="sxs-lookup"><span data-stu-id="c90b6-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="c90b6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c90b6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="c90b6-115">Obtém a conformidade de segurança de uma assinatura em uma data específica</span><span class="sxs-lookup"><span data-stu-id="c90b6-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="c90b6-116">OS</span><span class="sxs-lookup"><span data-stu-id="c90b6-116">PARAMETERS</span></span>

### <span data-ttu-id="c90b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90b6-117">-DefaultProfile</span></span>
<span data-ttu-id="c90b6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c90b6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c90b6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c90b6-119">-Name</span></span>
<span data-ttu-id="c90b6-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c90b6-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c90b6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c90b6-121">-ResourceId</span></span>
<span data-ttu-id="c90b6-122">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c90b6-122">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90b6-123">CommonParameters</span></span>
<span data-ttu-id="c90b6-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c90b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90b6-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c90b6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90b6-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c90b6-126">INPUTS</span></span>

### <span data-ttu-id="c90b6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c90b6-127">System.String</span></span>

## <span data-ttu-id="c90b6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c90b6-128">OUTPUTS</span></span>

### <span data-ttu-id="c90b6-129">Microsoft. Azure. Commands. Security. Models. Compliances. PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="c90b6-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="c90b6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c90b6-130">NOTES</span></span>

## <span data-ttu-id="c90b6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c90b6-131">RELATED LINKS</span></span>
