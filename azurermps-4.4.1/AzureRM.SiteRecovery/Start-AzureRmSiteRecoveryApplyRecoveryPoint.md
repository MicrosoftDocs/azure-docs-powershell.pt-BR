---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429067"
---
# <span data-ttu-id="ab787-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ab787-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="ab787-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab787-102">SYNOPSIS</span></span>
<span data-ttu-id="ab787-103">Altera um ponto de recuperação para um item com falha na proteção antes de confirmar a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="ab787-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab787-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab787-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab787-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab787-105">DESCRIPTION</span></span>
<span data-ttu-id="ab787-106">**Start-AzureRmSiteRecoveryApplyRecoveryPoint** altera um ponto de recuperação para um item com falha na proteção antes de confirmar a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="ab787-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="ab787-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab787-107">EXAMPLES</span></span>

## <span data-ttu-id="ab787-108">OS</span><span class="sxs-lookup"><span data-stu-id="ab787-108">PARAMETERS</span></span>

### <span data-ttu-id="ab787-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ab787-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="ab787-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ab787-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="ab787-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ab787-111">-RecoveryPoint</span></span>
<span data-ttu-id="ab787-112">Especifica o objeto de ponto de recuperação que este cmdlet altera.</span><span class="sxs-lookup"><span data-stu-id="ab787-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab787-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ab787-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ab787-114">Especifica o objeto de item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="ab787-114">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab787-115">-DefaultProfile</span></span>
<span data-ttu-id="ab787-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab787-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab787-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab787-117">CommonParameters</span></span>
<span data-ttu-id="ab787-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab787-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab787-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab787-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab787-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab787-120">INPUTS</span></span>

### <span data-ttu-id="ab787-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ab787-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="ab787-122">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ab787-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="ab787-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab787-123">OUTPUTS</span></span>

### <span data-ttu-id="ab787-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ab787-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab787-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab787-125">NOTES</span></span>

## <span data-ttu-id="ab787-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab787-126">RELATED LINKS</span></span>

[<span data-ttu-id="ab787-127">Cmdlets do Azure site Recovery</span><span class="sxs-lookup"><span data-stu-id="ab787-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
