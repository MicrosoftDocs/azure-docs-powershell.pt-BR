---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440794"
---
# <span data-ttu-id="15b2d-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="15b2d-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="15b2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="15b2d-103">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="15b2d-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15b2d-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b2d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="15b2d-106">O cmdlet **New-AzureRmFrontDoorFireWallPolicy** cria uma nova política do Azure WAF no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="15b2d-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="15b2d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15b2d-107">EXAMPLES</span></span>

### <span data-ttu-id="15b2d-108">Exemplo 1: criar uma política WAF</span><span class="sxs-lookup"><span data-stu-id="15b2d-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="15b2d-109">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="15b2d-109">Create WAF policy</span></span>

## <span data-ttu-id="15b2d-110">OS</span><span class="sxs-lookup"><span data-stu-id="15b2d-110">PARAMETERS</span></span>

### <span data-ttu-id="15b2d-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="15b2d-111">-Customrule</span></span>
<span data-ttu-id="15b2d-112">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="15b2d-112">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b2d-113">-DefaultProfile</span></span>
<span data-ttu-id="15b2d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15b2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15b2d-115">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="15b2d-115">-EnabledState</span></span>
<span data-ttu-id="15b2d-116">Se a política está no estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="15b2d-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="15b2d-117">Os valores possíveis incluem: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="15b2d-117">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="15b2d-118">-ManagedRule</span></span>
<span data-ttu-id="15b2d-119">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="15b2d-119">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="15b2d-120">-Mode</span></span>
<span data-ttu-id="15b2d-121">Descreve se ele está no modo de detecção ou no modo de prevenção em nível de política.</span><span class="sxs-lookup"><span data-stu-id="15b2d-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="15b2d-122">Os valores possíveis incluem: ' Prevention ', ' detecção '</span><span class="sxs-lookup"><span data-stu-id="15b2d-122">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="15b2d-123">-Name</span></span>
<span data-ttu-id="15b2d-124">Nome do WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="15b2d-124">WebApplicationFireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b2d-125">-ResourceGroupName</span></span>
<span data-ttu-id="15b2d-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="15b2d-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15b2d-127">-Confirm</span></span>
<span data-ttu-id="15b2d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b2d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b2d-129">-WhatIf</span></span>
<span data-ttu-id="15b2d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15b2d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b2d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15b2d-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b2d-132">CommonParameters</span></span>
<span data-ttu-id="15b2d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b2d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b2d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b2d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15b2d-135">INPUTS</span></span>

### <span data-ttu-id="15b2d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="15b2d-136">System.String</span></span>

## <span data-ttu-id="15b2d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15b2d-137">OUTPUTS</span></span>

### <span data-ttu-id="15b2d-138">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="15b2d-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="15b2d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15b2d-139">NOTES</span></span>

## <span data-ttu-id="15b2d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15b2d-140">RELATED LINKS</span></span>

<span data-ttu-id="15b2d-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="15b2d-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
