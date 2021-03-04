---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889842"
---
# <span data-ttu-id="31e8f-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e8f-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="31e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="31e8f-103">Atualiza um ponto de extremidade do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="31e8f-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="31e8f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="31e8f-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e8f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="31e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="31e8f-106">O cmdlet **Set-AzTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="31e8f-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="31e8f-107">Este cmdlet atualiza as configurações de um objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="31e8f-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="31e8f-108">Você pode especificar o objeto de ponto de extremidade usando o *parâmetro TrafficManagerEndpoint* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="31e8f-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="31e8f-109">Você pode obter um objeto local que representa um ponto de extremidade usando Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e8f-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="31e8f-110">Modifique o objeto localmente e, em seguida, use **Set-AzTrafficManagerEndpoint** para confirmação de suas alterações.</span><span class="sxs-lookup"><span data-stu-id="31e8f-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="31e8f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31e8f-111">EXAMPLES</span></span>

### <span data-ttu-id="31e8f-112">Exemplo 1: atualizar um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="31e8f-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="31e8f-113">O primeiro comando obtém um ponto de extremidade do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="31e8f-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="31e8f-114">O comando armazena o ponto de extremidade localmente na $TrafficManagerEndpoint variável.</span><span class="sxs-lookup"><span data-stu-id="31e8f-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="31e8f-115">O segundo comando altera esse ponto de extremidade localmente.</span><span class="sxs-lookup"><span data-stu-id="31e8f-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="31e8f-116">Este comando altera o peso do ponto de extremidade para 20.</span><span class="sxs-lookup"><span data-stu-id="31e8f-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="31e8f-117">O terceiro comando atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="31e8f-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="31e8f-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="31e8f-118">PARAMETERS</span></span>

### <span data-ttu-id="31e8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e8f-119">-DefaultProfile</span></span>
<span data-ttu-id="31e8f-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="31e8f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e8f-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e8f-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="31e8f-122">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="31e8f-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="31e8f-123">Este cmdlet atualiza o Gerenciador de Tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="31e8f-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31e8f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e8f-124">CommonParameters</span></span>
<span data-ttu-id="31e8f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e8f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e8f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e8f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e8f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31e8f-127">INPUTS</span></span>

### <span data-ttu-id="31e8f-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e8f-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="31e8f-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="31e8f-129">OUTPUTS</span></span>

### <span data-ttu-id="31e8f-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e8f-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="31e8f-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="31e8f-131">NOTES</span></span>

## <span data-ttu-id="31e8f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31e8f-132">RELATED LINKS</span></span>
