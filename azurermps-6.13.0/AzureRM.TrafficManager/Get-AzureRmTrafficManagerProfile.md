---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427111"
---
# <span data-ttu-id="fa521-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="fa521-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa521-102">SYNOPSIS</span></span>
<span data-ttu-id="fa521-103">Obtém um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="fa521-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa521-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa521-104">SYNTAX</span></span>

### <span data-ttu-id="fa521-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa521-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa521-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa521-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa521-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa521-107">DESCRIPTION</span></span>
<span data-ttu-id="fa521-108">O cmdlet **Get-AzureRmTrafficManagerProfile** Obtém um perfil do Gerenciador de tráfego do Azure e retorna um objeto que representa esse perfil.</span><span class="sxs-lookup"><span data-stu-id="fa521-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="fa521-109">Especifique um perfil com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa521-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="fa521-110">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao perfil usando o cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fa521-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="fa521-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa521-111">EXAMPLES</span></span>

### <span data-ttu-id="fa521-112">Exemplo 1: obter um perfil</span><span class="sxs-lookup"><span data-stu-id="fa521-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fa521-113">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fa521-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="fa521-114">OS</span><span class="sxs-lookup"><span data-stu-id="fa521-114">PARAMETERS</span></span>

### <span data-ttu-id="fa521-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-115">-DefaultProfile</span></span>
<span data-ttu-id="fa521-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa521-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa521-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa521-117">-Name</span></span>
<span data-ttu-id="fa521-118">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fa521-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa521-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa521-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa521-120">Especifica o nome de um grupo de recursos que contém o perfil do Gerenciador de tráfego que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fa521-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa521-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa521-121">CommonParameters</span></span>
<span data-ttu-id="fa521-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa521-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa521-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa521-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa521-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa521-124">INPUTS</span></span>

### <span data-ttu-id="fa521-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fa521-125">None</span></span>
<span data-ttu-id="fa521-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fa521-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa521-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa521-127">OUTPUTS</span></span>

### <span data-ttu-id="fa521-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="fa521-129">Esse cmdlet retorna um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="fa521-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="fa521-130">Você pode modificar esse objeto e, em seguida, aplicar alterações no Gerenciador de tráfego usando **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="fa521-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="fa521-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa521-131">NOTES</span></span>

## <span data-ttu-id="fa521-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa521-132">RELATED LINKS</span></span>

[<span data-ttu-id="fa521-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fa521-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fa521-135">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fa521-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fa521-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa521-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


