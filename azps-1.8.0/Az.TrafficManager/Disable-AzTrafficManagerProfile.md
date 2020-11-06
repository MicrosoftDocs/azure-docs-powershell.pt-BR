---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: e0702c8893aad7f82de5de5681d8cc14da0b3681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598408"
---
# <span data-ttu-id="41e18-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="41e18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41e18-102">SYNOPSIS</span></span>
<span data-ttu-id="41e18-103">Desabilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="41e18-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="41e18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41e18-104">SYNTAX</span></span>

### <span data-ttu-id="41e18-105">Campos</span><span class="sxs-lookup"><span data-stu-id="41e18-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41e18-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="41e18-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41e18-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41e18-107">DESCRIPTION</span></span>
<span data-ttu-id="41e18-108">O cmdlet **Disable-AzTrafficManagerProfile** desabilita um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="41e18-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="41e18-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="41e18-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="41e18-110">Você também pode especificar o perfil usando os parâmetros *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="41e18-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="41e18-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41e18-111">EXAMPLES</span></span>

### <span data-ttu-id="41e18-112">Exemplo 1: desabilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="41e18-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="41e18-113">Esse comando desabilita o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="41e18-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="41e18-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="41e18-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="41e18-115">Exemplo 2: desabilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="41e18-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="41e18-116">Esse comando obtém o perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="41e18-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="41e18-117">Em seguida, o comando passa esse perfil para o cmdlet **Disable-AzTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="41e18-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41e18-118">Esse cmdlet desabilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="41e18-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="41e18-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="41e18-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="41e18-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="41e18-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="41e18-121">OS</span><span class="sxs-lookup"><span data-stu-id="41e18-121">PARAMETERS</span></span>

### <span data-ttu-id="41e18-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-122">-DefaultProfile</span></span>
<span data-ttu-id="41e18-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41e18-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41e18-124">-Force</span><span class="sxs-lookup"><span data-stu-id="41e18-124">-Force</span></span>
<span data-ttu-id="41e18-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="41e18-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41e18-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="41e18-126">-Name</span></span>
<span data-ttu-id="41e18-127">Especifica o nome do perfil do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="41e18-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="41e18-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e18-128">-ResourceGroupName</span></span>
<span data-ttu-id="41e18-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41e18-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="41e18-130">Esse cmdlet desabilita um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41e18-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="41e18-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="41e18-132">Especifica um objeto **TrafficManagerProfile** a ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="41e18-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="41e18-133">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="41e18-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="41e18-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41e18-134">-Confirm</span></span>
<span data-ttu-id="41e18-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41e18-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e18-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e18-136">-WhatIf</span></span>
<span data-ttu-id="41e18-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41e18-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e18-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41e18-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e18-139">CommonParameters</span></span>
<span data-ttu-id="41e18-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e18-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e18-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e18-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41e18-142">INPUTS</span></span>

### <span data-ttu-id="41e18-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="41e18-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41e18-144">OUTPUTS</span></span>

### <span data-ttu-id="41e18-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41e18-145">System.Boolean</span></span>

## <span data-ttu-id="41e18-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41e18-146">NOTES</span></span>

## <span data-ttu-id="41e18-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41e18-147">RELATED LINKS</span></span>

[<span data-ttu-id="41e18-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="41e18-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="41e18-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="41e18-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="41e18-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="41e18-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


