---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942686"
---
# <span data-ttu-id="deb62-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="deb62-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="deb62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deb62-102">SYNOPSIS</span></span>
<span data-ttu-id="deb62-103">Cria uma configuração de NIC ASR que contém os detalhes de configuração relacionados ao failover e teste de failover.</span><span class="sxs-lookup"><span data-stu-id="deb62-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="deb62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deb62-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deb62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deb62-105">DESCRIPTION</span></span>
<span data-ttu-id="deb62-106">O cmdlet **New-AzRecoveryServicesAsrVMNicConfig** cria um objeto de configuração de NIC ASR que contém os detalhes relacionados ao failover e teste de failover.</span><span class="sxs-lookup"><span data-stu-id="deb62-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="deb62-107">Caso qualquer informação não seja passada, os valores correspondentes são separados do item de replicação protegida para evitar que esses valores sejam atualizados para NULL.</span><span class="sxs-lookup"><span data-stu-id="deb62-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="deb62-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deb62-108">EXAMPLES</span></span>

### <span data-ttu-id="deb62-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="deb62-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="deb62-110">Cria um objeto ASRVmNicConfig com as configurações de rede de failover e teste faiover configuradas para a NIC.</span><span class="sxs-lookup"><span data-stu-id="deb62-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="deb62-111">Qualquer propriedade que não seja passada acima é buscada do item protegido passado.</span><span class="sxs-lookup"><span data-stu-id="deb62-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="deb62-112">OS</span><span class="sxs-lookup"><span data-stu-id="deb62-112">PARAMETERS</span></span>

### <span data-ttu-id="deb62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb62-113">-DefaultProfile</span></span>
<span data-ttu-id="deb62-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deb62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb62-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="deb62-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="deb62-116">Especifica se a rede acelerada está habilitada na NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="deb62-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="deb62-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="deb62-118">Especifica se a rede acelerada está habilitada na NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="deb62-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="deb62-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="deb62-119">-NicId</span></span>
<span data-ttu-id="deb62-120">Especifique o GUID da NIC ASR.</span><span class="sxs-lookup"><span data-stu-id="deb62-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="deb62-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="deb62-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="deb62-122">Especifica as IDs dos pools de endereços back-end para a NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="deb62-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="deb62-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="deb62-124">Especifica a ID do NSG associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="deb62-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="deb62-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="deb62-126">Especifica o endereço IP da NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="deb62-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="deb62-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="deb62-128">Especifica a ID do endereço IP público associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="deb62-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="deb62-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="deb62-130">Especifica a ID da rede virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="deb62-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="deb62-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="deb62-132">Especifica o nome da sub-rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="deb62-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="deb62-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="deb62-134">Especifique o item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="deb62-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="deb62-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="deb62-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="deb62-136">Especifica as IDs dos pools de endereços back-end para a NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="deb62-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="deb62-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="deb62-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="deb62-138">Especifica a ID do NSG associado à NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="deb62-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="deb62-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="deb62-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="deb62-140">Especifica o endereço IP da NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="deb62-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="deb62-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="deb62-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="deb62-142">Especifica a ID do endereço IP público associado à NIC de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="deb62-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="deb62-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="deb62-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="deb62-144">Especifica a ID da rede virtual de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="deb62-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="deb62-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="deb62-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="deb62-146">Especifica o nome da sub-rede de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="deb62-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="deb62-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb62-147">CommonParameters</span></span>
<span data-ttu-id="deb62-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb62-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb62-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deb62-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb62-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deb62-150">INPUTS</span></span>

### <span data-ttu-id="deb62-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="deb62-151">None</span></span>

## <span data-ttu-id="deb62-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deb62-152">OUTPUTS</span></span>

### <span data-ttu-id="deb62-153">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="deb62-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="deb62-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deb62-154">NOTES</span></span>

## <span data-ttu-id="deb62-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deb62-155">RELATED LINKS</span></span>
