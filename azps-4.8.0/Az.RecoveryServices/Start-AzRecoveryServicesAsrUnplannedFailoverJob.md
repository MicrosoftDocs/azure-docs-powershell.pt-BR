---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947678"
---
# <span data-ttu-id="bca3a-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="bca3a-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="bca3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bca3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bca3a-103">Inicia uma operação de failover não planejada.</span><span class="sxs-lookup"><span data-stu-id="bca3a-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="bca3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bca3a-104">SYNTAX</span></span>

### <span data-ttu-id="bca3a-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="bca3a-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bca3a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="bca3a-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bca3a-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="bca3a-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bca3a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bca3a-108">DESCRIPTION</span></span>
<span data-ttu-id="bca3a-109">O cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** inicia o failover não planejado de um item protegido de replicação do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bca3a-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="bca3a-110">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="bca3a-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="bca3a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bca3a-111">EXAMPLES</span></span>

### <span data-ttu-id="bca3a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bca3a-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="bca3a-113">Inicia a operação de failover não planejado para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="bca3a-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="bca3a-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bca3a-114">Example 2</span></span>

<span data-ttu-id="bca3a-115">Inicia uma operação de failover não planejada.</span><span class="sxs-lookup"><span data-stu-id="bca3a-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="bca3a-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="bca3a-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="bca3a-117">OS</span><span class="sxs-lookup"><span data-stu-id="bca3a-117">PARAMETERS</span></span>

### <span data-ttu-id="bca3a-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="bca3a-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="bca3a-119">Especifica o caminho do arquivo de certificado primário de criptografia de dados para o failover do item protegido.</span><span class="sxs-lookup"><span data-stu-id="bca3a-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="bca3a-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="bca3a-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="bca3a-121">Especifica o caminho do arquivo de certificado secundário de criptografia de dados para o failover do item protegido.</span><span class="sxs-lookup"><span data-stu-id="bca3a-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="bca3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca3a-122">-DefaultProfile</span></span>
<span data-ttu-id="bca3a-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bca3a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bca3a-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="bca3a-124">-Direction</span></span>
<span data-ttu-id="bca3a-125">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="bca3a-125">Specifies the failover direction.</span></span>
<span data-ttu-id="bca3a-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bca3a-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bca3a-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="bca3a-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="bca3a-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="bca3a-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="bca3a-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="bca3a-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="bca3a-130">Executar a operação no lado da fonte antes de iniciar o failover não planejado.</span><span class="sxs-lookup"><span data-stu-id="bca3a-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca3a-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bca3a-131">-RecoveryPlan</span></span>
<span data-ttu-id="bca3a-132">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="bca3a-132">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bca3a-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bca3a-133">-RecoveryPoint</span></span>
<span data-ttu-id="bca3a-134">Especifica um ponto de recuperação personalizado no qual fazer failover da máquina protegida.</span><span class="sxs-lookup"><span data-stu-id="bca3a-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca3a-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="bca3a-135">-RecoveryTag</span></span>
<span data-ttu-id="bca3a-136">Especifica a marca de recuperação para failover.</span><span class="sxs-lookup"><span data-stu-id="bca3a-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca3a-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bca3a-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bca3a-138">Especifica um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bca3a-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bca3a-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bca3a-139">-Confirm</span></span>
<span data-ttu-id="bca3a-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bca3a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bca3a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bca3a-141">-WhatIf</span></span>
<span data-ttu-id="bca3a-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bca3a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bca3a-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bca3a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bca3a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca3a-144">CommonParameters</span></span>
<span data-ttu-id="bca3a-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca3a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca3a-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bca3a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca3a-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bca3a-147">INPUTS</span></span>

### <span data-ttu-id="bca3a-148">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bca3a-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="bca3a-149">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bca3a-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bca3a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bca3a-150">OUTPUTS</span></span>

### <span data-ttu-id="bca3a-151">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bca3a-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bca3a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bca3a-152">NOTES</span></span>

## <span data-ttu-id="bca3a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bca3a-153">RELATED LINKS</span></span>

[<span data-ttu-id="bca3a-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bca3a-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
