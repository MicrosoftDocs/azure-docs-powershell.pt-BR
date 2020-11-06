---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: 1cdfaa6b57a0bcf6d50e0e3a77f80c1a5c069069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427270"
---
# <span data-ttu-id="dca8c-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="dca8c-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="dca8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dca8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dca8c-103">Obter usos atuais para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="dca8c-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dca8c-104">SYNTAX</span></span>

### <span data-ttu-id="dca8c-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dca8c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dca8c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca8c-106">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dca8c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca8c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dca8c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dca8c-108">DESCRIPTION</span></span>
<span data-ttu-id="dca8c-109">O cmdlet **Get-AzureRmCognitiveServicesAccountUsage** Obtém os usos atuais para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="dca8c-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="dca8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dca8c-110">EXAMPLES</span></span>

### <span data-ttu-id="dca8c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dca8c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="dca8c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dca8c-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="dca8c-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dca8c-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="dca8c-114">OS</span><span class="sxs-lookup"><span data-stu-id="dca8c-114">PARAMETERS</span></span>

### <span data-ttu-id="dca8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca8c-115">-DefaultProfile</span></span>
<span data-ttu-id="dca8c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dca8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca8c-117">-InputObject</span></span>
<span data-ttu-id="dca8c-118">Objeto da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="dca8c-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="dca8c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="dca8c-119">-Name</span></span>
<span data-ttu-id="dca8c-120">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="dca8c-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="dca8c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca8c-121">-ResourceGroupName</span></span>
<span data-ttu-id="dca8c-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dca8c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="dca8c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dca8c-123">-ResourceId</span></span>
<span data-ttu-id="dca8c-124">ID de recurso da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="dca8c-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="dca8c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca8c-125">CommonParameters</span></span>
<span data-ttu-id="dca8c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca8c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca8c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca8c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca8c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dca8c-128">INPUTS</span></span>

### <span data-ttu-id="dca8c-129">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dca8c-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>
<span data-ttu-id="dca8c-130">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dca8c-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dca8c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dca8c-131">System.String</span></span>

## <span data-ttu-id="dca8c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dca8c-132">OUTPUTS</span></span>

### <span data-ttu-id="dca8c-133">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="dca8c-133">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="dca8c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dca8c-134">NOTES</span></span>

## <span data-ttu-id="dca8c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dca8c-135">RELATED LINKS</span></span>