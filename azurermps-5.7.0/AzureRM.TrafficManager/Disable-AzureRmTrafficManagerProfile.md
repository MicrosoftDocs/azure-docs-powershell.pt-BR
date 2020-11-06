---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603202"
---
# <span data-ttu-id="f1b3e-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="f1b3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b3e-103">Desabilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1b3e-104">SYNTAX</span></span>

### <span data-ttu-id="f1b3e-105">Campos</span><span class="sxs-lookup"><span data-stu-id="f1b3e-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1b3e-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="f1b3e-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1b3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b3e-108">O cmdlet **Disable-AzureRmTrafficManagerProfile** desabilita um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f1b3e-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="f1b3e-110">Você também pode especificar o perfil usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f1b3e-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="f1b3e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1b3e-111">EXAMPLES</span></span>

### <span data-ttu-id="f1b3e-112">Exemplo 1: desabilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="f1b3e-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f1b3e-113">Esse comando desabilita o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f1b3e-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f1b3e-115">Exemplo 2: desabilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="f1b3e-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="f1b3e-116">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f1b3e-117">Em seguida, o comando passa esse perfil para o cmdlet **Disable-AzureRmTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f1b3e-118">Esse cmdlet desabilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="f1b3e-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f1b3e-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f1b3e-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f1b3e-121">OS</span><span class="sxs-lookup"><span data-stu-id="f1b3e-121">PARAMETERS</span></span>

### <span data-ttu-id="f1b3e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-122">-DefaultProfile</span></span>
<span data-ttu-id="f1b3e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1b3e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f1b3e-124">-Force</span></span>
<span data-ttu-id="f1b3e-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b3e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1b3e-126">-Name</span></span>
<span data-ttu-id="f1b3e-127">Especifica o nome do perfil do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b3e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b3e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1b3e-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f1b3e-130">Esse cmdlet desabilita um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b3e-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="f1b3e-132">Especifica um objeto **TrafficManagerProfile** a ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="f1b3e-133">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b3e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1b3e-134">-Confirm</span></span>
<span data-ttu-id="f1b3e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b3e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b3e-136">-WhatIf</span></span>
<span data-ttu-id="f1b3e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b3e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b3e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b3e-139">CommonParameters</span></span>
<span data-ttu-id="f1b3e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b3e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b3e-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b3e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b3e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1b3e-142">INPUTS</span></span>

### <span data-ttu-id="f1b3e-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f1b3e-144">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f1b3e-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f1b3e-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1b3e-145">OUTPUTS</span></span>

### <span data-ttu-id="f1b3e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1b3e-146">System.Boolean</span></span>

## <span data-ttu-id="f1b3e-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1b3e-147">NOTES</span></span>

## <span data-ttu-id="f1b3e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1b3e-148">RELATED LINKS</span></span>

[<span data-ttu-id="f1b3e-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1b3e-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1b3e-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1b3e-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1b3e-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1b3e-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


