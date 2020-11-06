---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: c3a32c6bab916ad4a63db5e528e00fe3948a1d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602556"
---
# <span data-ttu-id="50d53-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="50d53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50d53-102">SYNOPSIS</span></span>
<span data-ttu-id="50d53-103">Desabilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="50d53-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50d53-104">SYNTAX</span></span>

### <span data-ttu-id="50d53-105">Campos</span><span class="sxs-lookup"><span data-stu-id="50d53-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50d53-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="50d53-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50d53-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50d53-107">DESCRIPTION</span></span>
<span data-ttu-id="50d53-108">O cmdlet **Disable-AzureRmTrafficManagerProfile** desabilita um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="50d53-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="50d53-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="50d53-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="50d53-110">Você também pode especificar o perfil usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="50d53-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="50d53-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50d53-111">EXAMPLES</span></span>

### <span data-ttu-id="50d53-112">Exemplo 1: desabilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="50d53-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="50d53-113">Esse comando desabilita o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="50d53-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="50d53-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="50d53-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="50d53-115">Exemplo 2: desabilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="50d53-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="50d53-116">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="50d53-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="50d53-117">Em seguida, o comando passa esse perfil para o cmdlet **Disable-AzureRmTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="50d53-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50d53-118">Esse cmdlet desabilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="50d53-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="50d53-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="50d53-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="50d53-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="50d53-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="50d53-121">OS</span><span class="sxs-lookup"><span data-stu-id="50d53-121">PARAMETERS</span></span>

### <span data-ttu-id="50d53-122">-Force</span><span class="sxs-lookup"><span data-stu-id="50d53-122">-Force</span></span>
<span data-ttu-id="50d53-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="50d53-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d53-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="50d53-124">-Name</span></span>
<span data-ttu-id="50d53-125">Especifica o nome do perfil do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="50d53-125">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="50d53-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d53-126">-ResourceGroupName</span></span>
<span data-ttu-id="50d53-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="50d53-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="50d53-128">Esse cmdlet desabilita um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="50d53-128">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="50d53-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="50d53-130">Especifica um objeto **TrafficManagerProfile** a ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="50d53-130">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="50d53-131">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="50d53-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="50d53-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="50d53-132">-Confirm</span></span>
<span data-ttu-id="50d53-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50d53-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d53-134">-WhatIf</span></span>
<span data-ttu-id="50d53-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50d53-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d53-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50d53-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d53-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-137">-DefaultProfile</span></span>
<span data-ttu-id="50d53-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50d53-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50d53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d53-139">CommonParameters</span></span>
<span data-ttu-id="50d53-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d53-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d53-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d53-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50d53-142">INPUTS</span></span>

### <span data-ttu-id="50d53-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="50d53-144">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="50d53-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="50d53-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50d53-145">OUTPUTS</span></span>

### <span data-ttu-id="50d53-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50d53-146">System.Boolean</span></span>

## <span data-ttu-id="50d53-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50d53-147">NOTES</span></span>

## <span data-ttu-id="50d53-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50d53-148">RELATED LINKS</span></span>

[<span data-ttu-id="50d53-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="50d53-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="50d53-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="50d53-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="50d53-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


