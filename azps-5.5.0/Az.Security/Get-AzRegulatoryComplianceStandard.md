---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111368"
---
# <span data-ttu-id="fe4ee-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="fe4ee-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="fe4ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4ee-103">Obtém padrões de conformidade regulamentar</span><span class="sxs-lookup"><span data-stu-id="fe4ee-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="fe4ee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe4ee-104">SYNTAX</span></span>

### <span data-ttu-id="fe4ee-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe4ee-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe4ee-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fe4ee-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe4ee-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="fe4ee-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe4ee-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe4ee-108">DESCRIPTION</span></span>
<span data-ttu-id="fe4ee-109">Receba detalhes de conformidade regulamentar spcifico ou liste todos os padrões regulatórios de conformidade sob assinatura específica.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="fe4ee-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe4ee-110">EXAMPLES</span></span>

### <span data-ttu-id="fe4ee-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe4ee-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="fe4ee-112">Obter todos os padrões regulatórios de conformidade sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="fe4ee-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fe4ee-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="fe4ee-114">Obter detalhes de padrões de conformidade regulamentar específicos de acordo com o nome padrão.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="fe4ee-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fe4ee-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="fe4ee-116">Obter detalhes de padrões de conformidade regulamentar específicos de acordo com a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="fe4ee-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe4ee-117">PARAMETERS</span></span>

### <span data-ttu-id="fe4ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4ee-118">-DefaultProfile</span></span>
<span data-ttu-id="fe4ee-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe4ee-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe4ee-120">-Name</span></span>
<span data-ttu-id="fe4ee-121">Nome padrão.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-121">Standard name.</span></span>

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

### <span data-ttu-id="fe4ee-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe4ee-122">-ResourceId</span></span>
<span data-ttu-id="fe4ee-123">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="fe4ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4ee-124">CommonParameters</span></span>
<span data-ttu-id="fe4ee-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4ee-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe4ee-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4ee-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe4ee-127">INPUTS</span></span>

### <span data-ttu-id="fe4ee-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fe4ee-128">System.String</span></span>

## <span data-ttu-id="fe4ee-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe4ee-129">OUTPUTS</span></span>

### <span data-ttu-id="fe4ee-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="fe4ee-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="fe4ee-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fe4ee-131">NOTES</span></span>

## <span data-ttu-id="fe4ee-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe4ee-132">RELATED LINKS</span></span>
