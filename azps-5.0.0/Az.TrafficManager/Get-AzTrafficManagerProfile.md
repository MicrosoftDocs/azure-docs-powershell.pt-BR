---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117902"
---
# <span data-ttu-id="b7f19-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="b7f19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7f19-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f19-103">Obtém um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="b7f19-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="b7f19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7f19-104">SYNTAX</span></span>

### <span data-ttu-id="b7f19-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f19-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7f19-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f19-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7f19-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7f19-107">DESCRIPTION</span></span>
<span data-ttu-id="b7f19-108">O cmdlet **Get-AzTrafficManagerProfile** Obtém um perfil do Gerenciador de tráfego do Azure e retorna um objeto que representa esse perfil.</span><span class="sxs-lookup"><span data-stu-id="b7f19-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="b7f19-109">Especifique um perfil com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7f19-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="b7f19-110">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao perfil usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b7f19-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="b7f19-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7f19-111">EXAMPLES</span></span>

### <span data-ttu-id="b7f19-112">Exemplo 1: obter um perfil</span><span class="sxs-lookup"><span data-stu-id="b7f19-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b7f19-113">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b7f19-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="b7f19-114">OS</span><span class="sxs-lookup"><span data-stu-id="b7f19-114">PARAMETERS</span></span>

### <span data-ttu-id="b7f19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-115">-DefaultProfile</span></span>
<span data-ttu-id="b7f19-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f19-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7f19-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7f19-117">-Name</span></span>
<span data-ttu-id="b7f19-118">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b7f19-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7f19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f19-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7f19-120">Especifica o nome de um grupo de recursos que contém o perfil do Gerenciador de tráfego que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b7f19-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7f19-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f19-121">CommonParameters</span></span>
<span data-ttu-id="b7f19-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f19-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f19-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f19-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f19-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7f19-124">INPUTS</span></span>

### <span data-ttu-id="b7f19-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f19-125">System.String</span></span>

## <span data-ttu-id="b7f19-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7f19-126">OUTPUTS</span></span>

### <span data-ttu-id="b7f19-127">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b7f19-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7f19-128">NOTES</span></span>

## <span data-ttu-id="b7f19-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7f19-129">RELATED LINKS</span></span>

[<span data-ttu-id="b7f19-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7f19-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7f19-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7f19-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7f19-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7f19-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


