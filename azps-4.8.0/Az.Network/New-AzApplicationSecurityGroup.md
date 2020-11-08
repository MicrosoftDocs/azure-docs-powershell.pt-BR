---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111581"
---
# <span data-ttu-id="6cd36-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cd36-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="6cd36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cd36-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd36-103">Cria um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cd36-103">Creates an application security group.</span></span>

## <span data-ttu-id="6cd36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cd36-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cd36-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cd36-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd36-106">O cmdlet **New-AzApplicationSecurityGroup** cria um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cd36-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="6cd36-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cd36-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd36-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6cd36-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="6cd36-109">Este exemplo cria um grupo de segurança de aplicativo sem associações.</span><span class="sxs-lookup"><span data-stu-id="6cd36-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="6cd36-110">Após a criação, as configurações de IP na interface de rede podem ser incluídas no grupo.</span><span class="sxs-lookup"><span data-stu-id="6cd36-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="6cd36-111">As regras de segurança também podem se referir ao grupo como suas origens ou destinos.</span><span class="sxs-lookup"><span data-stu-id="6cd36-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="6cd36-112">OS</span><span class="sxs-lookup"><span data-stu-id="6cd36-112">PARAMETERS</span></span>

### <span data-ttu-id="6cd36-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cd36-113">-AsJob</span></span>
<span data-ttu-id="6cd36-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6cd36-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cd36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd36-115">-DefaultProfile</span></span>
<span data-ttu-id="6cd36-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd36-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd36-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6cd36-117">-Force</span></span>
<span data-ttu-id="6cd36-118">Não peça confirmação se quiser substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="6cd36-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="6cd36-119">-Local</span><span class="sxs-lookup"><span data-stu-id="6cd36-119">-Location</span></span>
<span data-ttu-id="6cd36-120">O local.</span><span class="sxs-lookup"><span data-stu-id="6cd36-120">The location.</span></span>

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

### <span data-ttu-id="6cd36-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cd36-121">-Name</span></span>
<span data-ttu-id="6cd36-122">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cd36-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="6cd36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd36-123">-ResourceGroupName</span></span>
<span data-ttu-id="6cd36-124">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cd36-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="6cd36-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="6cd36-125">-Tag</span></span>
<span data-ttu-id="6cd36-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd36-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6cd36-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cd36-127">-Confirm</span></span>
<span data-ttu-id="6cd36-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cd36-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd36-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd36-129">-WhatIf</span></span>
<span data-ttu-id="6cd36-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cd36-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd36-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cd36-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd36-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd36-132">CommonParameters</span></span>
<span data-ttu-id="6cd36-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd36-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd36-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd36-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd36-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cd36-135">INPUTS</span></span>

### <span data-ttu-id="6cd36-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6cd36-136">System.String</span></span>

### <span data-ttu-id="6cd36-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6cd36-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6cd36-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cd36-138">OUTPUTS</span></span>

### <span data-ttu-id="6cd36-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cd36-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="6cd36-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cd36-140">NOTES</span></span>

## <span data-ttu-id="6cd36-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cd36-141">RELATED LINKS</span></span>

[<span data-ttu-id="6cd36-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cd36-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="6cd36-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cd36-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="6cd36-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd36-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6cd36-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd36-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6cd36-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd36-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6cd36-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cd36-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6cd36-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cd36-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6cd36-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cd36-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
