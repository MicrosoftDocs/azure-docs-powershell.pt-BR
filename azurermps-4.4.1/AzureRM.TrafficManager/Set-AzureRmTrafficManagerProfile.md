---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e8baf033131442f23a0db63339673018b209f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603080"
---
# <span data-ttu-id="9b0c3-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="9b0c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0c3-103">Atualiza um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b0c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b0c3-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b0c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="9b0c3-106">O cmdlet **set-AzureRmTrafficManagerProfile** atualiza um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9b0c3-107">Esse cmdlet atualiza as configurações do perfil de um objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="9b0c3-108">Você pode especificar o objeto de perfil usando o parâmetro *TrafficManagerProfile* ou usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="9b0c3-109">Você pode obter um objeto local que representa um perfil usando o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9b0c3-110">Modifique o objeto localmente e use **set-AzureRmTrafficManagerProfile** para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="9b0c3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b0c3-111">EXAMPLES</span></span>

### <span data-ttu-id="9b0c3-112">Exemplo 1: atualizar um perfil</span><span class="sxs-lookup"><span data-stu-id="9b0c3-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9b0c3-113">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9b0c3-114">O comando armazena o perfil localmente na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="9b0c3-115">O segundo comando altera esse perfil localmente.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="9b0c3-116">Esse comando desabilita o perfil.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-116">This command disables the profile.</span></span>

<span data-ttu-id="9b0c3-117">O terceiro comando atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9b0c3-118">OS</span><span class="sxs-lookup"><span data-stu-id="9b0c3-118">PARAMETERS</span></span>

### <span data-ttu-id="9b0c3-119">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-119">-TrafficManagerProfile</span></span>
<span data-ttu-id="9b0c3-120">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-120">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9b0c3-121">Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="9b0c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-122">-DefaultProfile</span></span>
<span data-ttu-id="9b0c3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b0c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0c3-124">CommonParameters</span></span>
<span data-ttu-id="9b0c3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b0c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0c3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b0c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0c3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b0c3-127">INPUTS</span></span>

### <span data-ttu-id="9b0c3-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9b0c3-129">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9b0c3-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9b0c3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b0c3-130">OUTPUTS</span></span>

### <span data-ttu-id="9b0c3-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9b0c3-132">Esse cmdlet retorna um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9b0c3-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9b0c3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b0c3-133">NOTES</span></span>

## <span data-ttu-id="9b0c3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b0c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b0c3-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9b0c3-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9b0c3-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9b0c3-137">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9b0c3-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9b0c3-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9b0c3-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b0c3-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


