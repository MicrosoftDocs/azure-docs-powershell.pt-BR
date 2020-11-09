---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280644"
---
# <span data-ttu-id="aeff3-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="aeff3-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="aeff3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aeff3-102">SYNOPSIS</span></span>
<span data-ttu-id="aeff3-103">Criar ou atualizar um HSM exclusivo na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="aeff3-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="aeff3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aeff3-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="aeff3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aeff3-105">DESCRIPTION</span></span>
<span data-ttu-id="aeff3-106">Criar ou atualizar um HSM exclusivo na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="aeff3-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="aeff3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aeff3-107">EXAMPLES</span></span>

### <span data-ttu-id="aeff3-108">Exemplo 1: criar um HSM dedicado para uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="aeff3-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="aeff3-109">Esse comando cria um HSM dedicado para uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="aeff3-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="aeff3-110">**Observação:** Atualmente `New-AzDedicatedHsm` tem uma limitação que ele retorna antes que o HSM seja totalmente provisionado no Azure.</span><span class="sxs-lookup"><span data-stu-id="aeff3-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="aeff3-111">Portanto, após a criação de um novo HSM, consulte o estado dele `Get-AzDedicatedHsm` e certifique-se de que `Provisioning State` esteja `Succeeded` antes de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="aeff3-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="aeff3-112">OS</span><span class="sxs-lookup"><span data-stu-id="aeff3-112">PARAMETERS</span></span>

### <span data-ttu-id="aeff3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aeff3-113">-AsJob</span></span>
<span data-ttu-id="aeff3-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="aeff3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="aeff3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeff3-115">-DefaultProfile</span></span>
<span data-ttu-id="aeff3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aeff3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeff3-117">-Local</span><span class="sxs-lookup"><span data-stu-id="aeff3-117">-Location</span></span>
<span data-ttu-id="aeff3-118">O local do Azure com suporte no qual o HSM dedicado deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="aeff3-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="aeff3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="aeff3-119">-Name</span></span>
<span data-ttu-id="aeff3-120">Nome do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="aeff3-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="aeff3-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aeff3-121">-NetworkInterface</span></span>
<span data-ttu-id="aeff3-122">Especifica a lista de IDs de recursos para as interfaces de rede associadas ao HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="aeff3-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="aeff3-123">Para construir, consulte a seção de notas para as propriedades NETWORKINTERFACE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aeff3-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="aeff3-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aeff3-124">-NoWait</span></span>
<span data-ttu-id="aeff3-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="aeff3-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aeff3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeff3-126">-ResourceGroupName</span></span>
<span data-ttu-id="aeff3-127">O nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="aeff3-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="aeff3-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="aeff3-128">-Sku</span></span>
<span data-ttu-id="aeff3-129">SKU do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="aeff3-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="aeff3-130">-Stampid</span><span class="sxs-lookup"><span data-stu-id="aeff3-130">-StampId</span></span>
<span data-ttu-id="aeff3-131">Este campo será usado quando o RP não oferecer suporte a zonas de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="aeff3-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="aeff3-132">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="aeff3-132">-SubnetId</span></span>
<span data-ttu-id="aeff3-133">A ID do recurso ARM na forma de/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="aeff3-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="aeff3-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aeff3-134">-SubscriptionId</span></span>
<span data-ttu-id="aeff3-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aeff3-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aeff3-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aeff3-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aeff3-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="aeff3-137">-Tag</span></span>
<span data-ttu-id="aeff3-138">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="aeff3-138">Resource tags</span></span>

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

### <span data-ttu-id="aeff3-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="aeff3-139">-Zone</span></span>
<span data-ttu-id="aeff3-140">As zonas do HSM dedicada.</span><span class="sxs-lookup"><span data-stu-id="aeff3-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="aeff3-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aeff3-141">-Confirm</span></span>
<span data-ttu-id="aeff3-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeff3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeff3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeff3-143">-WhatIf</span></span>
<span data-ttu-id="aeff3-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aeff3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeff3-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aeff3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeff3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeff3-146">CommonParameters</span></span>
<span data-ttu-id="aeff3-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeff3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeff3-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aeff3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeff3-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aeff3-149">INPUTS</span></span>

## <span data-ttu-id="aeff3-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aeff3-150">OUTPUTS</span></span>

### <span data-ttu-id="aeff3-151">Microsoft. Azure. PowerShell. cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="aeff3-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="aeff3-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aeff3-152">NOTES</span></span>

<span data-ttu-id="aeff3-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aeff3-153">ALIASES</span></span>

<span data-ttu-id="aeff3-154">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="aeff3-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aeff3-155">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="aeff3-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aeff3-156">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aeff3-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aeff3-157">NETWORKINTERFACE <INetworkInterface [] >: especifica a lista de IDs de recursos para as interfaces de rede associadas ao HSM dedicado.</span><span class="sxs-lookup"><span data-stu-id="aeff3-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="aeff3-158">`[PrivateIPAddress <String>]`: Endereço IP privado da interface</span><span class="sxs-lookup"><span data-stu-id="aeff3-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="aeff3-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aeff3-159">RELATED LINKS</span></span>

