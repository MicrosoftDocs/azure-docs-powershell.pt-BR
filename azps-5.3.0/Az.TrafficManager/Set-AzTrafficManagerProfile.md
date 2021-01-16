---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429590"
---
# <span data-ttu-id="aa417-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="aa417-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa417-102">SYNOPSIS</span></span>
<span data-ttu-id="aa417-103">Atualiza um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="aa417-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="aa417-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa417-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa417-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa417-105">DESCRIPTION</span></span>
<span data-ttu-id="aa417-106">O cmdlet **set-AzTrafficManagerProfile** atualiza um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa417-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="aa417-107">Esse cmdlet atualiza as configurações do perfil de um objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="aa417-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="aa417-108">Você pode especificar o objeto de perfil usando o parâmetro *TrafficManagerProfile* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa417-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="aa417-109">Você pode obter um objeto local que representa um perfil usando o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="aa417-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="aa417-110">Modifique o objeto localmente e use **set-AzTrafficManagerProfile** para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="aa417-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="aa417-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa417-111">EXAMPLES</span></span>

### <span data-ttu-id="aa417-112">Exemplo 1: atualizar um perfil</span><span class="sxs-lookup"><span data-stu-id="aa417-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="aa417-113">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="aa417-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="aa417-114">O comando armazena o perfil localmente na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="aa417-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="aa417-115">O segundo comando altera esse perfil localmente.</span><span class="sxs-lookup"><span data-stu-id="aa417-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="aa417-116">Esse comando desabilita o perfil.</span><span class="sxs-lookup"><span data-stu-id="aa417-116">This command disables the profile.</span></span>

<span data-ttu-id="aa417-117">O terceiro comando atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="aa417-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="aa417-118">OS</span><span class="sxs-lookup"><span data-stu-id="aa417-118">PARAMETERS</span></span>

### <span data-ttu-id="aa417-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-119">-DefaultProfile</span></span>
<span data-ttu-id="aa417-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa417-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa417-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="aa417-122">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="aa417-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="aa417-123">Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="aa417-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="aa417-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa417-124">CommonParameters</span></span>
<span data-ttu-id="aa417-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa417-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa417-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa417-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa417-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa417-127">INPUTS</span></span>

### <span data-ttu-id="aa417-128">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="aa417-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa417-129">OUTPUTS</span></span>

### <span data-ttu-id="aa417-130">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="aa417-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa417-131">NOTES</span></span>

## <span data-ttu-id="aa417-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa417-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa417-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="aa417-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="aa417-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="aa417-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="aa417-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="aa417-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="aa417-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aa417-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


