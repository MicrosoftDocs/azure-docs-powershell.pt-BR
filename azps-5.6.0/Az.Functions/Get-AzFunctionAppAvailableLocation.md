---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 987c4e351e024452231b5a5367ea7c2905d57863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887522"
---
# <span data-ttu-id="80d06-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="80d06-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="80d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d06-102">SYNOPSIS</span></span>
<span data-ttu-id="80d06-103">Obtém o local onde um aplicativo de função para o sistema operacional determinado e o tipo de plano está disponível.</span><span class="sxs-lookup"><span data-stu-id="80d06-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="80d06-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80d06-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="80d06-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80d06-105">DESCRIPTION</span></span>
<span data-ttu-id="80d06-106">Obtém o local onde um aplicativo de função para o sistema operacional determinado e o tipo de plano está disponível.</span><span class="sxs-lookup"><span data-stu-id="80d06-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="80d06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80d06-107">EXAMPLES</span></span>

### <span data-ttu-id="80d06-108">Exemplo 1: Obter os locais onde o Premium está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="80d06-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="80d06-109">Se nenhum parâmetro for especificado, PlanType será definido como 'Premium' e OSType será definido como 'Windows'.</span><span class="sxs-lookup"><span data-stu-id="80d06-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="80d06-110">Este comando obtém os locais onde Premium está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="80d06-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="80d06-111">Exemplo 2: Obter os locais onde o Premium está disponível para Linux.</span><span class="sxs-lookup"><span data-stu-id="80d06-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="80d06-112">Este comando obtém os locais onde o Premium está disponível para Linux.</span><span class="sxs-lookup"><span data-stu-id="80d06-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="80d06-113">Exemplo 3: Obter os locais onde o Consumo está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="80d06-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="80d06-114">Este comando obtém os locais onde o Consumo está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="80d06-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="80d06-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80d06-115">PARAMETERS</span></span>

### <span data-ttu-id="80d06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d06-116">-DefaultProfile</span></span>
<span data-ttu-id="80d06-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80d06-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d06-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="80d06-118">-OSType</span></span>
<span data-ttu-id="80d06-119">O tipo de sistema operacional do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="80d06-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d06-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="80d06-120">-PlanType</span></span>
<span data-ttu-id="80d06-121">O tipo de plano.</span><span class="sxs-lookup"><span data-stu-id="80d06-121">The plan type.</span></span>
<span data-ttu-id="80d06-122">Entradas válidas: Consumo ou Premium</span><span class="sxs-lookup"><span data-stu-id="80d06-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d06-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80d06-123">-SubscriptionId</span></span>
<span data-ttu-id="80d06-124">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="80d06-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d06-125">CommonParameters</span></span>
<span data-ttu-id="80d06-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d06-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80d06-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d06-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80d06-128">INPUTS</span></span>

## <span data-ttu-id="80d06-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80d06-129">OUTPUTS</span></span>

### <span data-ttu-id="80d06-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="80d06-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="80d06-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="80d06-131">NOTES</span></span>

<span data-ttu-id="80d06-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="80d06-132">ALIASES</span></span>

## <span data-ttu-id="80d06-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80d06-133">RELATED LINKS</span></span>

