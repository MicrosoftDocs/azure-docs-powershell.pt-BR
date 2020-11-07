---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: b8ce7dac361124129b3261d8ba368852726812ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771539"
---
# <span data-ttu-id="19900-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="19900-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="19900-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19900-102">SYNOPSIS</span></span>
<span data-ttu-id="19900-103">Remove um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="19900-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="19900-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19900-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19900-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19900-105">DESCRIPTION</span></span>
<span data-ttu-id="19900-106">O cmdlet Remove-AzDdosProtectionPlan remove um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="19900-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="19900-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19900-107">EXAMPLES</span></span>

### <span data-ttu-id="19900-108">Exemplo 1: remover um plano de proteção contra DDoS vazio</span><span class="sxs-lookup"><span data-stu-id="19900-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="19900-109">Nesse caso, removemos um plano de proteção contra DDoS conforme especificado.</span><span class="sxs-lookup"><span data-stu-id="19900-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="19900-110">Exemplo 2: remover um plano de proteção contra DDoS associado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="19900-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
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
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="19900-111">Os planos de proteção contra DDoS não podem ser excluídos se estiverem associados a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19900-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="19900-112">Portanto, a primeira etapa é desassociar os dois objetos.</span><span class="sxs-lookup"><span data-stu-id="19900-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="19900-113">Aqui, obtemos a versão mais atualizada da rede virtual associada ao plano e definimos a propriedade **DdosProtectionPlan** como um valor vazio e o sinalizador **EnableDdosProtection** (esse sinalizador não pode ser verdadeiro sem um plano).</span><span class="sxs-lookup"><span data-stu-id="19900-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="19900-114">Em seguida, persistemos o novo estado canalizando a variável local para **set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="19900-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="19900-115">Neste ponto, o plano não está mais associado à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19900-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="19900-116">Se este for o último associado ao plano, poderemos remover o plano de proteção contra DDoS usando o comando Remove-AzDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="19900-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="19900-117">OS</span><span class="sxs-lookup"><span data-stu-id="19900-117">PARAMETERS</span></span>

### <span data-ttu-id="19900-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19900-118">-DefaultProfile</span></span>
<span data-ttu-id="19900-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19900-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19900-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="19900-120">-Name</span></span>
<span data-ttu-id="19900-121">Especifica o nome do plano de proteção contra DDoS a ser removido.</span><span class="sxs-lookup"><span data-stu-id="19900-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="19900-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19900-122">-PassThru</span></span>
<span data-ttu-id="19900-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="19900-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19900-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="19900-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19900-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19900-125">-ResourceGroupName</span></span>
<span data-ttu-id="19900-126">Especifica o grupo de recursos do plano de proteção contra DDoS a ser removido.</span><span class="sxs-lookup"><span data-stu-id="19900-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="19900-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19900-127">-Confirm</span></span>
<span data-ttu-id="19900-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19900-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19900-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19900-129">-WhatIf</span></span>
<span data-ttu-id="19900-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19900-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19900-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19900-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19900-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19900-132">CommonParameters</span></span>
<span data-ttu-id="19900-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19900-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19900-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19900-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19900-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19900-135">INPUTS</span></span>

### <span data-ttu-id="19900-136">System. String</span><span class="sxs-lookup"><span data-stu-id="19900-136">System.String</span></span>

## <span data-ttu-id="19900-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19900-137">OUTPUTS</span></span>

### <span data-ttu-id="19900-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19900-138">System.Boolean</span></span>

## <span data-ttu-id="19900-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19900-139">NOTES</span></span>

## <span data-ttu-id="19900-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19900-140">RELATED LINKS</span></span>

[<span data-ttu-id="19900-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="19900-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="19900-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="19900-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="19900-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19900-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="19900-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19900-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="19900-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19900-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)