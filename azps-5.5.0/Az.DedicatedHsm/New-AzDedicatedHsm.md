---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116847"
---
# <span data-ttu-id="ac9d8-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="ac9d8-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="ac9d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9d8-103">Criar ou atualizar um HSM dedicado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="ac9d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac9d8-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ac9d8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9d8-106">Criar ou atualizar um HSM dedicado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="ac9d8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac9d8-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9d8-108">Exemplo 1: Criar um HSM Dedicado em uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="ac9d8-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="ac9d8-109">Esse comando cria um HSM Dedicado em uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="ac9d8-110">**OBSERVAÇÃO:** Atualmente, `New-AzDedicatedHsm` ela tem uma limitação que retorna antes que o HSM seja totalmente provisionado no Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="ac9d8-111">Portanto, depois de criar um novo HSM, consulte seu estado e verifique se `Get-AzDedicatedHsm` ele está antes de `Provisioning State` `Succeeded` usá-lo.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="ac9d8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac9d8-112">PARAMETERS</span></span>

### <span data-ttu-id="ac9d8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac9d8-113">-AsJob</span></span>
<span data-ttu-id="ac9d8-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ac9d8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ac9d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9d8-115">-DefaultProfile</span></span>
<span data-ttu-id="ac9d8-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9d8-117">-Local</span><span class="sxs-lookup"><span data-stu-id="ac9d8-117">-Location</span></span>
<span data-ttu-id="ac9d8-118">O local do Azure com suporte onde o HSM dedicado deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="ac9d8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac9d8-119">-Name</span></span>
<span data-ttu-id="ac9d8-120">Nome do Hsm dedicado</span><span class="sxs-lookup"><span data-stu-id="ac9d8-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="ac9d8-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ac9d8-121">-NetworkInterface</span></span>
<span data-ttu-id="ac9d8-122">Especifica a lista de IDs de recursos para as interfaces de rede associadas ao HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="ac9d8-123">Para construir, confira a seção ANOTAÇÕES para propriedades NETWORKINTERFACE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac9d8-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac9d8-124">-NoWait</span></span>
<span data-ttu-id="ac9d8-125">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="ac9d8-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac9d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac9d8-127">O nome do Grupo de Recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="ac9d8-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="ac9d8-128">-Sku</span></span>
<span data-ttu-id="ac9d8-129">SKU do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="ac9d8-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="ac9d8-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="ac9d8-130">-StampId</span></span>
<span data-ttu-id="ac9d8-131">Esse campo será usado quando NÃO FOR NECESSÁRIO dar suporte a zonas de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="ac9d8-132">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="ac9d8-132">-SubnetId</span></span>
<span data-ttu-id="ac9d8-133">A ID do recurso ARM na forma de /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="ac9d8-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="ac9d8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac9d8-134">-SubscriptionId</span></span>
<span data-ttu-id="ac9d8-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac9d8-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ac9d8-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac9d8-137">-Tag</span></span>
<span data-ttu-id="ac9d8-138">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="ac9d8-138">Resource tags</span></span>

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

### <span data-ttu-id="ac9d8-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="ac9d8-139">-Zone</span></span>
<span data-ttu-id="ac9d8-140">As zonas Hsm dedicadas.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="ac9d8-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ac9d8-141">-Confirm</span></span>
<span data-ttu-id="ac9d8-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9d8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9d8-143">-WhatIf</span></span>
<span data-ttu-id="ac9d8-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac9d8-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9d8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9d8-146">CommonParameters</span></span>
<span data-ttu-id="ac9d8-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9d8-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac9d8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9d8-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="ac9d8-149">INPUTS</span></span>

## <span data-ttu-id="ac9d8-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="ac9d8-150">OUTPUTS</span></span>

### <span data-ttu-id="ac9d8-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="ac9d8-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="ac9d8-152">Notas</span><span class="sxs-lookup"><span data-stu-id="ac9d8-152">NOTES</span></span>

<span data-ttu-id="ac9d8-153">Aliases</span><span class="sxs-lookup"><span data-stu-id="ac9d8-153">ALIASES</span></span>

<span data-ttu-id="ac9d8-154">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ac9d8-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac9d8-155">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac9d8-156">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac9d8-157">NETWORKINTERFACE <INetworkInterface[]>: Especifica a lista de IDs de recursos para as interfaces de rede associadas ao HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="ac9d8-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="ac9d8-158">`[PrivateIPAddress <String>]`: Endereço Ip particular da interface</span><span class="sxs-lookup"><span data-stu-id="ac9d8-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="ac9d8-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac9d8-159">RELATED LINKS</span></span>

