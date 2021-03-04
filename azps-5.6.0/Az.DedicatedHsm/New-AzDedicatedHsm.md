---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: 9d2d1ee1dd17b9d1783ba267b2f656be6adce05b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887183"
---
# <span data-ttu-id="be8c8-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="be8c8-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="be8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="be8c8-103">Crie ou atualize um HSM dedicado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="be8c8-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="be8c8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be8c8-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="be8c8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="be8c8-106">Crie ou atualize um HSM dedicado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="be8c8-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="be8c8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be8c8-107">EXAMPLES</span></span>

### <span data-ttu-id="be8c8-108">Exemplo 1: Criar um HSM dedicado em uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="be8c8-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="be8c8-109">Este comando cria um HSM dedicado em uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="be8c8-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="be8c8-110">**OBSERVAÇÃO:** Atualmente, `New-AzDedicatedHsm` tem uma limitação que retorna antes que o HSM seja totalmente provisionado no Azure.</span><span class="sxs-lookup"><span data-stu-id="be8c8-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="be8c8-111">Portanto, depois de criar um novo HSM, consulte seu estado e verifique se está antes `Get-AzDedicatedHsm` `Provisioning State` de `Succeeded` usá-lo.</span><span class="sxs-lookup"><span data-stu-id="be8c8-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="be8c8-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be8c8-112">PARAMETERS</span></span>

### <span data-ttu-id="be8c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be8c8-113">-AsJob</span></span>
<span data-ttu-id="be8c8-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="be8c8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="be8c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8c8-115">-DefaultProfile</span></span>
<span data-ttu-id="be8c8-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be8c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-117">-Location</span><span class="sxs-lookup"><span data-stu-id="be8c8-117">-Location</span></span>
<span data-ttu-id="be8c8-118">O local do Azure com suporte onde o HSM dedicado deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="be8c8-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="be8c8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="be8c8-119">-Name</span></span>
<span data-ttu-id="be8c8-120">Nome do Hsm dedicado</span><span class="sxs-lookup"><span data-stu-id="be8c8-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="be8c8-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="be8c8-121">-NetworkInterface</span></span>
<span data-ttu-id="be8c8-122">Especifica a lista de IDs de recursos para as interfaces de rede associadas ao HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="be8c8-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="be8c8-123">Para construir, consulte a seção NOTES para propriedades NETWORKINTERFACE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="be8c8-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be8c8-124">-NoWait</span></span>
<span data-ttu-id="be8c8-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="be8c8-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be8c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be8c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="be8c8-127">O nome do Grupo de Recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="be8c8-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="be8c8-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="be8c8-128">-Sku</span></span>
<span data-ttu-id="be8c8-129">SKU do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="be8c8-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="be8c8-130">-StampId</span></span>
<span data-ttu-id="be8c8-131">Esse campo será usado quando o RP não suportar zonas de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="be8c8-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="be8c8-132">-SubnetId</span></span>
<span data-ttu-id="be8c8-133">A ARM de recurso no formato /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="be8c8-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be8c8-134">-SubscriptionId</span></span>
<span data-ttu-id="be8c8-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be8c8-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="be8c8-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="be8c8-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="be8c8-137">-Tag</span></span>
<span data-ttu-id="be8c8-138">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="be8c8-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="be8c8-139">-Zone</span></span>
<span data-ttu-id="be8c8-140">As zonas Hsm dedicadas.</span><span class="sxs-lookup"><span data-stu-id="be8c8-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be8c8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be8c8-141">-Confirm</span></span>
<span data-ttu-id="be8c8-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be8c8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8c8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8c8-143">-WhatIf</span></span>
<span data-ttu-id="be8c8-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be8c8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be8c8-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be8c8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8c8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8c8-146">CommonParameters</span></span>
<span data-ttu-id="be8c8-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be8c8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8c8-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be8c8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8c8-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be8c8-149">INPUTS</span></span>

## <span data-ttu-id="be8c8-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be8c8-150">OUTPUTS</span></span>

### <span data-ttu-id="be8c8-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="be8c8-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="be8c8-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="be8c8-152">NOTES</span></span>

<span data-ttu-id="be8c8-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="be8c8-153">ALIASES</span></span>

<span data-ttu-id="be8c8-154">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="be8c8-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be8c8-155">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="be8c8-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be8c8-156">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be8c8-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be8c8-157">NETWORKINTERFACE <INetworkInterface[]>: Especifica a lista de IDs de recursos para as interfaces de rede associadas ao HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="be8c8-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="be8c8-158">`[PrivateIPAddress <String>]`: Endereço Ip privado da interface</span><span class="sxs-lookup"><span data-stu-id="be8c8-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="be8c8-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be8c8-159">RELATED LINKS</span></span>

