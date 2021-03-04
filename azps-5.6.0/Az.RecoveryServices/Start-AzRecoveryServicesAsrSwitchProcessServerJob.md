---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 269285b806149c191e8162b41faa80177f6ca4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886414"
---
# <span data-ttu-id="ea267-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="ea267-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="ea267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea267-102">SYNOPSIS</span></span>
<span data-ttu-id="ea267-103">Alternar a replicação de um servidor de processo para outro para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="ea267-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="ea267-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea267-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea267-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea267-105">DESCRIPTION</span></span>
<span data-ttu-id="ea267-106">O **Start-AzRecoveryServicesAsrSwitchProcessServerJob** alterna o movimento de dados de replicação para as máquinas virtuais especificadas ou um servidor de Processo especificado para o servidor de Processo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="ea267-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="ea267-107">Usado para balanceamento de carga ou alternamento de replicação entre servidores de processo.</span><span class="sxs-lookup"><span data-stu-id="ea267-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="ea267-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea267-108">EXAMPLES</span></span>

### <span data-ttu-id="ea267-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea267-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="ea267-110">Trabalho para controlar o servidor de processo de alternação de todos os itens protegidos de replicação do servidor de processo de origem para destino.</span><span class="sxs-lookup"><span data-stu-id="ea267-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="ea267-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea267-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="ea267-112">Trabalho para controlar o servidor de processo de alternação do item protegido de replicação passado da origem para o servidor de processo de destino.</span><span class="sxs-lookup"><span data-stu-id="ea267-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="ea267-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea267-113">PARAMETERS</span></span>

### <span data-ttu-id="ea267-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea267-114">-DefaultProfile</span></span>
<span data-ttu-id="ea267-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ea267-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea267-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="ea267-116">-Fabric</span></span>
<span data-ttu-id="ea267-117">Malha de recuperação de site correspondente ao Servidor de Configuração.</span><span class="sxs-lookup"><span data-stu-id="ea267-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="ea267-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ea267-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ea267-119">Lista de itens protegidos por replicação cujo servidor de processo será comutado.</span><span class="sxs-lookup"><span data-stu-id="ea267-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="ea267-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="ea267-120">-SourceProcessServer</span></span>
<span data-ttu-id="ea267-121">O servidor de Processo para mudar a replicação para fora.</span><span class="sxs-lookup"><span data-stu-id="ea267-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="ea267-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="ea267-122">-TargetProcessServer</span></span>
<span data-ttu-id="ea267-123">O servidor de processo para o que alternar a replicação.</span><span class="sxs-lookup"><span data-stu-id="ea267-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="ea267-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea267-124">-Confirm</span></span>
<span data-ttu-id="ea267-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea267-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea267-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea267-126">-WhatIf</span></span>
<span data-ttu-id="ea267-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea267-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea267-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea267-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea267-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea267-129">CommonParameters</span></span>
<span data-ttu-id="ea267-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea267-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea267-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea267-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea267-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea267-132">INPUTS</span></span>

### <span data-ttu-id="ea267-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ea267-133">None</span></span>

## <span data-ttu-id="ea267-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea267-134">OUTPUTS</span></span>

### <span data-ttu-id="ea267-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea267-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea267-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea267-136">NOTES</span></span>

## <span data-ttu-id="ea267-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea267-137">RELATED LINKS</span></span>
