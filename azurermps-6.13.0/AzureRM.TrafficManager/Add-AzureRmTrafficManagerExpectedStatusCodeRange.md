---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426251"
---
# <span data-ttu-id="9d30a-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9d30a-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="9d30a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d30a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d30a-103">Adiciona um intervalo de código de status esperado a um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="9d30a-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d30a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d30a-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d30a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d30a-105">DESCRIPTION</span></span>
<span data-ttu-id="9d30a-106">O cmdlet **Add-AzureRmTrafficManagerExpectedStatusCodeRange** adiciona um intervalo de códigos de status esperados a um objeto de perfil do Gerenciador de tráfego do Azure local.</span><span class="sxs-lookup"><span data-stu-id="9d30a-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9d30a-107">Você pode obter um perfil usando os cmdlets New-AzureRmTrafficManagerProfile ou Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d30a-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="9d30a-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="9d30a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9d30a-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d30a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9d30a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d30a-110">EXAMPLES</span></span>

### <span data-ttu-id="9d30a-111">Exemplo 1: adicionar um intervalo de código de status esperado a um perfil</span><span class="sxs-lookup"><span data-stu-id="9d30a-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9d30a-112">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9d30a-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9d30a-113">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d30a-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="9d30a-114">O segundo comando adiciona um intervalo de código de status esperado ao perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d30a-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9d30a-115">O comando final atualiza o perfil no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d30a-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9d30a-116">OS</span><span class="sxs-lookup"><span data-stu-id="9d30a-116">PARAMETERS</span></span>

### <span data-ttu-id="9d30a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d30a-117">-DefaultProfile</span></span>
<span data-ttu-id="9d30a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d30a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d30a-119">-Máximo</span><span class="sxs-lookup"><span data-stu-id="9d30a-119">-Max</span></span>
<span data-ttu-id="9d30a-120">Especifica o maior valor no intervalo de código de status a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="9d30a-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="9d30a-121">-Min</span><span class="sxs-lookup"><span data-stu-id="9d30a-121">-Min</span></span>
<span data-ttu-id="9d30a-122">Especifica o valor mais baixo no intervalo de código de status a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="9d30a-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="9d30a-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d30a-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="9d30a-124">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="9d30a-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9d30a-125">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="9d30a-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9d30a-126">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d30a-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9d30a-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d30a-127">-Confirm</span></span>
<span data-ttu-id="9d30a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d30a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d30a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d30a-129">-WhatIf</span></span>
<span data-ttu-id="9d30a-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d30a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d30a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d30a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d30a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d30a-132">CommonParameters</span></span>
<span data-ttu-id="9d30a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d30a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d30a-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d30a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d30a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d30a-135">INPUTS</span></span>

### <span data-ttu-id="9d30a-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d30a-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9d30a-137">Este cmdlet aceita um objeto **TrafficManagerProfile** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d30a-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="9d30a-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d30a-138">OUTPUTS</span></span>

### <span data-ttu-id="9d30a-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d30a-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9d30a-140">Esse cmdlet retorna um objeto **TrafficManagerProfile** modificado.</span><span class="sxs-lookup"><span data-stu-id="9d30a-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9d30a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d30a-141">NOTES</span></span>

## <span data-ttu-id="9d30a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d30a-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d30a-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9d30a-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="9d30a-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d30a-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9d30a-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d30a-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
