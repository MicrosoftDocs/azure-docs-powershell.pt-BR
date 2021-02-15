---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114927"
---
# <span data-ttu-id="641c6-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="641c6-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="641c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="641c6-102">SYNOPSIS</span></span>
<span data-ttu-id="641c6-103">Inicia a replicação de sincronização.</span><span class="sxs-lookup"><span data-stu-id="641c6-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="641c6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="641c6-104">SYNTAX</span></span>

### <span data-ttu-id="641c6-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="641c6-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="641c6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="641c6-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="641c6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="641c6-107">DESCRIPTION</span></span>
<span data-ttu-id="641c6-108">O cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** iniciará a ressincronização da replicação para o item protegido especificado se o protegido estiver em um estado necessário de ressincronização.</span><span class="sxs-lookup"><span data-stu-id="641c6-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="641c6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="641c6-109">EXAMPLES</span></span>

### <span data-ttu-id="641c6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="641c6-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="641c6-111">Inicia o trabalho para ressincronizar a replicação em um item protegido por replicação passada.</span><span class="sxs-lookup"><span data-stu-id="641c6-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="641c6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="641c6-112">PARAMETERS</span></span>

### <span data-ttu-id="641c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641c6-113">-DefaultProfile</span></span>
<span data-ttu-id="641c6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="641c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="641c6-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="641c6-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="641c6-116">Item protegido de replicação asR para ressincronizar a replicação.</span><span class="sxs-lookup"><span data-stu-id="641c6-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="641c6-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="641c6-117">-ResourceId</span></span>
<span data-ttu-id="641c6-118">ID do recurso do item protegido por replicação para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="641c6-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="641c6-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="641c6-119">-Confirm</span></span>
<span data-ttu-id="641c6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="641c6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="641c6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="641c6-121">-WhatIf</span></span>
<span data-ttu-id="641c6-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="641c6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="641c6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="641c6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="641c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641c6-124">CommonParameters</span></span>
<span data-ttu-id="641c6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641c6-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="641c6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641c6-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="641c6-127">INPUTS</span></span>

### <span data-ttu-id="641c6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="641c6-128">System.String</span></span>

### <span data-ttu-id="641c6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="641c6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="641c6-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="641c6-130">OUTPUTS</span></span>

### <span data-ttu-id="641c6-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="641c6-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="641c6-132">Notas</span><span class="sxs-lookup"><span data-stu-id="641c6-132">NOTES</span></span>

## <span data-ttu-id="641c6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="641c6-133">RELATED LINKS</span></span>
