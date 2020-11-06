---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 8e43fd59184d8d07688c5ac3d4a8a8cc872745f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427100"
---
# <span data-ttu-id="292e7-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="292e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="292e7-102">SYNOPSIS</span></span>
<span data-ttu-id="292e7-103">Exclui um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="292e7-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="292e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="292e7-104">SYNTAX</span></span>

### <span data-ttu-id="292e7-105">Campos</span><span class="sxs-lookup"><span data-stu-id="292e7-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="292e7-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="292e7-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="292e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="292e7-107">DESCRIPTION</span></span>
<span data-ttu-id="292e7-108">O cmdlet **Remove-AzureRmTrafficManagerProfile** exclui um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="292e7-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="292e7-109">Especifique o perfil a ser excluído usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="292e7-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="292e7-110">Como alternativa, você pode especificar um objeto **TrafficManagerProfile** usando o parâmetro *TrafficManagerProfile* ou pode usar o pipeline.</span><span class="sxs-lookup"><span data-stu-id="292e7-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="292e7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="292e7-111">EXAMPLES</span></span>

### <span data-ttu-id="292e7-112">Exemplo 1: excluir um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="292e7-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="292e7-113">Esse comando exclui o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="292e7-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="292e7-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="292e7-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="292e7-115">Exemplo 2: excluir um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="292e7-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="292e7-116">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="292e7-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="292e7-117">Em seguida, o comando passa o perfil para o cmdlet **Remove-AzureRmTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="292e7-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="292e7-118">Esse cmdlet exclui esse perfil.</span><span class="sxs-lookup"><span data-stu-id="292e7-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="292e7-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="292e7-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="292e7-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="292e7-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="292e7-121">OS</span><span class="sxs-lookup"><span data-stu-id="292e7-121">PARAMETERS</span></span>

### <span data-ttu-id="292e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-122">-DefaultProfile</span></span>
<span data-ttu-id="292e7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="292e7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="292e7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="292e7-124">-Force</span></span>
<span data-ttu-id="292e7-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="292e7-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="292e7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="292e7-126">-Name</span></span>
<span data-ttu-id="292e7-127">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="292e7-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="292e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="292e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="292e7-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="292e7-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="292e7-130">Esse cmdlet exclui um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="292e7-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="292e7-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="292e7-132">Especifica um objeto **TrafficManagerProfile** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="292e7-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="292e7-133">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="292e7-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="292e7-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="292e7-134">-Confirm</span></span>
<span data-ttu-id="292e7-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="292e7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="292e7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="292e7-136">-WhatIf</span></span>
<span data-ttu-id="292e7-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="292e7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="292e7-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="292e7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="292e7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292e7-139">CommonParameters</span></span>
<span data-ttu-id="292e7-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292e7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292e7-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="292e7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292e7-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="292e7-142">INPUTS</span></span>

### <span data-ttu-id="292e7-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="292e7-144">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="292e7-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="292e7-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="292e7-145">OUTPUTS</span></span>

### <span data-ttu-id="292e7-146">Booliana</span><span class="sxs-lookup"><span data-stu-id="292e7-146">Boolean</span></span>
<span data-ttu-id="292e7-147">Esse cmdlet retorna um valor de $True, se tiver êxito ou, se a exclusão falhar, um valor de $False.</span><span class="sxs-lookup"><span data-stu-id="292e7-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="292e7-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="292e7-148">NOTES</span></span>

## <span data-ttu-id="292e7-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="292e7-149">RELATED LINKS</span></span>

[<span data-ttu-id="292e7-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="292e7-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="292e7-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="292e7-153">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="292e7-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="292e7-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


