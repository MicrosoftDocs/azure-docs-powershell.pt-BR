---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426813"
---
# <span data-ttu-id="35c4d-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="35c4d-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="35c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="35c4d-103">Obter usos atuais para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="35c4d-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35c4d-104">SYNTAX</span></span>

### <span data-ttu-id="35c4d-105">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35c4d-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35c4d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35c4d-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35c4d-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35c4d-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c4d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35c4d-108">DESCRIPTION</span></span>
<span data-ttu-id="35c4d-109">O cmdlet **Get-AzureRmCognitiveServicesAccountUsage** Obtém os usos atuais para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="35c4d-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="35c4d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35c4d-110">EXAMPLES</span></span>

### <span data-ttu-id="35c4d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35c4d-111">Example 1</span></span>
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

### <span data-ttu-id="35c4d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="35c4d-112">Example 2</span></span>
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

### <span data-ttu-id="35c4d-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="35c4d-113">Example 3</span></span>
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

## <span data-ttu-id="35c4d-114">OS</span><span class="sxs-lookup"><span data-stu-id="35c4d-114">PARAMETERS</span></span>

### <span data-ttu-id="35c4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c4d-115">-DefaultProfile</span></span>
<span data-ttu-id="35c4d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35c4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35c4d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35c4d-117">-InputObject</span></span>
<span data-ttu-id="35c4d-118">Objeto da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="35c4d-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35c4d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="35c4d-119">-Name</span></span>
<span data-ttu-id="35c4d-120">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="35c4d-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35c4d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c4d-121">-ResourceGroupName</span></span>
<span data-ttu-id="35c4d-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35c4d-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35c4d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35c4d-123">-ResourceId</span></span>
<span data-ttu-id="35c4d-124">ID de recurso da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="35c4d-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35c4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c4d-125">CommonParameters</span></span>
<span data-ttu-id="35c4d-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c4d-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c4d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c4d-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35c4d-128">INPUTS</span></span>

### <span data-ttu-id="35c4d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="35c4d-129">System.String</span></span>

## <span data-ttu-id="35c4d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35c4d-130">OUTPUTS</span></span>

### <span data-ttu-id="35c4d-131">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="35c4d-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="35c4d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35c4d-132">NOTES</span></span>

## <span data-ttu-id="35c4d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35c4d-133">RELATED LINKS</span></span>
