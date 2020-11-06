---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426646"
---
# <span data-ttu-id="b974b-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b974b-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="b974b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b974b-102">SYNOPSIS</span></span>
<span data-ttu-id="b974b-103">Altera um ponto de recuperação para um item com falha na proteção antes de confirmar a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="b974b-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b974b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b974b-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b974b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b974b-105">DESCRIPTION</span></span>
<span data-ttu-id="b974b-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** altera o ponto de recuperação para um item com falha na proteção antes de confirmar a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="b974b-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="b974b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b974b-107">EXAMPLES</span></span>

### <span data-ttu-id="b974b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b974b-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b974b-109">Inicia a aplicação do ponto de recuperação especificado no item de replicação protegida e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="b974b-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b974b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b974b-110">PARAMETERS</span></span>

### <span data-ttu-id="b974b-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b974b-111">-Confirm</span></span>
<span data-ttu-id="b974b-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b974b-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b974b-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b974b-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="b974b-114">Especifica o arquivo de certificado primário se a criptografia de dados estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="b974b-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="b974b-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b974b-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="b974b-116">Especifica o arquivo de certificado secundário se a criptografia de dados estiver sendo usada.</span><span class="sxs-lookup"><span data-stu-id="b974b-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="b974b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b974b-117">-DefaultProfile</span></span>
<span data-ttu-id="b974b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b974b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b974b-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b974b-119">-RecoveryPoint</span></span>
<span data-ttu-id="b974b-120">Especifica o objeto de ponto de recuperação correspondente ao ponto de recuperação a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="b974b-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b974b-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b974b-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b974b-122">Especifica o objeto de item protegido da replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="b974b-122">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b974b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b974b-123">-WhatIf</span></span>
<span data-ttu-id="b974b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b974b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b974b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b974b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b974b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b974b-126">CommonParameters</span></span>
<span data-ttu-id="b974b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b974b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b974b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b974b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b974b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b974b-129">INPUTS</span></span>

### <span data-ttu-id="b974b-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b974b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b974b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b974b-131">OUTPUTS</span></span>

### <span data-ttu-id="b974b-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b974b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b974b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b974b-133">NOTES</span></span>

## <span data-ttu-id="b974b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b974b-134">RELATED LINKS</span></span>

[<span data-ttu-id="b974b-135">Cmdlets do Azure site Recovery</span><span class="sxs-lookup"><span data-stu-id="b974b-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
