---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429638"
---
# <span data-ttu-id="710f4-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="710f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="710f4-102">SYNOPSIS</span></span>
<span data-ttu-id="710f4-103">Exclui um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="710f4-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="710f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="710f4-104">SYNTAX</span></span>

### <span data-ttu-id="710f4-105">Campos</span><span class="sxs-lookup"><span data-stu-id="710f4-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="710f4-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="710f4-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="710f4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="710f4-107">DESCRIPTION</span></span>
<span data-ttu-id="710f4-108">O cmdlet **Remove-AzureRmTrafficManagerProfile** exclui um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="710f4-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="710f4-109">Especifique o perfil a ser excluído usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="710f4-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="710f4-110">Como alternativa, você pode especificar um objeto **TrafficManagerProfile** usando o parâmetro *TrafficManagerProfile* ou pode usar o pipeline.</span><span class="sxs-lookup"><span data-stu-id="710f4-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="710f4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="710f4-111">EXAMPLES</span></span>

### <span data-ttu-id="710f4-112">Exemplo 1: excluir um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="710f4-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="710f4-113">Esse comando exclui o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="710f4-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="710f4-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="710f4-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="710f4-115">Exemplo 2: excluir um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="710f4-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="710f4-116">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="710f4-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="710f4-117">Em seguida, o comando passa o perfil para o cmdlet **Remove-AzureRmTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="710f4-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="710f4-118">Esse cmdlet exclui esse perfil.</span><span class="sxs-lookup"><span data-stu-id="710f4-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="710f4-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="710f4-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="710f4-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="710f4-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="710f4-121">OS</span><span class="sxs-lookup"><span data-stu-id="710f4-121">PARAMETERS</span></span>

### <span data-ttu-id="710f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-122">-DefaultProfile</span></span>
<span data-ttu-id="710f4-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="710f4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="710f4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="710f4-124">-Force</span></span>
<span data-ttu-id="710f4-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="710f4-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="710f4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="710f4-126">-Name</span></span>
<span data-ttu-id="710f4-127">Especifica o nome do perfil do Gerenciador de tráfego que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="710f4-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="710f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="710f4-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="710f4-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="710f4-130">Esse cmdlet exclui um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="710f4-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="710f4-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="710f4-132">Especifica um objeto **TrafficManagerProfile** a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="710f4-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="710f4-133">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="710f4-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="710f4-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="710f4-134">-Confirm</span></span>
<span data-ttu-id="710f4-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="710f4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="710f4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="710f4-136">-WhatIf</span></span>
<span data-ttu-id="710f4-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="710f4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="710f4-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="710f4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="710f4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710f4-139">CommonParameters</span></span>
<span data-ttu-id="710f4-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="710f4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710f4-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710f4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710f4-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="710f4-142">INPUTS</span></span>

### <span data-ttu-id="710f4-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="710f4-144">Esse cmdlet aceita um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="710f4-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="710f4-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="710f4-145">OUTPUTS</span></span>

### <span data-ttu-id="710f4-146">Booliana</span><span class="sxs-lookup"><span data-stu-id="710f4-146">Boolean</span></span>
<span data-ttu-id="710f4-147">Esse cmdlet retorna um valor de $True, se tiver êxito ou, se a exclusão falhar, um valor de $False.</span><span class="sxs-lookup"><span data-stu-id="710f4-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="710f4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="710f4-148">NOTES</span></span>

## <span data-ttu-id="710f4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="710f4-149">RELATED LINKS</span></span>

[<span data-ttu-id="710f4-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="710f4-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="710f4-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="710f4-153">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="710f4-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


