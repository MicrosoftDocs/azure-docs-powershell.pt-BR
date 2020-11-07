---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: 4479cad8117c078c3d863b58cd764a388f78cd28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773144"
---
# <span data-ttu-id="d23a3-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="d23a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d23a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d23a3-103">Adiciona informações de cabeçalho personalizadas a um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="d23a3-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="d23a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d23a3-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d23a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d23a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d23a3-106">O cmdlet **Add-AzTrafficManagerCustomHeaderToProfile** adiciona informações de cabeçalho personalizadas a um objeto de perfil do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="d23a3-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="d23a3-107">Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d23a3-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="d23a3-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="d23a3-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="d23a3-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d23a3-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="d23a3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d23a3-110">EXAMPLES</span></span>

### <span data-ttu-id="d23a3-111">Exemplo 1: adicionar informações de cabeçalho personalizado a um perfil</span><span class="sxs-lookup"><span data-stu-id="d23a3-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="d23a3-112">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="d23a3-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d23a3-113">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d23a3-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="d23a3-114">O segundo comando adiciona informações de cabeçalho personalizado ao perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d23a3-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d23a3-115">O comando final atualiza o perfil no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d23a3-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="d23a3-116">OS</span><span class="sxs-lookup"><span data-stu-id="d23a3-116">PARAMETERS</span></span>

### <span data-ttu-id="d23a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-117">-DefaultProfile</span></span>
<span data-ttu-id="d23a3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d23a3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d23a3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d23a3-119">-Name</span></span>
<span data-ttu-id="d23a3-120">Especifica o nome das informações de cabeçalho personalizado a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="d23a3-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d23a3-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="d23a3-122">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="d23a3-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d23a3-123">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="d23a3-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d23a3-124">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d23a3-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d23a3-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="d23a3-125">-Value</span></span>
<span data-ttu-id="d23a3-126">Especifica o valor das informações de cabeçalho personalizado a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="d23a3-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d23a3-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d23a3-127">-Confirm</span></span>
<span data-ttu-id="d23a3-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23a3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d23a3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23a3-129">-WhatIf</span></span>
<span data-ttu-id="d23a3-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d23a3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d23a3-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d23a3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d23a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23a3-132">CommonParameters</span></span>
<span data-ttu-id="d23a3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23a3-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23a3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23a3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d23a3-135">INPUTS</span></span>

### <span data-ttu-id="d23a3-136">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d23a3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d23a3-137">OUTPUTS</span></span>

### <span data-ttu-id="d23a3-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d23a3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d23a3-139">NOTES</span></span>

## <span data-ttu-id="d23a3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d23a3-140">RELATED LINKS</span></span>

[<span data-ttu-id="d23a3-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="d23a3-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d23a3-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d23a3-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)