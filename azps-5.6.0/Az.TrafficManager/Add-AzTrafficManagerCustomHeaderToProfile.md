---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: 8421027f751aab64f5a9e63e08dafca4471d3169
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889865"
---
# <span data-ttu-id="2b7b5-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="2b7b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7b5-103">Adiciona informações de header personalizadas a um objeto de perfil do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="2b7b5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b7b5-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b7b5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7b5-106">O cmdlet **Add-AzTrafficManagerCustomHeaderToProfile** adiciona informações de header personalizadas a um objeto de perfil local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2b7b5-107">Você pode obter um perfil usando os New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="2b7b5-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2b7b5-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="2b7b5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7b5-111">Exemplo 1: Adicionar informações de header personalizadas a um perfil</span><span class="sxs-lookup"><span data-stu-id="2b7b5-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2b7b5-112">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="2b7b5-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2b7b5-113">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="2b7b5-114">O segundo comando adiciona informações de header personalizadas ao perfil armazenado $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2b7b5-115">O comando final atualiza o perfil no Gerenciador de Tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2b7b5-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-116">PARAMETERS</span></span>

### <span data-ttu-id="2b7b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-117">-DefaultProfile</span></span>
<span data-ttu-id="2b7b5-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b7b5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2b7b5-119">-Name</span></span>
<span data-ttu-id="2b7b5-120">Especifica o nome das informações de header personalizadas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2b7b5-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="2b7b5-122">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2b7b5-123">Este cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2b7b5-124">Para obter um **objeto TrafficManagerProfile,** use Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2b7b5-125">-Value</span><span class="sxs-lookup"><span data-stu-id="2b7b5-125">-Value</span></span>
<span data-ttu-id="2b7b5-126">Especifica o valor das informações de header personalizadas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2b7b5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b7b5-127">-Confirm</span></span>
<span data-ttu-id="2b7b5-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7b5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7b5-129">-WhatIf</span></span>
<span data-ttu-id="2b7b5-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b7b5-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7b5-132">CommonParameters</span></span>
<span data-ttu-id="2b7b5-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7b5-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7b5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7b5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-135">INPUTS</span></span>

### <span data-ttu-id="2b7b5-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2b7b5-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-137">OUTPUTS</span></span>

### <span data-ttu-id="2b7b5-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2b7b5-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b7b5-139">NOTES</span></span>

## <span data-ttu-id="2b7b5-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b7b5-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="2b7b5-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2b7b5-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
