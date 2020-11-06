---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432371"
---
# <span data-ttu-id="012a6-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="012a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="012a6-102">SYNOPSIS</span></span>
<span data-ttu-id="012a6-103">Obtém um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="012a6-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="012a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="012a6-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="012a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="012a6-105">DESCRIPTION</span></span>
<span data-ttu-id="012a6-106">O cmdlet **Get-AzureRmTrafficManagerProfile** Obtém um perfil do Gerenciador de tráfego do Azure e retorna um objeto que representa esse perfil.</span><span class="sxs-lookup"><span data-stu-id="012a6-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="012a6-107">Especifique um perfil com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="012a6-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="012a6-108">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao perfil usando o cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="012a6-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="012a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="012a6-109">EXAMPLES</span></span>

### <span data-ttu-id="012a6-110">Exemplo 1: obter um perfil</span><span class="sxs-lookup"><span data-stu-id="012a6-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="012a6-111">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="012a6-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="012a6-112">OS</span><span class="sxs-lookup"><span data-stu-id="012a6-112">PARAMETERS</span></span>

### <span data-ttu-id="012a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-113">-DefaultProfile</span></span>
<span data-ttu-id="012a6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="012a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012a6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="012a6-115">-Name</span></span>
<span data-ttu-id="012a6-116">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="012a6-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="012a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="012a6-118">Especifica o nome de um grupo de recursos que contém o perfil do Gerenciador de tráfego que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="012a6-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012a6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012a6-119">CommonParameters</span></span>
<span data-ttu-id="012a6-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="012a6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012a6-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="012a6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012a6-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="012a6-122">INPUTS</span></span>

### <span data-ttu-id="012a6-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="012a6-123">None</span></span>
<span data-ttu-id="012a6-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="012a6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="012a6-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="012a6-125">OUTPUTS</span></span>

### <span data-ttu-id="012a6-126">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="012a6-127">Esse cmdlet retorna um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="012a6-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="012a6-128">Você pode modificar esse objeto e, em seguida, aplicar alterações no Gerenciador de tráfego usando **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="012a6-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="012a6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="012a6-129">NOTES</span></span>

## <span data-ttu-id="012a6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="012a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="012a6-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="012a6-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="012a6-133">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="012a6-134">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="012a6-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="012a6-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


