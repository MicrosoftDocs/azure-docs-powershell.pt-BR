---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114925"
---
# <span data-ttu-id="1a0d0-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="1a0d0-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="1a0d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0d0-103">Alternar a replicação de um servidor de processos para outro para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="1a0d0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a0d0-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0d0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a0d0-105">DESCRIPTION</span></span>
<span data-ttu-id="1a0d0-106">O **Start-AzRecoveryServicesAsrSwserviceProcessServerJob** alterna o movimento de dados de replicação para as máquinas virtuais especificadas ou um servidor de Processo especificado para o servidor de Processo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="1a0d0-107">Usado para balanceamento de carga ou alternação de replicação entre servidores de processo.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="1a0d0-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a0d0-108">EXAMPLES</span></span>

### <span data-ttu-id="1a0d0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a0d0-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="1a0d0-110">Trabalho para controlar o servidor de processo de alternação de todos os itens protegidos por replicação da origem para o servidor de processo de destino.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="1a0d0-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1a0d0-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="1a0d0-112">Trabalho para controlar o servidor de processo de mudança para item protegido por replicação passado da origem para o servidor de processo de destino.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="1a0d0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a0d0-113">PARAMETERS</span></span>

### <span data-ttu-id="1a0d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0d0-114">-DefaultProfile</span></span>
<span data-ttu-id="1a0d0-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a0d0-116">-Malha</span><span class="sxs-lookup"><span data-stu-id="1a0d0-116">-Fabric</span></span>
<span data-ttu-id="1a0d0-117">Malha de recuperação de site correspondente ao Servidor de Configuração.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="1a0d0-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1a0d0-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1a0d0-119">Lista de itens protegidos por replicação cujo servidor de processo será alternado.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="1a0d0-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="1a0d0-120">-SourceProcessServer</span></span>
<span data-ttu-id="1a0d0-121">O Servidor de processo para a replicação.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="1a0d0-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="1a0d0-122">-TargetProcessServer</span></span>
<span data-ttu-id="1a0d0-123">O Servidor de processo para o que alternar a replicação.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="1a0d0-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1a0d0-124">-Confirm</span></span>
<span data-ttu-id="1a0d0-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0d0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0d0-126">-WhatIf</span></span>
<span data-ttu-id="1a0d0-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a0d0-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0d0-129">CommonParameters</span></span>
<span data-ttu-id="1a0d0-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0d0-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a0d0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0d0-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="1a0d0-132">INPUTS</span></span>

### <span data-ttu-id="1a0d0-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1a0d0-133">None</span></span>

## <span data-ttu-id="1a0d0-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1a0d0-134">OUTPUTS</span></span>

### <span data-ttu-id="1a0d0-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a0d0-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a0d0-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1a0d0-136">NOTES</span></span>

## <span data-ttu-id="1a0d0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a0d0-137">RELATED LINKS</span></span>
