---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114348"
---
# <span data-ttu-id="7e722-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="7e722-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="7e722-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e722-102">SYNOPSIS</span></span>
<span data-ttu-id="7e722-103">Remove um intervalo de código de status esperado de um objeto de perfil local do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="7e722-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="7e722-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e722-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e722-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e722-105">DESCRIPTION</span></span>
<span data-ttu-id="7e722-106">O cmdlet **Remove-AzTrafficManagerExpectedStatusCodeRange remove** um intervalo de códigos de status esperados de um objeto de perfil local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e722-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="7e722-107">Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="7e722-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="7e722-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="7e722-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="7e722-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e722-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="7e722-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7e722-110">EXAMPLES</span></span>

### <span data-ttu-id="7e722-111">Exemplo 1: remover um intervalo de código de status esperado de um perfil</span><span class="sxs-lookup"><span data-stu-id="7e722-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="7e722-112">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="7e722-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="7e722-113">O segundo comando remove um intervalo de código de status esperado do perfil armazenado no $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="7e722-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="7e722-114">O comando final atualiza o perfil no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="7e722-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="7e722-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e722-115">PARAMETERS</span></span>

### <span data-ttu-id="7e722-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e722-116">-DefaultProfile</span></span>
<span data-ttu-id="7e722-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7e722-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e722-118">-Mín</span><span class="sxs-lookup"><span data-stu-id="7e722-118">-Min</span></span>
<span data-ttu-id="7e722-119">Especifica o valor mais baixo no intervalo de código de status a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7e722-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="7e722-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e722-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="7e722-121">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="7e722-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="7e722-122">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="7e722-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7e722-123">Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="7e722-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7e722-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7e722-124">-Confirm</span></span>
<span data-ttu-id="7e722-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e722-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e722-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e722-126">-WhatIf</span></span>
<span data-ttu-id="7e722-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7e722-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e722-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e722-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e722-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e722-129">CommonParameters</span></span>
<span data-ttu-id="7e722-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e722-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e722-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e722-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e722-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="7e722-132">INPUTS</span></span>

### <span data-ttu-id="7e722-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e722-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7e722-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="7e722-134">OUTPUTS</span></span>

### <span data-ttu-id="7e722-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e722-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7e722-136">Notas</span><span class="sxs-lookup"><span data-stu-id="7e722-136">NOTES</span></span>

## <span data-ttu-id="7e722-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e722-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e722-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="7e722-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="7e722-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e722-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e722-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e722-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
