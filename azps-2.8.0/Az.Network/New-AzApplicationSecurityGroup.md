---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0bccee6b8242e3480ad405837f9c2a661eb97431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771904"
---
# <span data-ttu-id="b1873-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1873-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b1873-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1873-102">SYNOPSIS</span></span>
<span data-ttu-id="b1873-103">Cria um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1873-103">Creates an application security group.</span></span>

## <span data-ttu-id="b1873-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1873-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1873-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1873-105">DESCRIPTION</span></span>
<span data-ttu-id="b1873-106">O cmdlet **New-AzApplicationSecurityGroup** cria um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1873-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="b1873-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1873-107">EXAMPLES</span></span>

### <span data-ttu-id="b1873-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1873-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="b1873-109">Este exemplo cria um grupo de segurança de aplicativo sem associações.</span><span class="sxs-lookup"><span data-stu-id="b1873-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="b1873-110">Após a criação, as configurações de IP na interface de rede podem ser incluídas no grupo.</span><span class="sxs-lookup"><span data-stu-id="b1873-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="b1873-111">As regras de segurança também podem se referir ao grupo como suas origens ou destinos.</span><span class="sxs-lookup"><span data-stu-id="b1873-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="b1873-112">OS</span><span class="sxs-lookup"><span data-stu-id="b1873-112">PARAMETERS</span></span>

### <span data-ttu-id="b1873-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1873-113">-AsJob</span></span>
<span data-ttu-id="b1873-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b1873-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1873-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1873-115">-DefaultProfile</span></span>
<span data-ttu-id="b1873-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1873-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1873-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b1873-117">-Force</span></span>
<span data-ttu-id="b1873-118">Não peça confirmação se quiser substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="b1873-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="b1873-119">-Local</span><span class="sxs-lookup"><span data-stu-id="b1873-119">-Location</span></span>
<span data-ttu-id="b1873-120">O local.</span><span class="sxs-lookup"><span data-stu-id="b1873-120">The location.</span></span>

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

### <span data-ttu-id="b1873-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1873-121">-Name</span></span>
<span data-ttu-id="b1873-122">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1873-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="b1873-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1873-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1873-124">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1873-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b1873-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="b1873-125">-Tag</span></span>
<span data-ttu-id="b1873-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1873-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b1873-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1873-127">-Confirm</span></span>
<span data-ttu-id="b1873-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1873-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1873-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1873-129">-WhatIf</span></span>
<span data-ttu-id="b1873-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1873-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1873-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1873-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1873-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1873-132">CommonParameters</span></span>
<span data-ttu-id="b1873-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1873-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1873-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1873-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1873-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1873-135">INPUTS</span></span>

### <span data-ttu-id="b1873-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b1873-136">System.String</span></span>

### <span data-ttu-id="b1873-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1873-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b1873-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1873-138">OUTPUTS</span></span>

### <span data-ttu-id="b1873-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1873-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="b1873-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1873-140">NOTES</span></span>

## <span data-ttu-id="b1873-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1873-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1873-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1873-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b1873-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1873-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b1873-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1873-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b1873-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1873-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b1873-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1873-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b1873-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1873-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b1873-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1873-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b1873-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1873-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)