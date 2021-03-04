---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: 3d843729a9ab51e5a4e1ecf1952f778537e8bf11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889851"
---
# <span data-ttu-id="65aee-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="65aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65aee-102">SYNOPSIS</span></span>
<span data-ttu-id="65aee-103">Obtém um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="65aee-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="65aee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65aee-104">SYNTAX</span></span>

### <span data-ttu-id="65aee-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="65aee-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65aee-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="65aee-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65aee-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65aee-107">DESCRIPTION</span></span>
<span data-ttu-id="65aee-108">O cmdlet **Get-AzTrafficManagerProfile** obtém um perfil do Gerenciador de Tráfego do Azure e retorna um objeto que representa esse perfil.</span><span class="sxs-lookup"><span data-stu-id="65aee-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="65aee-109">Especifique um perfil pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65aee-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="65aee-110">Você pode modificar esse objeto localmente e aplicar alterações ao perfil usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65aee-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="65aee-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65aee-111">EXAMPLES</span></span>

### <span data-ttu-id="65aee-112">Exemplo 1: Obter um perfil</span><span class="sxs-lookup"><span data-stu-id="65aee-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="65aee-113">Este comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="65aee-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="65aee-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65aee-114">PARAMETERS</span></span>

### <span data-ttu-id="65aee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-115">-DefaultProfile</span></span>
<span data-ttu-id="65aee-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65aee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65aee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="65aee-117">-Name</span></span>
<span data-ttu-id="65aee-118">Especifica o nome do perfil do Gerenciador de Tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="65aee-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="65aee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65aee-119">-ResourceGroupName</span></span>
<span data-ttu-id="65aee-120">Especifica o nome de um grupo de recursos que contém o perfil do Gerenciador de Tráfego que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="65aee-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="65aee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65aee-121">CommonParameters</span></span>
<span data-ttu-id="65aee-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65aee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65aee-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65aee-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65aee-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65aee-124">INPUTS</span></span>

### <span data-ttu-id="65aee-125">System.String</span><span class="sxs-lookup"><span data-stu-id="65aee-125">System.String</span></span>

## <span data-ttu-id="65aee-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65aee-126">OUTPUTS</span></span>

### <span data-ttu-id="65aee-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="65aee-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="65aee-128">NOTES</span></span>

## <span data-ttu-id="65aee-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65aee-129">RELATED LINKS</span></span>

[<span data-ttu-id="65aee-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="65aee-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="65aee-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="65aee-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="65aee-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65aee-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


