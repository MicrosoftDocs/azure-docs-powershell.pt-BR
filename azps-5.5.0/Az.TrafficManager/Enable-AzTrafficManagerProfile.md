---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116281"
---
# <span data-ttu-id="433c5-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="433c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="433c5-102">SYNOPSIS</span></span>
<span data-ttu-id="433c5-103">Habilita um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="433c5-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="433c5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="433c5-104">SYNTAX</span></span>

### <span data-ttu-id="433c5-105">Campos</span><span class="sxs-lookup"><span data-stu-id="433c5-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433c5-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="433c5-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433c5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="433c5-107">DESCRIPTION</span></span>
<span data-ttu-id="433c5-108">O cmdlet **Enable-AzTrafficManagerProfile** habilita um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="433c5-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="433c5-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="433c5-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="433c5-110">Como alternativa, você pode especificar o perfil usando os parâmetros *Nome* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="433c5-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="433c5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="433c5-111">EXAMPLES</span></span>

### <span data-ttu-id="433c5-112">Exemplo 1: Habilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="433c5-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="433c5-113">Esse comando habilita o perfil chamado ContosoProfile no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="433c5-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="433c5-114">Exemplo 2: Habilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="433c5-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="433c5-115">Esse comando obtém o perfil chamado ContosoProfile no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="433c5-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="433c5-116">Em seguida, o comando passa esse perfil para o cmdlet **Enable-AzTrafficManagerProfile** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="433c5-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="433c5-117">Esse cmdlet habilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="433c5-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="433c5-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="433c5-118">PARAMETERS</span></span>

### <span data-ttu-id="433c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-119">-DefaultProfile</span></span>
<span data-ttu-id="433c5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="433c5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="433c5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="433c5-121">-Name</span></span>
<span data-ttu-id="433c5-122">Especifica o nome do perfil do Gerenciador de Tráfego que esse cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="433c5-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="433c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="433c5-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="433c5-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="433c5-125">Esse cmdlet habilita um perfil do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="433c5-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="433c5-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="433c5-127">Especifica um objeto **TrafficManagerProfile** para habilitar.</span><span class="sxs-lookup"><span data-stu-id="433c5-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="433c5-128">Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="433c5-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="433c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433c5-129">CommonParameters</span></span>
<span data-ttu-id="433c5-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433c5-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="433c5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433c5-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="433c5-132">INPUTS</span></span>

### <span data-ttu-id="433c5-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="433c5-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="433c5-134">OUTPUTS</span></span>

### <span data-ttu-id="433c5-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="433c5-135">System.Boolean</span></span>

## <span data-ttu-id="433c5-136">Notas</span><span class="sxs-lookup"><span data-stu-id="433c5-136">NOTES</span></span>

## <span data-ttu-id="433c5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="433c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="433c5-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="433c5-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="433c5-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="433c5-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="433c5-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="433c5-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


