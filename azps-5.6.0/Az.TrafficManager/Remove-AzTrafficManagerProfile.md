---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 1b1dab7edc07242dab28daa6028adefb8b7090eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890045"
---
# <span data-ttu-id="7caf9-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="7caf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7caf9-102">SYNOPSIS</span></span>
<span data-ttu-id="7caf9-103">Exclui um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="7caf9-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="7caf9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7caf9-104">SYNTAX</span></span>

### <span data-ttu-id="7caf9-105">Fields</span><span class="sxs-lookup"><span data-stu-id="7caf9-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7caf9-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="7caf9-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7caf9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7caf9-107">DESCRIPTION</span></span>
<span data-ttu-id="7caf9-108">O cmdlet **Remove-AzTrafficManagerProfile** exclui um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="7caf9-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7caf9-109">Especifique o perfil a ser excluído usando os parâmetros *Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="7caf9-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7caf9-110">Como alternativa, você pode especificar um **objeto TrafficManagerProfile** usando o *parâmetro TrafficManagerProfile* ou pode usar o pipeline.</span><span class="sxs-lookup"><span data-stu-id="7caf9-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="7caf9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7caf9-111">EXAMPLES</span></span>

### <span data-ttu-id="7caf9-112">Exemplo 1: Excluir um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="7caf9-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7caf9-113">Este comando exclui o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7caf9-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7caf9-114">O comando solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="7caf9-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7caf9-115">Exemplo 2: excluir um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="7caf9-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="7caf9-116">Este comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7caf9-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7caf9-117">Em seguida, o comando passa esse perfil para o cmdlet **Remove-AzTrafficManagerProfile** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="7caf9-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7caf9-118">Esse cmdlet exclui esse perfil.</span><span class="sxs-lookup"><span data-stu-id="7caf9-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="7caf9-119">O comando especifica o parâmetro *Force.*</span><span class="sxs-lookup"><span data-stu-id="7caf9-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7caf9-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="7caf9-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7caf9-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7caf9-121">PARAMETERS</span></span>

### <span data-ttu-id="7caf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-122">-DefaultProfile</span></span>
<span data-ttu-id="7caf9-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7caf9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7caf9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7caf9-124">-Force</span></span>
<span data-ttu-id="7caf9-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7caf9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7caf9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7caf9-126">-Name</span></span>
<span data-ttu-id="7caf9-127">Especifica o nome do perfil do Gerenciador de Tráfego que esse cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="7caf9-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7caf9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7caf9-128">-ResourceGroupName</span></span>
<span data-ttu-id="7caf9-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7caf9-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7caf9-130">Este cmdlet exclui um perfil do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7caf9-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7caf9-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="7caf9-132">Especifica um **objeto TrafficManagerProfile** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7caf9-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="7caf9-133">Para obter um **objeto TrafficManagerProfile,** use Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7caf9-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7caf9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7caf9-134">-Confirm</span></span>
<span data-ttu-id="7caf9-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7caf9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7caf9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7caf9-136">-WhatIf</span></span>
<span data-ttu-id="7caf9-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7caf9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7caf9-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7caf9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7caf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7caf9-139">CommonParameters</span></span>
<span data-ttu-id="7caf9-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7caf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7caf9-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7caf9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7caf9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7caf9-142">INPUTS</span></span>

### <span data-ttu-id="7caf9-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7caf9-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7caf9-144">OUTPUTS</span></span>

### <span data-ttu-id="7caf9-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7caf9-145">System.Boolean</span></span>

## <span data-ttu-id="7caf9-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="7caf9-146">NOTES</span></span>

## <span data-ttu-id="7caf9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7caf9-147">RELATED LINKS</span></span>

[<span data-ttu-id="7caf9-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="7caf9-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="7caf9-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7caf9-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7caf9-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7caf9-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


