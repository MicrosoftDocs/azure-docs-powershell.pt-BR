---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889838"
---
# <span data-ttu-id="10f3b-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="10f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="10f3b-103">Atualiza um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="10f3b-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="10f3b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10f3b-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10f3b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="10f3b-106">O cmdlet **Set-AzTrafficManagerProfile** atualiza um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="10f3b-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="10f3b-107">Este cmdlet atualiza as configurações do perfil de um objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="10f3b-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="10f3b-108">Você pode especificar o objeto de perfil usando o *parâmetro TrafficManagerProfile* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="10f3b-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="10f3b-109">Você pode obter um objeto local que representa um perfil usando Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f3b-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="10f3b-110">Modifique o objeto localmente e, em seguida, use **Set-AzTrafficManagerProfile** para comprometer suas alterações.</span><span class="sxs-lookup"><span data-stu-id="10f3b-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="10f3b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10f3b-111">EXAMPLES</span></span>

### <span data-ttu-id="10f3b-112">Exemplo 1: atualizar um perfil</span><span class="sxs-lookup"><span data-stu-id="10f3b-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="10f3b-113">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f3b-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="10f3b-114">O comando armazena o perfil localmente na $TrafficManagerProfile variável.</span><span class="sxs-lookup"><span data-stu-id="10f3b-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="10f3b-115">O segundo comando altera esse perfil localmente.</span><span class="sxs-lookup"><span data-stu-id="10f3b-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="10f3b-116">Este comando desabilita o perfil.</span><span class="sxs-lookup"><span data-stu-id="10f3b-116">This command disables the profile.</span></span>

<span data-ttu-id="10f3b-117">O terceiro comando atualiza o perfil do Gerenciador de Tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10f3b-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="10f3b-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10f3b-118">PARAMETERS</span></span>

### <span data-ttu-id="10f3b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-119">-DefaultProfile</span></span>
<span data-ttu-id="10f3b-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="10f3b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10f3b-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="10f3b-122">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="10f3b-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="10f3b-123">Este cmdlet atualiza o Gerenciador de Tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="10f3b-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="10f3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f3b-124">CommonParameters</span></span>
<span data-ttu-id="10f3b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f3b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10f3b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f3b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10f3b-127">INPUTS</span></span>

### <span data-ttu-id="10f3b-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="10f3b-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10f3b-129">OUTPUTS</span></span>

### <span data-ttu-id="10f3b-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="10f3b-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="10f3b-131">NOTES</span></span>

## <span data-ttu-id="10f3b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10f3b-132">RELATED LINKS</span></span>

[<span data-ttu-id="10f3b-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="10f3b-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="10f3b-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="10f3b-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="10f3b-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="10f3b-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="10f3b-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


