---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 3b12fdd4b82446f67eaaaec7a46bbc7f49307e94
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771257"
---
# <span data-ttu-id="68de1-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="68de1-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="68de1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68de1-102">SYNOPSIS</span></span>
<span data-ttu-id="68de1-103">Obter usos atuais para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="68de1-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="68de1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68de1-104">SYNTAX</span></span>

### <span data-ttu-id="68de1-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="68de1-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68de1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68de1-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68de1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68de1-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68de1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68de1-108">DESCRIPTION</span></span>
<span data-ttu-id="68de1-109">O cmdlet **Get-AzCognitiveServicesAccountUsage** Obtém os usos atuais para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="68de1-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="68de1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68de1-110">EXAMPLES</span></span>

### <span data-ttu-id="68de1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68de1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="68de1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="68de1-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="68de1-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="68de1-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="68de1-114">OS</span><span class="sxs-lookup"><span data-stu-id="68de1-114">PARAMETERS</span></span>

### <span data-ttu-id="68de1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68de1-115">-DefaultProfile</span></span>
<span data-ttu-id="68de1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68de1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68de1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68de1-117">-InputObject</span></span>
<span data-ttu-id="68de1-118">Objeto da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="68de1-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68de1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="68de1-119">-Name</span></span>
<span data-ttu-id="68de1-120">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="68de1-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68de1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68de1-121">-ResourceGroupName</span></span>
<span data-ttu-id="68de1-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68de1-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68de1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68de1-123">-ResourceId</span></span>
<span data-ttu-id="68de1-124">ID de recurso da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="68de1-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68de1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68de1-125">CommonParameters</span></span>
<span data-ttu-id="68de1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68de1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68de1-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68de1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68de1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68de1-128">INPUTS</span></span>

### <span data-ttu-id="68de1-129">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="68de1-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="68de1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="68de1-130">System.String</span></span>

## <span data-ttu-id="68de1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68de1-131">OUTPUTS</span></span>

### <span data-ttu-id="68de1-132">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="68de1-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="68de1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68de1-133">NOTES</span></span>

## <span data-ttu-id="68de1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68de1-134">RELATED LINKS</span></span>
