---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 748278cd6096a8ab67538df77aa3b81cc54d3ace
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886416"
---
# <span data-ttu-id="b4930-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b4930-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="b4930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4930-102">SYNOPSIS</span></span>
<span data-ttu-id="b4930-103">Altera um ponto de recuperação para um item protegido com falha antes de comprometer a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="b4930-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="b4930-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4930-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4930-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4930-105">DESCRIPTION</span></span>
<span data-ttu-id="b4930-106">O **Start-AzRecoveryServicesAsrApplyRecoveryPoint** altera o ponto de recuperação de um item com falha sobre protegido antes de comprometer a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="b4930-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="b4930-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4930-107">EXAMPLES</span></span>

### <span data-ttu-id="b4930-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4930-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b4930-109">Inicia a aplicação do ponto de recuperação especificado ao item protegido de replicação e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="b4930-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b4930-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4930-110">PARAMETERS</span></span>

### <span data-ttu-id="b4930-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b4930-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="b4930-112">Especifica o arquivo de certificado principal se a criptografia de dados estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="b4930-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="b4930-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b4930-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="b4930-114">Especifica o arquivo de certificado secundário se a criptografia de dados estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="b4930-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="b4930-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4930-115">-DefaultProfile</span></span>
<span data-ttu-id="b4930-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4930-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b4930-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b4930-117">-RecoveryPoint</span></span>
<span data-ttu-id="b4930-118">Especifica o objeto de ponto de recuperação correspondente ao ponto de recuperação a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="b4930-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="b4930-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b4930-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b4930-120">Especifica o objeto de item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="b4930-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="b4930-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4930-121">-Confirm</span></span>
<span data-ttu-id="b4930-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4930-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4930-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4930-123">-WhatIf</span></span>
<span data-ttu-id="b4930-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4930-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4930-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4930-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4930-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4930-126">CommonParameters</span></span>
<span data-ttu-id="b4930-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4930-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4930-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4930-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4930-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4930-129">INPUTS</span></span>

### <span data-ttu-id="b4930-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b4930-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b4930-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4930-131">OUTPUTS</span></span>

### <span data-ttu-id="b4930-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b4930-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b4930-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4930-133">NOTES</span></span>

## <span data-ttu-id="b4930-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4930-134">RELATED LINKS</span></span>

[<span data-ttu-id="b4930-135">Cmdlets de Recuperação de Site do Azure</span><span class="sxs-lookup"><span data-stu-id="b4930-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
