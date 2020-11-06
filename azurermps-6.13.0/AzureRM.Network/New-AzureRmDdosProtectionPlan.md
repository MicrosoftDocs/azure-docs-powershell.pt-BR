---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 79a9f0cb2b46150c7746112553949b1bbcbaf1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429471"
---
# <span data-ttu-id="d7bff-101">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7bff-101">New-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="d7bff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7bff-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bff-103">Cria um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="d7bff-103">Creates a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7bff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7bff-104">SYNTAX</span></span>

```
New-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7bff-105">DESCRIPTION</span></span>
<span data-ttu-id="d7bff-106">O cmdlet New-AzureRmDdosProtectionPlan cria um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="d7bff-106">The New-AzureRmDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="d7bff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7bff-107">EXAMPLES</span></span>

### <span data-ttu-id="d7bff-108">Exemplo 1: criar e associar um plano de proteção contra DDoS com uma nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="d7bff-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzureRmVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzureRmvirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="d7bff-109">Primeiro, criamos um novo plano de proteção contra DDoS com o comando **New-AzureRmDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="d7bff-109">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="d7bff-110">Em seguida, criamos uma nova rede virtual com **New-AzureRmvirtualNetwork** e especificamos a ID do plano recém-criado no parâmetro **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="d7bff-110">Then, we create a new virtual network with **New-AzureRmvirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="d7bff-111">Nesse caso, como estamos associando a rede virtual a um plano, também podemos especificar o parâmetro **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="d7bff-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="d7bff-112">Exemplo 2: criar e associar um plano de proteção contra DDoS a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="d7bff-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzureRmVirtualNetwork


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

<span data-ttu-id="d7bff-113">Primeiro, criamos um novo plano de proteção contra DDoS com o comando **New-AzureRmDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="d7bff-113">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="d7bff-114">Em segundo lugar, obtemos a versão mais atualizada da rede virtual que queremos associar ao plano.</span><span class="sxs-lookup"><span data-stu-id="d7bff-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="d7bff-115">Atualizamos a propriedade **DdosProtectionPlan** com um objeto **PSResourceId** que contém uma referência à ID do plano recém-criado.</span><span class="sxs-lookup"><span data-stu-id="d7bff-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="d7bff-116">Nesse caso, se associarmos a rede virtual a um plano de proteção contra DDoS, também poderemos definir o sinalizador **EnableDdosProtection** como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="d7bff-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="d7bff-117">Por fim, persistemos o novo estado canalizando a variável local para **set-AzureRmVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="d7bff-117">Finally, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span>

## <span data-ttu-id="d7bff-118">OS</span><span class="sxs-lookup"><span data-stu-id="d7bff-118">PARAMETERS</span></span>

### <span data-ttu-id="d7bff-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7bff-119">-AsJob</span></span>
<span data-ttu-id="d7bff-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7bff-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7bff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bff-121">-DefaultProfile</span></span>
<span data-ttu-id="d7bff-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7bff-123">-Local</span><span class="sxs-lookup"><span data-stu-id="d7bff-123">-Location</span></span>
<span data-ttu-id="d7bff-124">Especifica o local do plano de proteção contra DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d7bff-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="d7bff-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7bff-125">-Name</span></span>
<span data-ttu-id="d7bff-126">Especifica o nome do plano de proteção contra DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d7bff-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="d7bff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bff-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7bff-128">Especifica o grupo de recursos do plano de proteção contra DDoS a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d7bff-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="d7bff-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="d7bff-129">-Tag</span></span>
<span data-ttu-id="d7bff-130">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7bff-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d7bff-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7bff-131">-Confirm</span></span>
<span data-ttu-id="d7bff-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7bff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bff-133">-WhatIf</span></span>
<span data-ttu-id="d7bff-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7bff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7bff-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7bff-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bff-136">CommonParameters</span></span>
<span data-ttu-id="d7bff-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bff-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bff-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7bff-139">INPUTS</span></span>

### <span data-ttu-id="d7bff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d7bff-140">System.String</span></span>

### <span data-ttu-id="d7bff-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d7bff-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d7bff-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7bff-142">OUTPUTS</span></span>

### <span data-ttu-id="d7bff-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7bff-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="d7bff-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7bff-144">NOTES</span></span>

## <span data-ttu-id="d7bff-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7bff-145">RELATED LINKS</span></span>

[<span data-ttu-id="d7bff-146">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7bff-146">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="d7bff-147">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7bff-147">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="d7bff-148">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7bff-148">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="d7bff-149">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7bff-149">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="d7bff-150">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7bff-150">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
