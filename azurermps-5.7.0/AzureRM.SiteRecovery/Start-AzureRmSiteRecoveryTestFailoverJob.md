---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427423"
---
# <span data-ttu-id="572bb-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="572bb-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="572bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="572bb-102">SYNOPSIS</span></span>
<span data-ttu-id="572bb-103">Inicia um failover de teste para uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="572bb-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="572bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="572bb-104">SYNTAX</span></span>

### <span data-ttu-id="572bb-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="572bb-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="572bb-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="572bb-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="572bb-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="572bb-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="572bb-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="572bb-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="572bb-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572bb-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="572bb-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="572bb-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="572bb-114">DESCRIPTION</span></span>
<span data-ttu-id="572bb-115">O cmdlet **Start-AzureRmSiteRecoveryTestFailoverJob** inicia o failover de teste de uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="572bb-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="572bb-116">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="572bb-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="572bb-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="572bb-117">EXAMPLES</span></span>

## <span data-ttu-id="572bb-118">OS</span><span class="sxs-lookup"><span data-stu-id="572bb-118">PARAMETERS</span></span>

### <span data-ttu-id="572bb-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="572bb-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="572bb-120">Especifica a ID de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="572bb-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="572bb-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="572bb-122">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="572bb-122">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="572bb-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="572bb-124">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="572bb-124">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572bb-125">-DefaultProfile</span></span>
<span data-ttu-id="572bb-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="572bb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-127">-Direction</span><span class="sxs-lookup"><span data-stu-id="572bb-127">-Direction</span></span>
<span data-ttu-id="572bb-128">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="572bb-128">Specifies the failover direction.</span></span>
<span data-ttu-id="572bb-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="572bb-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="572bb-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="572bb-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="572bb-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="572bb-131">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="572bb-132">-ProtectionEntity</span></span>
<span data-ttu-id="572bb-133">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="572bb-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="572bb-134">-RecoveryPlan</span></span>
<span data-ttu-id="572bb-135">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="572bb-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="572bb-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="572bb-137">-VMNetwork</span></span>
<span data-ttu-id="572bb-138">Especifica a rede de máquina virtual de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="572bb-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572bb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572bb-139">CommonParameters</span></span>
<span data-ttu-id="572bb-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572bb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572bb-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572bb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572bb-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="572bb-142">INPUTS</span></span>

### <span data-ttu-id="572bb-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="572bb-143">ASRProtectionEntity</span></span>
<span data-ttu-id="572bb-144">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="572bb-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="572bb-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="572bb-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="572bb-146">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="572bb-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="572bb-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="572bb-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="572bb-148">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="572bb-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="572bb-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="572bb-149">OUTPUTS</span></span>

### <span data-ttu-id="572bb-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="572bb-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="572bb-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="572bb-151">NOTES</span></span>

## <span data-ttu-id="572bb-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="572bb-152">RELATED LINKS</span></span>

[<span data-ttu-id="572bb-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="572bb-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
