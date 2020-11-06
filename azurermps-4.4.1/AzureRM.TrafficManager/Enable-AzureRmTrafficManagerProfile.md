---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 7f3849e1cabcd2fc838255bb312f5bfe5959e088
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431756"
---
# <span data-ttu-id="d4711-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="d4711-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4711-102">SYNOPSIS</span></span>
<span data-ttu-id="d4711-103">Habilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="d4711-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4711-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4711-104">SYNTAX</span></span>

### <span data-ttu-id="d4711-105">Campos</span><span class="sxs-lookup"><span data-stu-id="d4711-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4711-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="d4711-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4711-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4711-107">DESCRIPTION</span></span>
<span data-ttu-id="d4711-108">O cmdlet **Enable-AzureRmTrafficManagerProfile** habilita um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4711-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d4711-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d4711-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="d4711-110">Você também pode especificar o perfil usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d4711-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d4711-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4711-111">EXAMPLES</span></span>

### <span data-ttu-id="d4711-112">Exemplo 1: habilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="d4711-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d4711-113">Esse comando habilita o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d4711-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="d4711-114">Exemplo 2: habilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d4711-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="d4711-115">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d4711-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="d4711-116">Em seguida, o comando passa o perfil para o cmdlet **Enable-AzureRmTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d4711-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d4711-117">Esse cmdlet habilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="d4711-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="d4711-118">OS</span><span class="sxs-lookup"><span data-stu-id="d4711-118">PARAMETERS</span></span>

### <span data-ttu-id="d4711-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4711-119">-Name</span></span>
<span data-ttu-id="d4711-120">Especifica o nome do perfil do Gerenciador de tráfego que o cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="d4711-120">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="d4711-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4711-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4711-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4711-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d4711-123">Esse cmdlet habilita um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d4711-123">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d4711-124">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-124">-TrafficManagerProfile</span></span>
<span data-ttu-id="d4711-125">Especifica um objeto **TrafficManagerProfile** para habilitar.</span><span class="sxs-lookup"><span data-stu-id="d4711-125">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="d4711-126">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d4711-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d4711-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-127">-DefaultProfile</span></span>
<span data-ttu-id="d4711-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4711-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4711-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4711-129">CommonParameters</span></span>
<span data-ttu-id="d4711-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4711-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4711-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4711-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4711-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4711-132">INPUTS</span></span>

### <span data-ttu-id="d4711-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="d4711-134">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="d4711-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="d4711-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4711-135">OUTPUTS</span></span>

### <span data-ttu-id="d4711-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4711-136">System.Boolean</span></span>

## <span data-ttu-id="d4711-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4711-137">NOTES</span></span>

## <span data-ttu-id="d4711-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4711-138">RELATED LINKS</span></span>

[<span data-ttu-id="d4711-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d4711-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d4711-141">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d4711-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d4711-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d4711-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


