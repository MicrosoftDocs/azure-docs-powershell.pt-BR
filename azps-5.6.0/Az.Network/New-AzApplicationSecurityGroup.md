---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: d0fcdff243294210449eb32f99faa3d9d74cef0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888625"
---
# <span data-ttu-id="80820-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80820-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="80820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80820-102">SYNOPSIS</span></span>
<span data-ttu-id="80820-103">Cria um grupo de segurança de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="80820-103">Creates an application security group.</span></span>

## <span data-ttu-id="80820-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80820-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80820-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80820-105">DESCRIPTION</span></span>
<span data-ttu-id="80820-106">O cmdlet **New-AzApplicationSecurityGroup** cria um grupo de segurança de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="80820-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="80820-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80820-107">EXAMPLES</span></span>

### <span data-ttu-id="80820-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80820-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="80820-109">Este exemplo cria um grupo de segurança de aplicativos sem associações.</span><span class="sxs-lookup"><span data-stu-id="80820-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="80820-110">Depois de criada, as configurações IP na interface de rede podem ser incluídas no grupo.</span><span class="sxs-lookup"><span data-stu-id="80820-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="80820-111">As regras de segurança também podem se referir ao grupo como suas fontes ou destinos.</span><span class="sxs-lookup"><span data-stu-id="80820-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="80820-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80820-112">PARAMETERS</span></span>

### <span data-ttu-id="80820-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80820-113">-AsJob</span></span>
<span data-ttu-id="80820-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="80820-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80820-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80820-115">-DefaultProfile</span></span>
<span data-ttu-id="80820-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="80820-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80820-117">-Force</span><span class="sxs-lookup"><span data-stu-id="80820-117">-Force</span></span>
<span data-ttu-id="80820-118">Não peça confirmação se quiser substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="80820-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="80820-119">-Location</span><span class="sxs-lookup"><span data-stu-id="80820-119">-Location</span></span>
<span data-ttu-id="80820-120">O local.</span><span class="sxs-lookup"><span data-stu-id="80820-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80820-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80820-121">-Name</span></span>
<span data-ttu-id="80820-122">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="80820-122">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80820-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80820-123">-ResourceGroupName</span></span>
<span data-ttu-id="80820-124">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="80820-124">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80820-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="80820-125">-Tag</span></span>
<span data-ttu-id="80820-126">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="80820-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80820-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80820-127">-Confirm</span></span>
<span data-ttu-id="80820-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80820-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80820-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80820-129">-WhatIf</span></span>
<span data-ttu-id="80820-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80820-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80820-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80820-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80820-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80820-132">CommonParameters</span></span>
<span data-ttu-id="80820-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80820-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80820-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80820-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80820-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80820-135">INPUTS</span></span>

### <span data-ttu-id="80820-136">System.String</span><span class="sxs-lookup"><span data-stu-id="80820-136">System.String</span></span>

### <span data-ttu-id="80820-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="80820-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80820-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80820-138">OUTPUTS</span></span>

### <span data-ttu-id="80820-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80820-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="80820-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="80820-140">NOTES</span></span>

## <span data-ttu-id="80820-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80820-141">RELATED LINKS</span></span>

[<span data-ttu-id="80820-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80820-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="80820-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80820-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="80820-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80820-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="80820-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80820-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="80820-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80820-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="80820-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80820-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="80820-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80820-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="80820-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80820-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
