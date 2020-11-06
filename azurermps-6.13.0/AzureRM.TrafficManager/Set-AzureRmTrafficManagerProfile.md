---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 9536e6250f73270c7700a14406cb24b8e8f31189
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427097"
---
# <span data-ttu-id="6ec1e-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="6ec1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ec1e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec1e-103">Atualiza um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ec1e-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec1e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ec1e-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec1e-106">O cmdlet **set-AzureRmTrafficManagerProfile** atualiza um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6ec1e-107">Esse cmdlet atualiza as configurações do perfil de um objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="6ec1e-108">Você pode especificar o objeto de perfil usando o parâmetro *TrafficManagerProfile* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="6ec1e-109">Você pode obter um objeto local que representa um perfil usando o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="6ec1e-110">Modifique o objeto localmente e use **set-AzureRmTrafficManagerProfile** para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="6ec1e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ec1e-111">EXAMPLES</span></span>

### <span data-ttu-id="6ec1e-112">Exemplo 1: atualizar um perfil</span><span class="sxs-lookup"><span data-stu-id="6ec1e-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="6ec1e-113">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="6ec1e-114">O comando armazena o perfil localmente na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="6ec1e-115">O segundo comando altera esse perfil localmente.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="6ec1e-116">Esse comando desabilita o perfil.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-116">This command disables the profile.</span></span>

<span data-ttu-id="6ec1e-117">O terceiro comando atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="6ec1e-118">OS</span><span class="sxs-lookup"><span data-stu-id="6ec1e-118">PARAMETERS</span></span>

### <span data-ttu-id="6ec1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-119">-DefaultProfile</span></span>
<span data-ttu-id="6ec1e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ec1e-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="6ec1e-122">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6ec1e-123">Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="6ec1e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec1e-124">CommonParameters</span></span>
<span data-ttu-id="6ec1e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec1e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec1e-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec1e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec1e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ec1e-127">INPUTS</span></span>

### <span data-ttu-id="6ec1e-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6ec1e-129">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="6ec1e-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="6ec1e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ec1e-130">OUTPUTS</span></span>

### <span data-ttu-id="6ec1e-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6ec1e-132">Esse cmdlet retorna um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="6ec1e-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="6ec1e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ec1e-133">NOTES</span></span>

## <span data-ttu-id="6ec1e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ec1e-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ec1e-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6ec1e-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6ec1e-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6ec1e-137">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6ec1e-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6ec1e-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6ec1e-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ec1e-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


