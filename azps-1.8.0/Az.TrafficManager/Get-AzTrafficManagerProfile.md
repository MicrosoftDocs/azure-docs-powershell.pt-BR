---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: fe97e35c0b4b728601cc33888deb9afbdb0620b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598403"
---
# <span data-ttu-id="eff8a-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="eff8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eff8a-102">SYNOPSIS</span></span>
<span data-ttu-id="eff8a-103">Obtém um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="eff8a-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="eff8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eff8a-104">SYNTAX</span></span>

### <span data-ttu-id="eff8a-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="eff8a-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eff8a-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eff8a-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eff8a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eff8a-107">DESCRIPTION</span></span>
<span data-ttu-id="eff8a-108">O cmdlet **Get-AzTrafficManagerProfile** Obtém um perfil do Gerenciador de tráfego do Azure e retorna um objeto que representa esse perfil.</span><span class="sxs-lookup"><span data-stu-id="eff8a-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="eff8a-109">Especifique um perfil com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eff8a-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="eff8a-110">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao perfil usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="eff8a-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="eff8a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eff8a-111">EXAMPLES</span></span>

### <span data-ttu-id="eff8a-112">Exemplo 1: obter um perfil</span><span class="sxs-lookup"><span data-stu-id="eff8a-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="eff8a-113">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="eff8a-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="eff8a-114">OS</span><span class="sxs-lookup"><span data-stu-id="eff8a-114">PARAMETERS</span></span>

### <span data-ttu-id="eff8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-115">-DefaultProfile</span></span>
<span data-ttu-id="eff8a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eff8a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff8a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="eff8a-117">-Name</span></span>
<span data-ttu-id="eff8a-118">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="eff8a-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eff8a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff8a-119">-ResourceGroupName</span></span>
<span data-ttu-id="eff8a-120">Especifica o nome de um grupo de recursos que contém o perfil do Gerenciador de tráfego que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="eff8a-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eff8a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff8a-121">CommonParameters</span></span>
<span data-ttu-id="eff8a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff8a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff8a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff8a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff8a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eff8a-124">INPUTS</span></span>

### <span data-ttu-id="eff8a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eff8a-125">System.String</span></span>

## <span data-ttu-id="eff8a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eff8a-126">OUTPUTS</span></span>

### <span data-ttu-id="eff8a-127">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="eff8a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eff8a-128">NOTES</span></span>

## <span data-ttu-id="eff8a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eff8a-129">RELATED LINKS</span></span>

[<span data-ttu-id="eff8a-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="eff8a-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="eff8a-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="eff8a-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="eff8a-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff8a-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


