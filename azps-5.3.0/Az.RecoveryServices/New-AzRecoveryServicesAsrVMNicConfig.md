---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428805"
---
# <span data-ttu-id="07ac0-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="07ac0-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="07ac0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="07ac0-103">Cria uma configuração de NIC ASR que contém os detalhes de configuração relacionados ao failover e teste de failover.</span><span class="sxs-lookup"><span data-stu-id="07ac0-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="07ac0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07ac0-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07ac0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07ac0-105">DESCRIPTION</span></span>
<span data-ttu-id="07ac0-106">O cmdlet **New-AzRecoveryServicesAsrVMNicConfig** cria um objeto de configuração de NIC ASR que contém os detalhes relacionados ao failover e teste de failover.</span><span class="sxs-lookup"><span data-stu-id="07ac0-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="07ac0-107">Caso qualquer informação não seja passada, os valores correspondentes são separados do item de replicação protegida para evitar que esses valores sejam atualizados para NULL.</span><span class="sxs-lookup"><span data-stu-id="07ac0-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="07ac0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07ac0-108">EXAMPLES</span></span>

### <span data-ttu-id="07ac0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07ac0-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="07ac0-110">Cria um objeto ASRVmNicConfig com as configurações de rede de failover e teste faiover configuradas para a NIC.</span><span class="sxs-lookup"><span data-stu-id="07ac0-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="07ac0-111">Qualquer propriedade que não seja passada acima é buscada do item protegido passado.</span><span class="sxs-lookup"><span data-stu-id="07ac0-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="07ac0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07ac0-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="07ac0-113">Cria um objeto ASRVmNicConfig com as configurações de rede faiover de teste configuradas para a renomeação da NIC.</span><span class="sxs-lookup"><span data-stu-id="07ac0-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="07ac0-114">Qualquer propriedade que não seja passada acima é buscada do item protegido passado.</span><span class="sxs-lookup"><span data-stu-id="07ac0-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="07ac0-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="07ac0-115">Example 3</span></span>

<span data-ttu-id="07ac0-116">Cria uma configuração de NIC ASR que contém os detalhes de configuração relacionados ao failover e teste de failover.</span><span class="sxs-lookup"><span data-stu-id="07ac0-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="07ac0-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="07ac0-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="07ac0-118">OS</span><span class="sxs-lookup"><span data-stu-id="07ac0-118">PARAMETERS</span></span>

### <span data-ttu-id="07ac0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ac0-119">-DefaultProfile</span></span>
<span data-ttu-id="07ac0-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07ac0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ac0-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="07ac0-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="07ac0-122">Especifica se a rede acelerada está habilitada na NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="07ac0-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="07ac0-124">Especifica se a rede acelerada está habilitada na NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="07ac0-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="07ac0-125">-NicId</span></span>
<span data-ttu-id="07ac0-126">Especifique o GUID da NIC ASR.</span><span class="sxs-lookup"><span data-stu-id="07ac0-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="07ac0-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="07ac0-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="07ac0-128">Especifica as IDs dos pools de endereços back-end para a NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="07ac0-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="07ac0-130">Especifica a ID do NSG associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="07ac0-131">-RecoveryNicName</span></span>
<span data-ttu-id="07ac0-132">Especifica o nome da NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ac0-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="07ac0-134">Especifica o nome do grupo de recursos da NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="07ac0-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="07ac0-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="07ac0-136">Especifica o endereço IP da NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="07ac0-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="07ac0-138">Especifica a ID do endereço IP público associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="07ac0-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="07ac0-140">Especifica a ID da rede virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="07ac0-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="07ac0-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="07ac0-142">Especifica o nome da sub-rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="07ac0-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07ac0-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="07ac0-144">Especifique o item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="07ac0-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ac0-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="07ac0-145">-ReuseExistingNic</span></span>
<span data-ttu-id="07ac0-146">Especifica se uma NIC existente pode ser usada durante o failover.</span><span class="sxs-lookup"><span data-stu-id="07ac0-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="07ac0-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="07ac0-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="07ac0-148">Especifica as IDs dos pools de endereços back-end para a NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07ac0-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="07ac0-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="07ac0-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="07ac0-150">Especifica a ID do NSG associado à NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="07ac0-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="07ac0-151">-TfoNicName</span></span>
<span data-ttu-id="07ac0-152">Especifica o nome da NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="07ac0-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ac0-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="07ac0-154">Especifica o nome do grupo de recursos NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="07ac0-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="07ac0-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="07ac0-156">Especifica o endereço IP da NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="07ac0-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="07ac0-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="07ac0-158">Especifica a ID do endereço IP público associado à NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="07ac0-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="07ac0-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="07ac0-160">Especifica se uma NIC existente pode ser usada durante o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="07ac0-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="07ac0-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="07ac0-162">Especifica a ID da rede virtual de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="07ac0-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="07ac0-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="07ac0-164">Especifica o nome da sub-rede de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="07ac0-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="07ac0-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07ac0-165">-Confirm</span></span>
<span data-ttu-id="07ac0-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07ac0-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ac0-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ac0-167">-WhatIf</span></span>
<span data-ttu-id="07ac0-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07ac0-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07ac0-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07ac0-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ac0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ac0-170">CommonParameters</span></span>
<span data-ttu-id="07ac0-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ac0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ac0-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07ac0-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ac0-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07ac0-173">INPUTS</span></span>

### <span data-ttu-id="07ac0-174">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="07ac0-174">None</span></span>

## <span data-ttu-id="07ac0-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07ac0-175">OUTPUTS</span></span>

### <span data-ttu-id="07ac0-176">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="07ac0-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="07ac0-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07ac0-177">NOTES</span></span>

## <span data-ttu-id="07ac0-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07ac0-178">RELATED LINKS</span></span>
