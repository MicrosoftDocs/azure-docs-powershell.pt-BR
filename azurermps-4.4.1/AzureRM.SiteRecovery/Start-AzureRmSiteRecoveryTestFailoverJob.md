---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440166"
---
# <span data-ttu-id="0cf90-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0cf90-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="0cf90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cf90-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf90-103">Inicia um failover de teste para uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0cf90-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cf90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cf90-104">SYNTAX</span></span>

### <span data-ttu-id="0cf90-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="0cf90-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0cf90-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0cf90-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0cf90-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0cf90-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0cf90-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="0cf90-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0cf90-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf90-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0cf90-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf90-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cf90-114">DESCRIPTION</span></span>
<span data-ttu-id="0cf90-115">O cmdlet **Start-AzureRmSiteRecoveryTestFailoverJob** inicia o failover de teste de uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0cf90-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="0cf90-116">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="0cf90-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="0cf90-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cf90-117">EXAMPLES</span></span>

## <span data-ttu-id="0cf90-118">OS</span><span class="sxs-lookup"><span data-stu-id="0cf90-118">PARAMETERS</span></span>

### <span data-ttu-id="0cf90-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0cf90-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="0cf90-120">Especifica a ID de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf90-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf90-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0cf90-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0cf90-122">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="0cf90-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="0cf90-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0cf90-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0cf90-124">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="0cf90-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="0cf90-125">-Direction</span><span class="sxs-lookup"><span data-stu-id="0cf90-125">-Direction</span></span>
<span data-ttu-id="0cf90-126">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="0cf90-126">Specifies the failover direction.</span></span>
<span data-ttu-id="0cf90-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0cf90-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cf90-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0cf90-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="0cf90-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0cf90-129">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf90-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0cf90-130">-ProtectionEntity</span></span>
<span data-ttu-id="0cf90-131">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="0cf90-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf90-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0cf90-132">-RecoveryPlan</span></span>
<span data-ttu-id="0cf90-133">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0cf90-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf90-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf90-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf90-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="0cf90-135">-VMNetwork</span></span>
<span data-ttu-id="0cf90-136">Especifica a rede de máquina virtual de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="0cf90-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf90-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf90-137">-DefaultProfile</span></span>
<span data-ttu-id="0cf90-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf90-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf90-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf90-139">CommonParameters</span></span>
<span data-ttu-id="0cf90-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf90-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf90-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf90-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf90-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cf90-142">INPUTS</span></span>

### <span data-ttu-id="0cf90-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0cf90-143">ASRProtectionEntity</span></span>
<span data-ttu-id="0cf90-144">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0cf90-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="0cf90-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0cf90-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="0cf90-146">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0cf90-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="0cf90-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf90-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="0cf90-148">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0cf90-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="0cf90-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cf90-149">OUTPUTS</span></span>

### <span data-ttu-id="0cf90-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0cf90-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0cf90-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cf90-151">NOTES</span></span>

## <span data-ttu-id="0cf90-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cf90-152">RELATED LINKS</span></span>

[<span data-ttu-id="0cf90-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0cf90-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
