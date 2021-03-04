---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 0a8386a4ed91fa6e35adafbdc8ec532bb781f75e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886207"
---
# <span data-ttu-id="e72ac-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e72ac-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="e72ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e72ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e72ac-103">Cria um plano de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="e72ac-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="e72ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e72ac-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72ac-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e72ac-105">DESCRIPTION</span></span>
<span data-ttu-id="e72ac-106">O New-AzDdosProtectionPlan cmdlet cria um plano de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="e72ac-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="e72ac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e72ac-107">EXAMPLES</span></span>

### <span data-ttu-id="e72ac-108">Exemplo 1: Criar e associar um plano de proteção DDoS a uma nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="e72ac-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="e72ac-109">Primeiro, criamos um novo plano de Proteção DDoS com o **comando New-AzDdosProtectionPlan.**</span><span class="sxs-lookup"><span data-stu-id="e72ac-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="e72ac-110">Em seguida, criamos uma nova rede virtual com **New-AzVirtualNetwork** e especificamos a ID do plano recém-criado no parâmetro **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="e72ac-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="e72ac-111">Nesse caso, como estamos associando a rede virtual a um plano, também podemos especificar o parâmetro **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="e72ac-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="e72ac-112">Exemplo 2: Criar e associar um plano de proteção DDoS a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="e72ac-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="e72ac-113">Primeiro, criamos um novo plano de Proteção DDoS com o **comando New-AzDdosProtectionPlan.**</span><span class="sxs-lookup"><span data-stu-id="e72ac-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="e72ac-114">Em segundo lugar, temos a versão mais atualizada da rede virtual que queremos associar ao plano.</span><span class="sxs-lookup"><span data-stu-id="e72ac-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="e72ac-115">Atualizamos a **propriedade DdosProtectionPlan** com um **objeto PSResourceId** que contém uma referência à ID do plano recém-criado.</span><span class="sxs-lookup"><span data-stu-id="e72ac-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="e72ac-116">Nesse caso, se associarmos a rede virtual a um plano de proteção DDoS, também podemos definir o sinalizador **EnableDdosProtection** como true.</span><span class="sxs-lookup"><span data-stu-id="e72ac-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="e72ac-117">Por fim, persistimos o novo estado canalização da variável local para **Set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="e72ac-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="e72ac-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e72ac-118">PARAMETERS</span></span>

### <span data-ttu-id="e72ac-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e72ac-119">-AsJob</span></span>
<span data-ttu-id="e72ac-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e72ac-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e72ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72ac-121">-DefaultProfile</span></span>
<span data-ttu-id="e72ac-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e72ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e72ac-123">-Location</span><span class="sxs-lookup"><span data-stu-id="e72ac-123">-Location</span></span>
<span data-ttu-id="e72ac-124">Especifica o local do plano de proteção DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e72ac-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="e72ac-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e72ac-125">-Name</span></span>
<span data-ttu-id="e72ac-126">Especifica o nome do plano de proteção DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e72ac-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="e72ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="e72ac-128">Especifica o grupo de recursos do plano de proteção DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e72ac-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="e72ac-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e72ac-129">-Tag</span></span>
<span data-ttu-id="e72ac-130">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e72ac-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e72ac-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e72ac-131">-Confirm</span></span>
<span data-ttu-id="e72ac-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72ac-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72ac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72ac-133">-WhatIf</span></span>
<span data-ttu-id="e72ac-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e72ac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e72ac-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e72ac-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72ac-136">CommonParameters</span></span>
<span data-ttu-id="e72ac-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72ac-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72ac-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72ac-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e72ac-139">INPUTS</span></span>

### <span data-ttu-id="e72ac-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e72ac-140">System.String</span></span>

### <span data-ttu-id="e72ac-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e72ac-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e72ac-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e72ac-142">OUTPUTS</span></span>

### <span data-ttu-id="e72ac-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e72ac-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="e72ac-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="e72ac-144">NOTES</span></span>

## <span data-ttu-id="e72ac-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e72ac-145">RELATED LINKS</span></span>

[<span data-ttu-id="e72ac-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e72ac-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="e72ac-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e72ac-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="e72ac-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e72ac-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="e72ac-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e72ac-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="e72ac-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e72ac-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)