---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112365"
---
# <span data-ttu-id="e9964-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="e9964-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9964-102">SYNOPSIS</span></span>
<span data-ttu-id="e9964-103">Remove informações personalizadas do header de um objeto de perfil local do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="e9964-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="e9964-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9964-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9964-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9964-105">DESCRIPTION</span></span>
<span data-ttu-id="e9964-106">O cmdlet **Remove-AzTrafficManagerCusagerCustomHeaderFromProfile** remove informações personalizadas do header de um objeto de perfil local do Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e9964-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="e9964-107">Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="e9964-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="e9964-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="e9964-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="e9964-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9964-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="e9964-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9964-110">EXAMPLES</span></span>

### <span data-ttu-id="e9964-111">Exemplo 1: Remover informações personalizadas do header de um perfil</span><span class="sxs-lookup"><span data-stu-id="e9964-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="e9964-112">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="e9964-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="e9964-113">O segundo comando remove informações personalizadas do header do perfil armazenado no $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e9964-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="e9964-114">O comando final atualiza o perfil no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e9964-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="e9964-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9964-115">PARAMETERS</span></span>

### <span data-ttu-id="e9964-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-116">-DefaultProfile</span></span>
<span data-ttu-id="e9964-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e9964-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9964-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9964-118">-Name</span></span>
<span data-ttu-id="e9964-119">Especifica o nome das informações de cabeça personalizadas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="e9964-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="e9964-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="e9964-121">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="e9964-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="e9964-122">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="e9964-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e9964-123">Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="e9964-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="e9964-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e9964-124">-Confirm</span></span>
<span data-ttu-id="e9964-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9964-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9964-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9964-126">-WhatIf</span></span>
<span data-ttu-id="e9964-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e9964-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9964-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9964-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9964-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9964-129">CommonParameters</span></span>
<span data-ttu-id="e9964-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9964-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9964-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9964-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9964-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="e9964-132">INPUTS</span></span>

### <span data-ttu-id="e9964-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e9964-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="e9964-134">OUTPUTS</span></span>

### <span data-ttu-id="e9964-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e9964-136">Notas</span><span class="sxs-lookup"><span data-stu-id="e9964-136">NOTES</span></span>

## <span data-ttu-id="e9964-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9964-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9964-138">Add-AzTrafficManagerCusagerHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="e9964-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e9964-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e9964-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
