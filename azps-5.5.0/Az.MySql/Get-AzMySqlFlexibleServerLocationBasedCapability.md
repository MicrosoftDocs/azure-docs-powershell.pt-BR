---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 20c142df2a3df0ea6448c2bcb58ad47169d9e483
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111740"
---
# <span data-ttu-id="2dfaf-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="2dfaf-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="2dfaf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfaf-103">Obter as informações de SKU disponíveis para o local</span><span class="sxs-lookup"><span data-stu-id="2dfaf-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="2dfaf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dfaf-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2dfaf-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2dfaf-105">DESCRIPTION</span></span>
<span data-ttu-id="2dfaf-106">Obter as informações de SKU disponíveis para o local</span><span class="sxs-lookup"><span data-stu-id="2dfaf-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="2dfaf-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2dfaf-107">EXAMPLES</span></span>

### <span data-ttu-id="2dfaf-108">Exemplo 1: Obter recursos de localização por nome de local</span><span class="sxs-lookup"><span data-stu-id="2dfaf-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerLocationBasedCapability -Location westus2
"Please refer to https://aka.ms/mysql-pricing for pricing details"

SKU               Tier            Memory vCore
---               ----            ------ -----
Standard_B1s      Burstable         1024     1
Standard_B1ms     Burstable         2048     1
Standard_B2s      Burstable         2048     2
Standard_D2ds_v4  GeneralPurpose    4096     2
Standard_D4ds_v4  GeneralPurpose    4096     4
Standard_D8ds_v4  GeneralPurpose    4096     8
Standard_D16ds_v4 GeneralPurpose    4096    16
Standard_D32ds_v4 GeneralPurpose    4096    32
Standard_D48ds_v4 GeneralPurpose    4096    48
Standard_D64ds_v4 GeneralPurpose    4096    64
Standard_E2ds_v4  MemoryOptimized   8192     2
Standard_E4ds_v4  MemoryOptimized   8192     4
Standard_E8ds_v4  MemoryOptimized   8192     8
Standard_E16ds_v4 MemoryOptimized   8192    16
Standard_E32ds_v4 MemoryOptimized   8192    32
Standard_E48ds_v4 MemoryOptimized   8192    48
Standard_E64ds_v4 MemoryOptimized   8192    64

```

<span data-ttu-id="2dfaf-109">Este cmdlet mostra informações básicas sobre a SKU do local fornecido.</span><span class="sxs-lookup"><span data-stu-id="2dfaf-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="2dfaf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dfaf-110">PARAMETERS</span></span>

### <span data-ttu-id="2dfaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfaf-111">-DefaultProfile</span></span>
<span data-ttu-id="2dfaf-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dfaf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfaf-113">-Local</span><span class="sxs-lookup"><span data-stu-id="2dfaf-113">-Location</span></span>
<span data-ttu-id="2dfaf-114">O nome do local.</span><span class="sxs-lookup"><span data-stu-id="2dfaf-114">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfaf-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2dfaf-115">-SubscriptionId</span></span>
<span data-ttu-id="2dfaf-116">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2dfaf-116">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfaf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfaf-117">CommonParameters</span></span>
<span data-ttu-id="2dfaf-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dfaf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfaf-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dfaf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfaf-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="2dfaf-120">INPUTS</span></span>

## <span data-ttu-id="2dfaf-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="2dfaf-121">OUTPUTS</span></span>

### <span data-ttu-id="2dfaf-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="2dfaf-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="2dfaf-123">Notas</span><span class="sxs-lookup"><span data-stu-id="2dfaf-123">NOTES</span></span>

<span data-ttu-id="2dfaf-124">Aliases</span><span class="sxs-lookup"><span data-stu-id="2dfaf-124">ALIASES</span></span>

## <span data-ttu-id="2dfaf-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dfaf-125">RELATED LINKS</span></span>

