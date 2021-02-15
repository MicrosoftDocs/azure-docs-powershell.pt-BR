---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116285"
---
# <span data-ttu-id="fed71-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="fed71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fed71-102">SYNOPSIS</span></span>
<span data-ttu-id="fed71-103">Desabilita um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="fed71-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="fed71-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fed71-104">SYNTAX</span></span>

### <span data-ttu-id="fed71-105">Campos</span><span class="sxs-lookup"><span data-stu-id="fed71-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed71-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="fed71-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fed71-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fed71-107">DESCRIPTION</span></span>
<span data-ttu-id="fed71-108">O cmdlet **Disable-AzTrafficManagerProfile** desabilita um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="fed71-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="fed71-109">Você pode especificar o objeto de perfil usando o pipeline ou como um valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fed71-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="fed71-110">Como alternativa, você pode especificar o perfil usando os parâmetros *Nome* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="fed71-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="fed71-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fed71-111">EXAMPLES</span></span>

### <span data-ttu-id="fed71-112">Exemplo 1: Desabilitar um perfil especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="fed71-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fed71-113">Esse comando desabilita o perfil chamado ContosoProfile no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fed71-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fed71-114">O comando solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="fed71-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="fed71-115">Exemplo 2: Desabilitar um perfil usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="fed71-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="fed71-116">Esse comando obtém o perfil chamado ContosoProfile no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fed71-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fed71-117">Em seguida, o comando passa esse perfil para o cmdlet **Disable-AzTrafficManagerProfile** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="fed71-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fed71-118">Esse cmdlet desabilita esse perfil.</span><span class="sxs-lookup"><span data-stu-id="fed71-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="fed71-119">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="fed71-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fed71-120">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="fed71-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fed71-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fed71-121">PARAMETERS</span></span>

### <span data-ttu-id="fed71-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-122">-DefaultProfile</span></span>
<span data-ttu-id="fed71-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fed71-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fed71-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="fed71-124">-Force</span></span>
<span data-ttu-id="fed71-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fed71-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fed71-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fed71-126">-Name</span></span>
<span data-ttu-id="fed71-127">Especifica o nome do perfil do Gerenciador de Tráfego desabilitado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed71-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="fed71-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed71-128">-ResourceGroupName</span></span>
<span data-ttu-id="fed71-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fed71-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fed71-130">Esse cmdlet desabilita um perfil do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fed71-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fed71-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="fed71-132">Especifica um objeto **TrafficManagerProfile** a ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fed71-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="fed71-133">Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="fed71-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fed71-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fed71-134">-Confirm</span></span>
<span data-ttu-id="fed71-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed71-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed71-136">-WhatIf</span></span>
<span data-ttu-id="fed71-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fed71-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed71-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fed71-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed71-139">CommonParameters</span></span>
<span data-ttu-id="fed71-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed71-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed71-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed71-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="fed71-142">INPUTS</span></span>

### <span data-ttu-id="fed71-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fed71-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="fed71-144">OUTPUTS</span></span>

### <span data-ttu-id="fed71-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fed71-145">System.Boolean</span></span>

## <span data-ttu-id="fed71-146">Notas</span><span class="sxs-lookup"><span data-stu-id="fed71-146">NOTES</span></span>

## <span data-ttu-id="fed71-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fed71-147">RELATED LINKS</span></span>

[<span data-ttu-id="fed71-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="fed71-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="fed71-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="fed71-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="fed71-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fed71-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


