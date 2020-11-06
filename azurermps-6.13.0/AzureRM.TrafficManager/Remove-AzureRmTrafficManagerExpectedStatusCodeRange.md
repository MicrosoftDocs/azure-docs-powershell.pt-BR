---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427102"
---
# <span data-ttu-id="9b4f6-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9b4f6-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="9b4f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4f6-103">Remove um intervalo de código de status esperado de um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b4f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b4f6-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b4f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="9b4f6-106">O cmdlet **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** remove um intervalo de códigos de status esperados de um objeto de perfil do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9b4f6-107">Você pode obter um perfil usando os cmdlets New-AzureRmTrafficManagerProfile ou Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="9b4f6-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9b4f6-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9b4f6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b4f6-110">EXAMPLES</span></span>

### <span data-ttu-id="9b4f6-111">Exemplo 1: remover um intervalo de código de status esperado de um perfil</span><span class="sxs-lookup"><span data-stu-id="9b4f6-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9b4f6-112">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9b4f6-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9b4f6-113">O segundo comando Remove um intervalo de código de status esperado do perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9b4f6-114">O comando final atualiza o perfil no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9b4f6-115">OS</span><span class="sxs-lookup"><span data-stu-id="9b4f6-115">PARAMETERS</span></span>

### <span data-ttu-id="9b4f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-116">-DefaultProfile</span></span>
<span data-ttu-id="9b4f6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b4f6-118">-Min</span><span class="sxs-lookup"><span data-stu-id="9b4f6-118">-Min</span></span>
<span data-ttu-id="9b4f6-119">Especifica o valor mais baixo no intervalo de código de status a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="9b4f6-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="9b4f6-121">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9b4f6-122">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9b4f6-123">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9b4f6-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b4f6-124">-Confirm</span></span>
<span data-ttu-id="9b4f6-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b4f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b4f6-126">-WhatIf</span></span>
<span data-ttu-id="9b4f6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b4f6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b4f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4f6-129">CommonParameters</span></span>
<span data-ttu-id="9b4f6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4f6-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4f6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4f6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b4f6-132">INPUTS</span></span>

### <span data-ttu-id="9b4f6-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9b4f6-134">Este cmdlet aceita um objeto **TrafficManagerProfile** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="9b4f6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b4f6-135">OUTPUTS</span></span>

### <span data-ttu-id="9b4f6-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9b4f6-137">Esse cmdlet retorna um objeto **TrafficManagerProfile** modificado.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9b4f6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b4f6-138">NOTES</span></span>

## <span data-ttu-id="9b4f6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b4f6-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b4f6-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9b4f6-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="9b4f6-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9b4f6-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
