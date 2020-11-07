---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945303"
---
# <span data-ttu-id="d64da-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="d64da-101">New-AzsIPPool</span></span>

## <span data-ttu-id="d64da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d64da-102">SYNOPSIS</span></span>
<span data-ttu-id="d64da-103">Crie um pool de IP.</span><span class="sxs-lookup"><span data-stu-id="d64da-103">Create an IP pool.</span></span>
<span data-ttu-id="d64da-104">Após a criação de um pool de IPs não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d64da-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="d64da-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d64da-105">SYNTAX</span></span>

### <span data-ttu-id="d64da-106">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="d64da-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d64da-107">Criados</span><span class="sxs-lookup"><span data-stu-id="d64da-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d64da-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d64da-108">DESCRIPTION</span></span>
<span data-ttu-id="d64da-109">Crie um pool de IP.</span><span class="sxs-lookup"><span data-stu-id="d64da-109">Create an IP pool.</span></span>
<span data-ttu-id="d64da-110">Após a criação de um pool de IPs não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d64da-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="d64da-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d64da-111">EXAMPLES</span></span>

### <span data-ttu-id="d64da-112">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="d64da-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="d64da-113">Crie um novo pool de IP.</span><span class="sxs-lookup"><span data-stu-id="d64da-113">Create a new IP pool.</span></span>



## <span data-ttu-id="d64da-114">OS</span><span class="sxs-lookup"><span data-stu-id="d64da-114">PARAMETERS</span></span>

### <span data-ttu-id="d64da-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d64da-115">-AddressPrefix</span></span>
<span data-ttu-id="d64da-116">O prefixo do endereço.</span><span class="sxs-lookup"><span data-stu-id="d64da-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d64da-117">-AsJob</span></span>
<span data-ttu-id="d64da-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d64da-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d64da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64da-119">-DefaultProfile</span></span>
<span data-ttu-id="d64da-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d64da-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d64da-121">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="d64da-121">-EndIPAddress</span></span>
<span data-ttu-id="d64da-122">O endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="d64da-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-123">-Local</span><span class="sxs-lookup"><span data-stu-id="d64da-123">-Location</span></span>
<span data-ttu-id="d64da-124">A região em que o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="d64da-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d64da-125">-Name</span></span>
<span data-ttu-id="d64da-126">Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="d64da-126">IP pool name.</span></span>

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

### <span data-ttu-id="d64da-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d64da-127">-NoWait</span></span>
<span data-ttu-id="d64da-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d64da-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d64da-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="d64da-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="d64da-130">O número de endereços IP atualmente alocados.</span><span class="sxs-lookup"><span data-stu-id="d64da-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="d64da-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="d64da-132">O número total de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="d64da-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="d64da-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="d64da-134">O número atual de endereços IP na transição.</span><span class="sxs-lookup"><span data-stu-id="d64da-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-135">-Pool</span><span class="sxs-lookup"><span data-stu-id="d64da-135">-Pool</span></span>
<span data-ttu-id="d64da-136">Esse recurso define o intervalo de endereços IP dos quais os endereços são alocados para nós dentro de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d64da-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="d64da-137">Para construir, consulte a seção de anotações para propriedades do POOL e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d64da-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64da-138">-ResourceGroupName</span></span>
<span data-ttu-id="d64da-139">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d64da-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d64da-140">-StartIPAddress</span></span>
<span data-ttu-id="d64da-141">O endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="d64da-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d64da-142">-SubscriptionId</span></span>
<span data-ttu-id="d64da-143">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d64da-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d64da-144">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d64da-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d64da-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="d64da-145">-Tag</span></span>
<span data-ttu-id="d64da-146">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="d64da-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d64da-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d64da-147">-Confirm</span></span>
<span data-ttu-id="d64da-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64da-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64da-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64da-149">-WhatIf</span></span>
<span data-ttu-id="d64da-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d64da-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d64da-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d64da-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64da-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64da-152">CommonParameters</span></span>
<span data-ttu-id="d64da-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64da-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64da-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d64da-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64da-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d64da-155">INPUTS</span></span>

### <span data-ttu-id="d64da-156">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="d64da-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="d64da-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d64da-157">OUTPUTS</span></span>

### <span data-ttu-id="d64da-158">Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="d64da-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="d64da-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d64da-159">NOTES</span></span>

<span data-ttu-id="d64da-160">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d64da-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d64da-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d64da-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d64da-162">POOL <IIPPool> : esse recurso define o intervalo de endereços IP dos quais os endereços são alocados para nós dentro de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d64da-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="d64da-163">`[Location <String>]`: A região onde o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="d64da-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="d64da-164">`[Tag <IResourceTags>]`: Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="d64da-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="d64da-165">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="d64da-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d64da-166">`[AddressPrefix <String>]`: O prefixo do endereço.</span><span class="sxs-lookup"><span data-stu-id="d64da-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="d64da-167">`[EndIPAddress <String>]`: O endereço IP final.</span><span class="sxs-lookup"><span data-stu-id="d64da-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="d64da-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: O número de endereços IP atualmente alocados.</span><span class="sxs-lookup"><span data-stu-id="d64da-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="d64da-169">`[NumberOfIPAddresses <Int64?>]`: O número total de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="d64da-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="d64da-170">`[NumberOfIPAddressesInTransition <Int64?>]`: O número atual de endereços IP na transição.</span><span class="sxs-lookup"><span data-stu-id="d64da-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="d64da-171">`[StartIPAddress <String>]`: O endereço IP inicial.</span><span class="sxs-lookup"><span data-stu-id="d64da-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="d64da-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d64da-172">RELATED LINKS</span></span>

