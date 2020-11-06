---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 6ee25231b7bb8861a1294537e2f42a0bf914b994
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602100"
---
# <span data-ttu-id="91925-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="91925-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="91925-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91925-102">SYNOPSIS</span></span>
<span data-ttu-id="91925-103">Inicia a ressincronização de duplicação.</span><span class="sxs-lookup"><span data-stu-id="91925-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91925-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91925-104">SYNTAX</span></span>

### <span data-ttu-id="91925-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="91925-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91925-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91925-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91925-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91925-107">DESCRIPTION</span></span>
<span data-ttu-id="91925-108">O cmdlet **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** inicia a ressincronização da replicação para o item protegido especificado se a proteção estiver em um estado obrigatório de ressincronização.</span><span class="sxs-lookup"><span data-stu-id="91925-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="91925-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91925-109">EXAMPLES</span></span>

### <span data-ttu-id="91925-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91925-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="91925-111">Inicia o trabalho para sincronizar novamente a replicação no item protegido de replicação aprovado.</span><span class="sxs-lookup"><span data-stu-id="91925-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="91925-112">OS</span><span class="sxs-lookup"><span data-stu-id="91925-112">PARAMETERS</span></span>

### <span data-ttu-id="91925-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91925-113">-DefaultProfile</span></span>
<span data-ttu-id="91925-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91925-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91925-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91925-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="91925-116">Duplicação ASR item protegido para sincronização de replicação.</span><span class="sxs-lookup"><span data-stu-id="91925-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91925-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91925-117">-ResourceId</span></span>
<span data-ttu-id="91925-118">ID do recurso de item protegido de replicação para sincronizar novamente.</span><span class="sxs-lookup"><span data-stu-id="91925-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91925-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91925-119">-Confirm</span></span>
<span data-ttu-id="91925-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91925-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91925-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91925-121">-WhatIf</span></span>
<span data-ttu-id="91925-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91925-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91925-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91925-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91925-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91925-124">CommonParameters</span></span>
<span data-ttu-id="91925-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91925-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91925-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91925-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91925-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91925-127">INPUTS</span></span>

### <span data-ttu-id="91925-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91925-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="91925-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91925-129">OUTPUTS</span></span>

### <span data-ttu-id="91925-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="91925-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91925-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91925-131">NOTES</span></span>

## <span data-ttu-id="91925-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91925-132">RELATED LINKS</span></span>
