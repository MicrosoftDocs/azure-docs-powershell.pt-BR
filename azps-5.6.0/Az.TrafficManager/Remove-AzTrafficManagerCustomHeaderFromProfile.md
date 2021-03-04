---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 1026f5e34c2b8efc17503a81a521a0ceb3d92060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890499"
---
# <span data-ttu-id="bb28d-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="bb28d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb28d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb28d-103">Remove informações de header personalizadas de um objeto de perfil do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="bb28d-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="bb28d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb28d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb28d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb28d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb28d-106">O cmdlet **Remove-AzTrafficManagerCustomHeaderFromProfile** remove informações de header personalizadas de um objeto de perfil local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb28d-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="bb28d-107">Você pode obter um perfil usando os New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile cmdlets.</span><span class="sxs-lookup"><span data-stu-id="bb28d-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="bb28d-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="bb28d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="bb28d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb28d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="bb28d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb28d-110">EXAMPLES</span></span>

### <span data-ttu-id="bb28d-111">Exemplo 1: Remover informações de header personalizadas de um perfil</span><span class="sxs-lookup"><span data-stu-id="bb28d-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="bb28d-112">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="bb28d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="bb28d-113">O segundo comando remove informações de header personalizadas do perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="bb28d-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="bb28d-114">O comando final atualiza o perfil no Gerenciador de Tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="bb28d-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="bb28d-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb28d-115">PARAMETERS</span></span>

### <span data-ttu-id="bb28d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-116">-DefaultProfile</span></span>
<span data-ttu-id="bb28d-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bb28d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb28d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bb28d-118">-Name</span></span>
<span data-ttu-id="bb28d-119">Especifica o nome das informações de header personalizadas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="bb28d-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="bb28d-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="bb28d-121">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="bb28d-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="bb28d-122">Este cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="bb28d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="bb28d-123">Para obter um **objeto TrafficManagerProfile,** use Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb28d-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bb28d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb28d-124">-Confirm</span></span>
<span data-ttu-id="bb28d-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb28d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb28d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb28d-126">-WhatIf</span></span>
<span data-ttu-id="bb28d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb28d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb28d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb28d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb28d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb28d-129">CommonParameters</span></span>
<span data-ttu-id="bb28d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb28d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb28d-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb28d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb28d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb28d-132">INPUTS</span></span>

### <span data-ttu-id="bb28d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="bb28d-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb28d-134">OUTPUTS</span></span>

### <span data-ttu-id="bb28d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="bb28d-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb28d-136">NOTES</span></span>

## <span data-ttu-id="bb28d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb28d-137">RELATED LINKS</span></span>

[<span data-ttu-id="bb28d-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="bb28d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="bb28d-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb28d-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
