---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112359"
---
# <span data-ttu-id="ae28b-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae28b-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ae28b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae28b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae28b-103">Atualiza um ponto de extremidade do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="ae28b-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="ae28b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae28b-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae28b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae28b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae28b-106">O cmdlet **Set-AzTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae28b-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="ae28b-107">Este cmdlet atualiza as configurações de um objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="ae28b-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="ae28b-108">Você pode especificar o objeto do ponto de extremidade usando o parâmetro *TrafficManagerEndpoint* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae28b-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="ae28b-109">Você pode obter um objeto local que representa um ponto de extremidade usando Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae28b-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="ae28b-110">Modifique o objeto localmente e use **Set-AzTrafficManagerEndpoint** para comprometer suas alterações.</span><span class="sxs-lookup"><span data-stu-id="ae28b-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="ae28b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae28b-111">EXAMPLES</span></span>

### <span data-ttu-id="ae28b-112">Exemplo 1: Atualizar um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="ae28b-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="ae28b-113">O primeiro comando obtém um ponto de extremidade do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="ae28b-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="ae28b-114">O comando armazena o ponto de extremidade localmente na variável $TrafficManagerEndpoint dados.</span><span class="sxs-lookup"><span data-stu-id="ae28b-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="ae28b-115">O segundo comando altera esse ponto de extremidade localmente.</span><span class="sxs-lookup"><span data-stu-id="ae28b-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="ae28b-116">Esse comando altera a peso do ponto de extremidade para 20.</span><span class="sxs-lookup"><span data-stu-id="ae28b-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="ae28b-117">O terceiro comando atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ae28b-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="ae28b-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae28b-118">PARAMETERS</span></span>

### <span data-ttu-id="ae28b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae28b-119">-DefaultProfile</span></span>
<span data-ttu-id="ae28b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ae28b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae28b-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae28b-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ae28b-122">Especifica um objeto **Local TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="ae28b-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="ae28b-123">Este cmdlet atualiza o Gerenciador de Tráfego para corresponder a este objeto local.</span><span class="sxs-lookup"><span data-stu-id="ae28b-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="ae28b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae28b-124">CommonParameters</span></span>
<span data-ttu-id="ae28b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae28b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae28b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae28b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae28b-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="ae28b-127">INPUTS</span></span>

### <span data-ttu-id="ae28b-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae28b-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ae28b-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="ae28b-129">OUTPUTS</span></span>

### <span data-ttu-id="ae28b-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae28b-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ae28b-131">Notas</span><span class="sxs-lookup"><span data-stu-id="ae28b-131">NOTES</span></span>

## <span data-ttu-id="ae28b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae28b-132">RELATED LINKS</span></span>
