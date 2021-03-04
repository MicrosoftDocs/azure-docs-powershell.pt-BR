---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0675756b21c5af56ff3dc3fdff3b48d3bc9c999c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889890"
---
# <span data-ttu-id="912ed-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="912ed-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="912ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912ed-102">SYNOPSIS</span></span>
<span data-ttu-id="912ed-103">Inicia a ressincronização de replicação.</span><span class="sxs-lookup"><span data-stu-id="912ed-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="912ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="912ed-104">SYNTAX</span></span>

### <span data-ttu-id="912ed-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="912ed-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="912ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="912ed-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="912ed-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="912ed-107">DESCRIPTION</span></span>
<span data-ttu-id="912ed-108">O cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** inicia a ressincronização da replicação para o item protegido especificado se o protegido estiver em um estado necessário de ressincronização.</span><span class="sxs-lookup"><span data-stu-id="912ed-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="912ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="912ed-109">EXAMPLES</span></span>

### <span data-ttu-id="912ed-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="912ed-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="912ed-111">Inicia o trabalho para ressincronizar a replicação no item protegido de replicação passado.</span><span class="sxs-lookup"><span data-stu-id="912ed-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="912ed-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="912ed-112">PARAMETERS</span></span>

### <span data-ttu-id="912ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912ed-113">-DefaultProfile</span></span>
<span data-ttu-id="912ed-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="912ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="912ed-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="912ed-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="912ed-116">Item protegido de replicação ASR para ressincronizar a replicação.</span><span class="sxs-lookup"><span data-stu-id="912ed-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="912ed-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="912ed-117">-ResourceId</span></span>
<span data-ttu-id="912ed-118">ID de recurso do item protegido de replicação para ressincronizar.</span><span class="sxs-lookup"><span data-stu-id="912ed-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="912ed-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="912ed-119">-Confirm</span></span>
<span data-ttu-id="912ed-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="912ed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="912ed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="912ed-121">-WhatIf</span></span>
<span data-ttu-id="912ed-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="912ed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="912ed-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="912ed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="912ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912ed-124">CommonParameters</span></span>
<span data-ttu-id="912ed-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912ed-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="912ed-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912ed-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="912ed-127">INPUTS</span></span>

### <span data-ttu-id="912ed-128">System.String</span><span class="sxs-lookup"><span data-stu-id="912ed-128">System.String</span></span>

### <span data-ttu-id="912ed-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="912ed-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="912ed-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="912ed-130">OUTPUTS</span></span>

### <span data-ttu-id="912ed-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="912ed-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="912ed-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="912ed-132">NOTES</span></span>

## <span data-ttu-id="912ed-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="912ed-133">RELATED LINKS</span></span>
