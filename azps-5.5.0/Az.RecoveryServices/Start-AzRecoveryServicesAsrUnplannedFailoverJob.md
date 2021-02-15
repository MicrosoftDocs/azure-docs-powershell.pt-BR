---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111463"
---
# <span data-ttu-id="0afca-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0afca-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="0afca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0afca-102">SYNOPSIS</span></span>
<span data-ttu-id="0afca-103">Inicia uma operação de failover não planejada.</span><span class="sxs-lookup"><span data-stu-id="0afca-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="0afca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0afca-104">SYNTAX</span></span>

### <span data-ttu-id="0afca-105">ByRPIObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0afca-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afca-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0afca-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afca-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0afca-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afca-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0afca-108">DESCRIPTION</span></span>
<span data-ttu-id="0afca-109">O cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** inicia failover não planejado de um item protegido ou plano de recuperação de Recuperação de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="0afca-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="0afca-110">Você pode verificar se o trabalho foi bem-sucedido usando Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afca-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="0afca-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0afca-111">EXAMPLES</span></span>

### <span data-ttu-id="0afca-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0afca-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="0afca-113">Inicia a operação de failover não planejada para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="0afca-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="0afca-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0afca-114">Example 2</span></span>

<span data-ttu-id="0afca-115">Inicia uma operação de failover não planejada.</span><span class="sxs-lookup"><span data-stu-id="0afca-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="0afca-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="0afca-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="0afca-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0afca-117">PARAMETERS</span></span>

### <span data-ttu-id="0afca-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0afca-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0afca-119">Especifica o caminho do arquivo de certificado principal de criptografia de dados para failover do Item Protegido.</span><span class="sxs-lookup"><span data-stu-id="0afca-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="0afca-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0afca-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0afca-121">Especifica o caminho do arquivo de certificado secundário de criptografia de dados para failover do Item Protegido.</span><span class="sxs-lookup"><span data-stu-id="0afca-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="0afca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afca-122">-DefaultProfile</span></span>
<span data-ttu-id="0afca-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0afca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0afca-124">-Direção</span><span class="sxs-lookup"><span data-stu-id="0afca-124">-Direction</span></span>
<span data-ttu-id="0afca-125">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="0afca-125">Specifies the failover direction.</span></span>
<span data-ttu-id="0afca-126">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0afca-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0afca-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0afca-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="0afca-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0afca-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="0afca-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="0afca-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="0afca-130">Execute a operação no lado de origem antes de iniciar o failover não planejado.</span><span class="sxs-lookup"><span data-stu-id="0afca-130">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="0afca-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0afca-131">-RecoveryPlan</span></span>
<span data-ttu-id="0afca-132">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="0afca-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="0afca-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0afca-133">-RecoveryPoint</span></span>
<span data-ttu-id="0afca-134">Especifica um ponto de recuperação personalizado para o failover do computador protegido.</span><span class="sxs-lookup"><span data-stu-id="0afca-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="0afca-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0afca-135">-RecoveryTag</span></span>
<span data-ttu-id="0afca-136">Especifica a marca de recuperação para o failover.</span><span class="sxs-lookup"><span data-stu-id="0afca-136">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="0afca-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0afca-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0afca-138">Especifica um item protegido de replicação de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="0afca-138">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="0afca-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0afca-139">-Confirm</span></span>
<span data-ttu-id="0afca-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afca-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afca-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afca-141">-WhatIf</span></span>
<span data-ttu-id="0afca-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0afca-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0afca-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0afca-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afca-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afca-144">CommonParameters</span></span>
<span data-ttu-id="0afca-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afca-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afca-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0afca-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afca-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="0afca-147">INPUTS</span></span>

### <span data-ttu-id="0afca-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0afca-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="0afca-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0afca-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0afca-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="0afca-150">OUTPUTS</span></span>

### <span data-ttu-id="0afca-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="0afca-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0afca-152">Notas</span><span class="sxs-lookup"><span data-stu-id="0afca-152">NOTES</span></span>

## <span data-ttu-id="0afca-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0afca-153">RELATED LINKS</span></span>

[<span data-ttu-id="0afca-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0afca-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
