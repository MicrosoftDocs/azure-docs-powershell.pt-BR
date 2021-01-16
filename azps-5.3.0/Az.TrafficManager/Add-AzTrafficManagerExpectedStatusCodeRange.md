---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272286"
---
# <span data-ttu-id="5a0fc-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="5a0fc-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="5a0fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0fc-103">Adiciona um intervalo de código de status esperado a um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="5a0fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a0fc-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a0fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="5a0fc-106">O cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** adiciona um intervalo de códigos de status esperados a um objeto de perfil do Gerenciador de tráfego do Azure local.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="5a0fc-107">Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="5a0fc-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="5a0fc-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="5a0fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a0fc-110">EXAMPLES</span></span>

### <span data-ttu-id="5a0fc-111">Exemplo 1: adicionar um intervalo de código de status esperado a um perfil</span><span class="sxs-lookup"><span data-stu-id="5a0fc-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="5a0fc-112">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="5a0fc-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="5a0fc-113">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="5a0fc-114">O segundo comando adiciona um intervalo de código de status esperado ao perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="5a0fc-115">O comando final atualiza o perfil no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="5a0fc-116">OS</span><span class="sxs-lookup"><span data-stu-id="5a0fc-116">PARAMETERS</span></span>

### <span data-ttu-id="5a0fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0fc-117">-DefaultProfile</span></span>
<span data-ttu-id="5a0fc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a0fc-119">-Máximo</span><span class="sxs-lookup"><span data-stu-id="5a0fc-119">-Max</span></span>
<span data-ttu-id="5a0fc-120">Especifica o maior valor no intervalo de código de status a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0fc-121">-Min</span><span class="sxs-lookup"><span data-stu-id="5a0fc-121">-Min</span></span>
<span data-ttu-id="5a0fc-122">Especifica o valor mais baixo no intervalo de código de status a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0fc-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a0fc-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="5a0fc-124">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5a0fc-125">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="5a0fc-126">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0fc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a0fc-127">-Confirm</span></span>
<span data-ttu-id="5a0fc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0fc-129">-WhatIf</span></span>
<span data-ttu-id="5a0fc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a0fc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0fc-132">CommonParameters</span></span>
<span data-ttu-id="5a0fc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a0fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0fc-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0fc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0fc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a0fc-135">INPUTS</span></span>

### <span data-ttu-id="5a0fc-136">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a0fc-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5a0fc-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a0fc-137">OUTPUTS</span></span>

### <span data-ttu-id="5a0fc-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a0fc-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5a0fc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a0fc-139">NOTES</span></span>

## <span data-ttu-id="5a0fc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a0fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="5a0fc-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="5a0fc-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="5a0fc-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a0fc-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5a0fc-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a0fc-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
