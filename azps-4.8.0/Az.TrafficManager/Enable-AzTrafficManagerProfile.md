---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114670"
---
# <span data-ttu-id="e4cf9-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="e4cf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4cf9-103">Habilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="e4cf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4cf9-104">SYNTAX</span></span>

### <span data-ttu-id="e4cf9-105">Campos</span><span class="sxs-lookup"><span data-stu-id="e4cf9-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4cf9-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="e4cf9-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4cf9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4cf9-107">DESCRIPTION</span></span>
<span data-ttu-id="e4cf9-108">O cmdlet **Enable-AzTrafficManagerProfile** habilita um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="e4cf9-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="e4cf9-110">Você também pode especificar o perfil usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e4cf9-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="e4cf9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4cf9-111">EXAMPLES</span></span>

### <span data-ttu-id="e4cf9-112">Exemplo 1: habilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="e4cf9-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e4cf9-113">Esse comando habilita o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="e4cf9-114">Exemplo 2: habilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="e4cf9-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="e4cf9-115">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="e4cf9-116">Em seguida, o comando passa o perfil para o cmdlet **Enable-AzTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e4cf9-117">Esse cmdlet habilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="e4cf9-118">OS</span><span class="sxs-lookup"><span data-stu-id="e4cf9-118">PARAMETERS</span></span>

### <span data-ttu-id="e4cf9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-119">-DefaultProfile</span></span>
<span data-ttu-id="e4cf9-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4cf9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4cf9-121">-Name</span></span>
<span data-ttu-id="e4cf9-122">Especifica o nome do perfil do Gerenciador de tráfego que o cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cf9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4cf9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4cf9-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e4cf9-125">Esse cmdlet habilita um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cf9-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="e4cf9-127">Especifica um objeto **TrafficManagerProfile** para habilitar.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="e4cf9-128">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4cf9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4cf9-129">CommonParameters</span></span>
<span data-ttu-id="e4cf9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4cf9-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4cf9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4cf9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4cf9-132">INPUTS</span></span>

### <span data-ttu-id="e4cf9-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e4cf9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4cf9-134">OUTPUTS</span></span>

### <span data-ttu-id="e4cf9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4cf9-135">System.Boolean</span></span>

## <span data-ttu-id="e4cf9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4cf9-136">NOTES</span></span>

## <span data-ttu-id="e4cf9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4cf9-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4cf9-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="e4cf9-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e4cf9-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="e4cf9-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="e4cf9-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf9-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


