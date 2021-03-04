---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889845"
---
# <span data-ttu-id="69797-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="69797-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="69797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69797-102">SYNOPSIS</span></span>
<span data-ttu-id="69797-103">Remove um intervalo de código de status esperado de um objeto de perfil do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="69797-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="69797-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69797-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69797-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69797-105">DESCRIPTION</span></span>
<span data-ttu-id="69797-106">O cmdlet **Remove-AzTrafficManagerExpectedStatusCodeRange** remove um intervalo de códigos de status esperados de um objeto de perfil local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="69797-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="69797-107">Você pode obter um perfil usando os New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile cmdlets.</span><span class="sxs-lookup"><span data-stu-id="69797-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="69797-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="69797-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="69797-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69797-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="69797-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69797-110">EXAMPLES</span></span>

### <span data-ttu-id="69797-111">Exemplo 1: Remover um intervalo de código de status esperado de um perfil</span><span class="sxs-lookup"><span data-stu-id="69797-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="69797-112">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="69797-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="69797-113">O segundo comando remove um intervalo de código de status esperado do perfil armazenado $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="69797-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="69797-114">O comando final atualiza o perfil no Gerenciador de Tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="69797-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="69797-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69797-115">PARAMETERS</span></span>

### <span data-ttu-id="69797-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69797-116">-DefaultProfile</span></span>
<span data-ttu-id="69797-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="69797-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69797-118">-Min</span><span class="sxs-lookup"><span data-stu-id="69797-118">-Min</span></span>
<span data-ttu-id="69797-119">Especifica o valor mais baixo no intervalo de código de status a ser removido.</span><span class="sxs-lookup"><span data-stu-id="69797-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="69797-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69797-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="69797-121">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="69797-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="69797-122">Este cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="69797-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="69797-123">Para obter um **objeto TrafficManagerProfile,** use Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69797-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="69797-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69797-124">-Confirm</span></span>
<span data-ttu-id="69797-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69797-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69797-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69797-126">-WhatIf</span></span>
<span data-ttu-id="69797-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69797-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69797-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69797-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69797-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69797-129">CommonParameters</span></span>
<span data-ttu-id="69797-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69797-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69797-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69797-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69797-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69797-132">INPUTS</span></span>

### <span data-ttu-id="69797-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69797-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="69797-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69797-134">OUTPUTS</span></span>

### <span data-ttu-id="69797-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69797-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="69797-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="69797-136">NOTES</span></span>

## <span data-ttu-id="69797-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69797-137">RELATED LINKS</span></span>

[<span data-ttu-id="69797-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="69797-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="69797-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69797-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="69797-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69797-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
