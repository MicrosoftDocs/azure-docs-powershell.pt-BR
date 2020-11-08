---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113569"
---
# <span data-ttu-id="543d1-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="543d1-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="543d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="543d1-102">SYNOPSIS</span></span>
<span data-ttu-id="543d1-103">Obtém o local onde um aplicativo de função para o sistema operacional e o tipo de plano fornecido está disponível.</span><span class="sxs-lookup"><span data-stu-id="543d1-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="543d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="543d1-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="543d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="543d1-105">DESCRIPTION</span></span>
<span data-ttu-id="543d1-106">Obtém o local onde um aplicativo de função para o sistema operacional e o tipo de plano fornecido está disponível.</span><span class="sxs-lookup"><span data-stu-id="543d1-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="543d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="543d1-107">EXAMPLES</span></span>

### <span data-ttu-id="543d1-108">Exemplo 1: Obtenha os locais onde o Premium está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="543d1-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="543d1-109">Se nenhum parâmetro for especificado, Plantype será definido como ' Premium ' e OSType será definido como ' Windows '.</span><span class="sxs-lookup"><span data-stu-id="543d1-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="543d1-110">Esse comando obtém os locais onde o Premium está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="543d1-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="543d1-111">Exemplo 2: Obtenha os locais onde o Premium está disponível para Linux.</span><span class="sxs-lookup"><span data-stu-id="543d1-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="543d1-112">Este comando obtém os locais onde o Premium está disponível para Linux.</span><span class="sxs-lookup"><span data-stu-id="543d1-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="543d1-113">Exemplo 3: obter os locais onde o consumo está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="543d1-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="543d1-114">Esse comando obtém os locais onde o consumo está disponível para Windows.</span><span class="sxs-lookup"><span data-stu-id="543d1-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="543d1-115">OS</span><span class="sxs-lookup"><span data-stu-id="543d1-115">PARAMETERS</span></span>

### <span data-ttu-id="543d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="543d1-116">-DefaultProfile</span></span>
<span data-ttu-id="543d1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="543d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="543d1-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="543d1-118">-OSType</span></span>
<span data-ttu-id="543d1-119">O tipo de sistema operacional do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="543d1-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="543d1-120">-Plantype</span><span class="sxs-lookup"><span data-stu-id="543d1-120">-PlanType</span></span>
<span data-ttu-id="543d1-121">O tipo de plano.</span><span class="sxs-lookup"><span data-stu-id="543d1-121">The plan type.</span></span>
<span data-ttu-id="543d1-122">Entradas válidas: consumo ou Premium</span><span class="sxs-lookup"><span data-stu-id="543d1-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="543d1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="543d1-123">-SubscriptionId</span></span>
<span data-ttu-id="543d1-124">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="543d1-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="543d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="543d1-125">CommonParameters</span></span>
<span data-ttu-id="543d1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="543d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="543d1-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="543d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="543d1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="543d1-128">INPUTS</span></span>

## <span data-ttu-id="543d1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="543d1-129">OUTPUTS</span></span>

### <span data-ttu-id="543d1-130">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="543d1-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="543d1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="543d1-131">NOTES</span></span>

<span data-ttu-id="543d1-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="543d1-132">ALIASES</span></span>

## <span data-ttu-id="543d1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="543d1-133">RELATED LINKS</span></span>

