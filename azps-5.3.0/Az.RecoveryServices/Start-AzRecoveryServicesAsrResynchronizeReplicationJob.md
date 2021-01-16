---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272492"
---
# <span data-ttu-id="b90f1-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="b90f1-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="b90f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b90f1-102">SYNOPSIS</span></span>
<span data-ttu-id="b90f1-103">Inicia a ressincronização de duplicação.</span><span class="sxs-lookup"><span data-stu-id="b90f1-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="b90f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b90f1-104">SYNTAX</span></span>

### <span data-ttu-id="b90f1-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="b90f1-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b90f1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b90f1-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90f1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b90f1-107">DESCRIPTION</span></span>
<span data-ttu-id="b90f1-108">O cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** inicia a ressincronização da replicação para o item protegido especificado se a proteção estiver em um estado obrigatório de ressincronização.</span><span class="sxs-lookup"><span data-stu-id="b90f1-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="b90f1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b90f1-109">EXAMPLES</span></span>

### <span data-ttu-id="b90f1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b90f1-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="b90f1-111">Inicia o trabalho para sincronizar novamente a replicação no item protegido de replicação aprovado.</span><span class="sxs-lookup"><span data-stu-id="b90f1-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="b90f1-112">OS</span><span class="sxs-lookup"><span data-stu-id="b90f1-112">PARAMETERS</span></span>

### <span data-ttu-id="b90f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90f1-113">-DefaultProfile</span></span>
<span data-ttu-id="b90f1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b90f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b90f1-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b90f1-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b90f1-116">Duplicação ASR item protegido para sincronização de replicação.</span><span class="sxs-lookup"><span data-stu-id="b90f1-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="b90f1-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b90f1-117">-ResourceId</span></span>
<span data-ttu-id="b90f1-118">ID do recurso de item protegido de replicação para sincronizar novamente.</span><span class="sxs-lookup"><span data-stu-id="b90f1-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="b90f1-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b90f1-119">-Confirm</span></span>
<span data-ttu-id="b90f1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b90f1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b90f1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90f1-121">-WhatIf</span></span>
<span data-ttu-id="b90f1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b90f1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90f1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b90f1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b90f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90f1-124">CommonParameters</span></span>
<span data-ttu-id="b90f1-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b90f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90f1-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b90f1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90f1-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b90f1-127">INPUTS</span></span>

### <span data-ttu-id="b90f1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b90f1-128">System.String</span></span>

### <span data-ttu-id="b90f1-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b90f1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b90f1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b90f1-130">OUTPUTS</span></span>

### <span data-ttu-id="b90f1-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b90f1-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b90f1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b90f1-132">NOTES</span></span>

## <span data-ttu-id="b90f1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b90f1-133">RELATED LINKS</span></span>
