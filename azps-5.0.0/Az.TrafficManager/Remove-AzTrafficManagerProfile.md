---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118440"
---
# <span data-ttu-id="94f4b-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="94f4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="94f4b-103">Exclui um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="94f4b-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="94f4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94f4b-104">SYNTAX</span></span>

### <span data-ttu-id="94f4b-105">Campos</span><span class="sxs-lookup"><span data-stu-id="94f4b-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f4b-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="94f4b-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f4b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94f4b-107">DESCRIPTION</span></span>
<span data-ttu-id="94f4b-108">O cmdlet **Remove-AzTrafficManagerProfile** exclui um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="94f4b-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="94f4b-109">Especifique o perfil a ser excluído usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="94f4b-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="94f4b-110">Como alternativa, você pode especificar um objeto **TrafficManagerProfile** usando o parâmetro *TrafficManagerProfile* ou pode usar o pipeline.</span><span class="sxs-lookup"><span data-stu-id="94f4b-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="94f4b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94f4b-111">EXAMPLES</span></span>

### <span data-ttu-id="94f4b-112">Exemplo 1: excluir um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="94f4b-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="94f4b-113">Esse comando exclui o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="94f4b-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="94f4b-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="94f4b-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="94f4b-115">Exemplo 2: excluir um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="94f4b-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="94f4b-116">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="94f4b-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="94f4b-117">Em seguida, o comando passa o perfil para o cmdlet **Remove-AzTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="94f4b-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94f4b-118">Esse cmdlet exclui esse perfil.</span><span class="sxs-lookup"><span data-stu-id="94f4b-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="94f4b-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="94f4b-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="94f4b-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="94f4b-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="94f4b-121">OS</span><span class="sxs-lookup"><span data-stu-id="94f4b-121">PARAMETERS</span></span>

### <span data-ttu-id="94f4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-122">-DefaultProfile</span></span>
<span data-ttu-id="94f4b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94f4b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f4b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="94f4b-124">-Force</span></span>
<span data-ttu-id="94f4b-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="94f4b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94f4b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="94f4b-126">-Name</span></span>
<span data-ttu-id="94f4b-127">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="94f4b-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="94f4b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f4b-128">-ResourceGroupName</span></span>
<span data-ttu-id="94f4b-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94f4b-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="94f4b-130">Esse cmdlet exclui um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="94f4b-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="94f4b-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="94f4b-132">Especifica um objeto **TrafficManagerProfile** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="94f4b-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="94f4b-133">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="94f4b-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="94f4b-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94f4b-134">-Confirm</span></span>
<span data-ttu-id="94f4b-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f4b-136">-WhatIf</span></span>
<span data-ttu-id="94f4b-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94f4b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f4b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94f4b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f4b-139">CommonParameters</span></span>
<span data-ttu-id="94f4b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f4b-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f4b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f4b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94f4b-142">INPUTS</span></span>

### <span data-ttu-id="94f4b-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="94f4b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94f4b-144">OUTPUTS</span></span>

### <span data-ttu-id="94f4b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94f4b-145">System.Boolean</span></span>

## <span data-ttu-id="94f4b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94f4b-146">NOTES</span></span>

## <span data-ttu-id="94f4b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94f4b-147">RELATED LINKS</span></span>

[<span data-ttu-id="94f4b-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="94f4b-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="94f4b-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="94f4b-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="94f4b-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94f4b-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


