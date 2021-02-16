---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117897"
---
# <span data-ttu-id="a4ef4-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="a4ef4-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="a4ef4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ef4-103">Obter os usos atuais de uma conta dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="a4ef4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4ef4-104">SYNTAX</span></span>

### <span data-ttu-id="a4ef4-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a4ef4-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ef4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ef4-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ef4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ef4-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ef4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="a4ef4-109">O cmdlet **Get-AzCognitiveServicesAccountUsage obtém** os usos atuais de uma conta do Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="a4ef4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4ef4-110">EXAMPLES</span></span>

### <span data-ttu-id="a4ef4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4ef4-111">Example 1</span></span>
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

### <span data-ttu-id="a4ef4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a4ef4-112">Example 2</span></span>
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

### <span data-ttu-id="a4ef4-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a4ef4-113">Example 3</span></span>
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

## <span data-ttu-id="a4ef4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4ef4-114">PARAMETERS</span></span>

### <span data-ttu-id="a4ef4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ef4-115">-DefaultProfile</span></span>
<span data-ttu-id="a4ef4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ef4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ef4-117">-InputObject</span></span>
<span data-ttu-id="a4ef4-118">Objeto de Conta do Serviço Cognitiva.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="a4ef4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4ef4-119">-Name</span></span>
<span data-ttu-id="a4ef4-120">Nome da conta do Serviço Cognitiva.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="a4ef4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ef4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4ef4-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4ef4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ef4-123">-ResourceId</span></span>
<span data-ttu-id="a4ef4-124">ID do Recurso de Conta do Serviço Cognitiva.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="a4ef4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ef4-125">CommonParameters</span></span>
<span data-ttu-id="a4ef4-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ef4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ef4-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4ef4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ef4-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="a4ef4-128">INPUTS</span></span>

### <span data-ttu-id="a4ef4-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4ef4-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="a4ef4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a4ef4-130">System.String</span></span>

## <span data-ttu-id="a4ef4-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="a4ef4-131">OUTPUTS</span></span>

### <span data-ttu-id="a4ef4-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="a4ef4-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="a4ef4-133">Notas</span><span class="sxs-lookup"><span data-stu-id="a4ef4-133">NOTES</span></span>

## <span data-ttu-id="a4ef4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4ef4-134">RELATED LINKS</span></span>
