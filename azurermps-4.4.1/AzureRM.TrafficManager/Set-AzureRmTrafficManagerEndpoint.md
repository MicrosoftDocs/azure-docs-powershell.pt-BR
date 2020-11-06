---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432158"
---
# <span data-ttu-id="3dd36-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dd36-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="3dd36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3dd36-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd36-103">Atualiza um ponto de extremidade do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="3dd36-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dd36-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dd36-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3dd36-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd36-106">O cmdlet **set-AzureRmTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd36-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="3dd36-107">Esse cmdlet atualiza as configurações de um objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="3dd36-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="3dd36-108">Você pode especificar o objeto de ponto de extremidade usando o parâmetro *TrafficManagerEndpoint* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="3dd36-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="3dd36-109">Você pode obter um objeto local que representa um ponto de extremidade usando o cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3dd36-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="3dd36-110">Modifique o objeto localmente e use **set-AzureRmTrafficManagerEndpoint** para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="3dd36-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="3dd36-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dd36-111">EXAMPLES</span></span>

### <span data-ttu-id="3dd36-112">Exemplo 1: atualizar um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3dd36-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="3dd36-113">O primeiro comando obtém um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="3dd36-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="3dd36-114">O comando armazena o ponto de extremidade localmente na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3dd36-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="3dd36-115">O segundo comando altera esse ponto de extremidade localmente.</span><span class="sxs-lookup"><span data-stu-id="3dd36-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="3dd36-116">Esse comando altera a espessura do ponto de extremidade para 20.</span><span class="sxs-lookup"><span data-stu-id="3dd36-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="3dd36-117">O terceiro comando atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3dd36-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="3dd36-118">OS</span><span class="sxs-lookup"><span data-stu-id="3dd36-118">PARAMETERS</span></span>

### <span data-ttu-id="3dd36-119">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dd36-119">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3dd36-120">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="3dd36-120">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="3dd36-121">Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="3dd36-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="3dd36-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd36-122">-DefaultProfile</span></span>
<span data-ttu-id="3dd36-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd36-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd36-124">CommonParameters</span></span>
<span data-ttu-id="3dd36-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd36-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd36-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd36-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3dd36-127">INPUTS</span></span>

### <span data-ttu-id="3dd36-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dd36-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="3dd36-129">Esse cmdlet aceita um objeto **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="3dd36-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="3dd36-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3dd36-130">OUTPUTS</span></span>

### <span data-ttu-id="3dd36-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dd36-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="3dd36-132">Esse cmdlet retorna um objeto **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="3dd36-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="3dd36-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3dd36-133">NOTES</span></span>

## <span data-ttu-id="3dd36-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dd36-134">RELATED LINKS</span></span>

