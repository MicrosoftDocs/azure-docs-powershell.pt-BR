---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272495"
---
# <span data-ttu-id="95d0f-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="95d0f-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="95d0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="95d0f-103">Altera um ponto de recuperação para um item com falha na proteção antes de confirmar a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="95d0f-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="95d0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95d0f-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95d0f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="95d0f-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** altera o ponto de recuperação para um item com falha na proteção antes de confirmar a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="95d0f-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="95d0f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="95d0f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95d0f-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="95d0f-109">Inicia a aplicação do ponto de recuperação especificado no item de replicação protegida e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="95d0f-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="95d0f-110">OS</span><span class="sxs-lookup"><span data-stu-id="95d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="95d0f-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="95d0f-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="95d0f-112">Especifica o arquivo de certificado primário se a criptografia de dados estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="95d0f-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="95d0f-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="95d0f-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="95d0f-114">Especifica o arquivo de certificado secundário se a criptografia de dados estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="95d0f-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="95d0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d0f-115">-DefaultProfile</span></span>
<span data-ttu-id="95d0f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95d0f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="95d0f-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="95d0f-117">-RecoveryPoint</span></span>
<span data-ttu-id="95d0f-118">Especifica o objeto de ponto de recuperação correspondente ao ponto de recuperação a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="95d0f-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d0f-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95d0f-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="95d0f-120">Especifica o objeto de item protegido da replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="95d0f-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95d0f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95d0f-121">-Confirm</span></span>
<span data-ttu-id="95d0f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d0f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d0f-123">-WhatIf</span></span>
<span data-ttu-id="95d0f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95d0f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95d0f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95d0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d0f-126">CommonParameters</span></span>
<span data-ttu-id="95d0f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d0f-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95d0f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d0f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95d0f-129">INPUTS</span></span>

### <span data-ttu-id="95d0f-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95d0f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="95d0f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95d0f-131">OUTPUTS</span></span>

### <span data-ttu-id="95d0f-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="95d0f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="95d0f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95d0f-133">NOTES</span></span>

## <span data-ttu-id="95d0f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95d0f-134">RELATED LINKS</span></span>

[<span data-ttu-id="95d0f-135">Cmdlets do Azure site Recovery</span><span class="sxs-lookup"><span data-stu-id="95d0f-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
