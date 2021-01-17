---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428779"
---
# <span data-ttu-id="e44b3-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="e44b3-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="e44b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e44b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e44b3-103">Alterne a replicação de um servidor de processo para outro para o balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="e44b3-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="e44b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e44b3-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e44b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e44b3-106">O **Start-AzRecoveryServicesAsrSwitchProcessServerJob** alterna a movimentação de dados de replicação das máquinas virtuais especificadas ou um servidor de processo especificado para o servidor de processo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="e44b3-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="e44b3-107">Usado para balancear a carga ou alternar a replicação entre servidores de processo.</span><span class="sxs-lookup"><span data-stu-id="e44b3-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="e44b3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e44b3-108">EXAMPLES</span></span>

### <span data-ttu-id="e44b3-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e44b3-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="e44b3-110">Trabalho para acompanhar a mudança do servidor de processo para todos os itens protegidos de origem do servidor de processo de destino.</span><span class="sxs-lookup"><span data-stu-id="e44b3-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="e44b3-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e44b3-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="e44b3-112">Trabalho para acompanhar o processo de comutação do servidor para o item protegido de replicação do servidor de processo de origem para destino.</span><span class="sxs-lookup"><span data-stu-id="e44b3-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="e44b3-113">OS</span><span class="sxs-lookup"><span data-stu-id="e44b3-113">PARAMETERS</span></span>

### <span data-ttu-id="e44b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44b3-114">-DefaultProfile</span></span>
<span data-ttu-id="e44b3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e44b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e44b3-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e44b3-116">-Fabric</span></span>
<span data-ttu-id="e44b3-117">Infraestrutura de recuperação de site correspondente ao servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="e44b3-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44b3-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e44b3-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e44b3-119">Lista de itens protegidos por replicação cujo servidor de processo deve ser trocado.</span><span class="sxs-lookup"><span data-stu-id="e44b3-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44b3-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="e44b3-120">-SourceProcessServer</span></span>
<span data-ttu-id="e44b3-121">O servidor de processo para o qual mudar de replicação.</span><span class="sxs-lookup"><span data-stu-id="e44b3-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44b3-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="e44b3-122">-TargetProcessServer</span></span>
<span data-ttu-id="e44b3-123">O servidor de processo para o qual mudar a replicação.</span><span class="sxs-lookup"><span data-stu-id="e44b3-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44b3-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e44b3-124">-Confirm</span></span>
<span data-ttu-id="e44b3-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e44b3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44b3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44b3-126">-WhatIf</span></span>
<span data-ttu-id="e44b3-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e44b3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44b3-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e44b3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44b3-129">CommonParameters</span></span>
<span data-ttu-id="e44b3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44b3-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e44b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44b3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e44b3-132">INPUTS</span></span>

### <span data-ttu-id="e44b3-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e44b3-133">None</span></span>

## <span data-ttu-id="e44b3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e44b3-134">OUTPUTS</span></span>

### <span data-ttu-id="e44b3-135">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e44b3-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e44b3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e44b3-136">NOTES</span></span>

## <span data-ttu-id="e44b3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e44b3-137">RELATED LINKS</span></span>
