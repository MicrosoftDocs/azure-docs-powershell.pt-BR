---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125878"
---
# <span data-ttu-id="c1fc4-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1fc4-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c1fc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fc4-103">Atualiza um ponto de extremidade do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="c1fc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1fc4-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1fc4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="c1fc4-106">O cmdlet **set-AzTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="c1fc4-107">Esse cmdlet atualiza as configurações de um objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="c1fc4-108">Você pode especificar o objeto de ponto de extremidade usando o parâmetro *TrafficManagerEndpoint* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="c1fc4-109">Você pode obter um objeto local que representa um ponto de extremidade usando o cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="c1fc4-110">Modifique o objeto localmente e use **set-AzTrafficManagerEndpoint** para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="c1fc4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1fc4-111">EXAMPLES</span></span>

### <span data-ttu-id="c1fc4-112">Exemplo 1: atualizar um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="c1fc4-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="c1fc4-113">O primeiro comando obtém um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="c1fc4-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="c1fc4-114">O comando armazena o ponto de extremidade localmente na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="c1fc4-115">O segundo comando altera esse ponto de extremidade localmente.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="c1fc4-116">Esse comando altera a espessura do ponto de extremidade para 20.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="c1fc4-117">O terceiro comando atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="c1fc4-118">OS</span><span class="sxs-lookup"><span data-stu-id="c1fc4-118">PARAMETERS</span></span>

### <span data-ttu-id="c1fc4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fc4-119">-DefaultProfile</span></span>
<span data-ttu-id="c1fc4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1fc4-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1fc4-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c1fc4-122">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="c1fc4-123">Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="c1fc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fc4-124">CommonParameters</span></span>
<span data-ttu-id="c1fc4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fc4-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fc4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fc4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1fc4-127">INPUTS</span></span>

### <span data-ttu-id="c1fc4-128">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1fc4-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c1fc4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1fc4-129">OUTPUTS</span></span>

### <span data-ttu-id="c1fc4-130">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1fc4-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c1fc4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1fc4-131">NOTES</span></span>

## <span data-ttu-id="c1fc4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1fc4-132">RELATED LINKS</span></span>
