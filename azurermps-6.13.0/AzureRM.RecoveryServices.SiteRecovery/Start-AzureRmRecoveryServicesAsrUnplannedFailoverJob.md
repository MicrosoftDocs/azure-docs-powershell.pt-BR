---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: b7a9dffe443ca7603b8b5a3bdd100560d83a498e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427202"
---
# <span data-ttu-id="087f3-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="087f3-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="087f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="087f3-102">SYNOPSIS</span></span>
<span data-ttu-id="087f3-103">Inicia uma operação de failover não planejada.</span><span class="sxs-lookup"><span data-stu-id="087f3-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="087f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="087f3-104">SYNTAX</span></span>

### <span data-ttu-id="087f3-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="087f3-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="087f3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="087f3-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="087f3-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="087f3-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="087f3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="087f3-108">DESCRIPTION</span></span>
<span data-ttu-id="087f3-109">O cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** inicia o failover de teste de um item protegido de replicação do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="087f3-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="087f3-110">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="087f3-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="087f3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="087f3-111">EXAMPLES</span></span>

### <span data-ttu-id="087f3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="087f3-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="087f3-113">Inicia a operação de failover de teste para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="087f3-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="087f3-114">OS</span><span class="sxs-lookup"><span data-stu-id="087f3-114">PARAMETERS</span></span>

### <span data-ttu-id="087f3-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="087f3-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="087f3-116">Especifica o caminho do arquivo de certificado primário de criptografia de dados para o failover do item protegido.</span><span class="sxs-lookup"><span data-stu-id="087f3-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="087f3-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="087f3-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="087f3-118">Especifica o caminho do arquivo de certificado secundário de criptografia de dados para o failover do item protegido.</span><span class="sxs-lookup"><span data-stu-id="087f3-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="087f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087f3-119">-DefaultProfile</span></span>
<span data-ttu-id="087f3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="087f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="087f3-121">-Direction</span><span class="sxs-lookup"><span data-stu-id="087f3-121">-Direction</span></span>
<span data-ttu-id="087f3-122">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="087f3-122">Specifies the failover direction.</span></span>
<span data-ttu-id="087f3-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="087f3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="087f3-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="087f3-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="087f3-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="087f3-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="087f3-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="087f3-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="087f3-127">Executar a operação no lado da fonte antes de iniciar o failover não planejado.</span><span class="sxs-lookup"><span data-stu-id="087f3-127">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="087f3-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="087f3-128">-RecoveryPlan</span></span>
<span data-ttu-id="087f3-129">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="087f3-129">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="087f3-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="087f3-130">-RecoveryPoint</span></span>
<span data-ttu-id="087f3-131">Especifica um ponto de recuperação personalizado no qual fazer failover da máquina protegida.</span><span class="sxs-lookup"><span data-stu-id="087f3-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="087f3-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="087f3-132">-RecoveryTag</span></span>
<span data-ttu-id="087f3-133">Especifica a marca de recuperação para failover.</span><span class="sxs-lookup"><span data-stu-id="087f3-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

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
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087f3-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="087f3-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="087f3-135">Especifica um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="087f3-135">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="087f3-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="087f3-136">-Confirm</span></span>
<span data-ttu-id="087f3-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="087f3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="087f3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="087f3-138">-WhatIf</span></span>
<span data-ttu-id="087f3-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="087f3-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="087f3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="087f3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="087f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087f3-141">CommonParameters</span></span>
<span data-ttu-id="087f3-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087f3-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="087f3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087f3-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="087f3-144">INPUTS</span></span>

### <span data-ttu-id="087f3-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="087f3-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="087f3-146">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="087f3-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="087f3-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="087f3-147">OUTPUTS</span></span>

### <span data-ttu-id="087f3-148">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="087f3-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="087f3-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="087f3-149">NOTES</span></span>

## <span data-ttu-id="087f3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="087f3-150">RELATED LINKS</span></span>

[<span data-ttu-id="087f3-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="087f3-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)