---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264440"
---
# <span data-ttu-id="8ed04-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8ed04-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="8ed04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ed04-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed04-103">Cria um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="8ed04-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="8ed04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ed04-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ed04-105">DESCRIPTION</span></span>
<span data-ttu-id="8ed04-106">O cmdlet New-AzDdosProtectionPlan cria um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="8ed04-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="8ed04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ed04-107">EXAMPLES</span></span>

### <span data-ttu-id="8ed04-108">Exemplo 1: criar e associar um plano de proteção contra DDoS com uma nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="8ed04-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="8ed04-109">Primeiro, criamos um novo plano de proteção contra DDoS com o comando **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="8ed04-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="8ed04-110">Em seguida, criamos uma nova rede virtual com **New-AzVirtualNetwork** e especificamos a ID do plano recém-criado no parâmetro **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="8ed04-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="8ed04-111">Nesse caso, como estamos associando a rede virtual a um plano, também podemos especificar o parâmetro **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="8ed04-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="8ed04-112">Exemplo 2: criar e associar um plano de proteção contra DDoS a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="8ed04-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
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

<span data-ttu-id="8ed04-113">Primeiro, criamos um novo plano de proteção contra DDoS com o comando **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="8ed04-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="8ed04-114">Em segundo lugar, obtemos a versão mais atualizada da rede virtual que queremos associar ao plano.</span><span class="sxs-lookup"><span data-stu-id="8ed04-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="8ed04-115">Atualizamos a propriedade **DdosProtectionPlan** com um objeto **PSResourceId** que contém uma referência à ID do plano recém-criado.</span><span class="sxs-lookup"><span data-stu-id="8ed04-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="8ed04-116">Nesse caso, se associarmos a rede virtual a um plano de proteção contra DDoS, também poderemos definir o sinalizador **EnableDdosProtection** como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="8ed04-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="8ed04-117">Por fim, persistemos o novo estado canalizando a variável local para **set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="8ed04-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="8ed04-118">OS</span><span class="sxs-lookup"><span data-stu-id="8ed04-118">PARAMETERS</span></span>

### <span data-ttu-id="8ed04-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ed04-119">-AsJob</span></span>
<span data-ttu-id="8ed04-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8ed04-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ed04-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed04-121">-DefaultProfile</span></span>
<span data-ttu-id="8ed04-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ed04-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed04-123">-Local</span><span class="sxs-lookup"><span data-stu-id="8ed04-123">-Location</span></span>
<span data-ttu-id="8ed04-124">Especifica o local do plano de proteção contra DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8ed04-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="8ed04-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ed04-125">-Name</span></span>
<span data-ttu-id="8ed04-126">Especifica o nome do plano de proteção contra DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8ed04-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="8ed04-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed04-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ed04-128">Especifica o grupo de recursos do plano de proteção contra DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8ed04-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="8ed04-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="8ed04-129">-Tag</span></span>
<span data-ttu-id="8ed04-130">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ed04-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8ed04-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ed04-131">-Confirm</span></span>
<span data-ttu-id="8ed04-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ed04-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed04-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed04-133">-WhatIf</span></span>
<span data-ttu-id="8ed04-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ed04-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ed04-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ed04-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed04-136">CommonParameters</span></span>
<span data-ttu-id="8ed04-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed04-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ed04-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed04-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ed04-139">INPUTS</span></span>

### <span data-ttu-id="8ed04-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8ed04-140">System.String</span></span>

### <span data-ttu-id="8ed04-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ed04-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8ed04-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ed04-142">OUTPUTS</span></span>

### <span data-ttu-id="8ed04-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8ed04-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="8ed04-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ed04-144">NOTES</span></span>

## <span data-ttu-id="8ed04-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ed04-145">RELATED LINKS</span></span>

[<span data-ttu-id="8ed04-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8ed04-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="8ed04-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="8ed04-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="8ed04-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ed04-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="8ed04-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ed04-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="8ed04-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ed04-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)