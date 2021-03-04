---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 533a5932aea282158bb1f53bf9464942ed9f17c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885535"
---
# <span data-ttu-id="83332-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83332-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="83332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83332-102">SYNOPSIS</span></span>
<span data-ttu-id="83332-103">Interrompe/desabilita a replicação para um item protegido de replicação de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="83332-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="83332-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="83332-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83332-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="83332-105">DESCRIPTION</span></span>
<span data-ttu-id="83332-106">O cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** desabilita a replicação do item protegido de replicação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="83332-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="83332-107">Essa operação faz com que a replicação pare para o item protegido.</span><span class="sxs-lookup"><span data-stu-id="83332-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="83332-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83332-108">EXAMPLES</span></span>

### <span data-ttu-id="83332-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83332-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="83332-110">Inicia a operação desabilitar a replicação do item protegido de replicação especificado e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="83332-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="83332-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="83332-111">PARAMETERS</span></span>

### <span data-ttu-id="83332-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83332-112">-DefaultProfile</span></span>
<span data-ttu-id="83332-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83332-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="83332-114">-Force</span><span class="sxs-lookup"><span data-stu-id="83332-114">-Force</span></span>
<span data-ttu-id="83332-115">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="83332-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83332-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83332-116">-InputObject</span></span>
<span data-ttu-id="83332-117">O objeto de entrada para o cmdlet: o objeto de item protegido de replicação ASR correspondente ao item protegido de replicação para o qual a replicação deve ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="83332-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83332-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="83332-118">-WaitForCompletion</span></span>
<span data-ttu-id="83332-119">Indica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="83332-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83332-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83332-120">-Confirm</span></span>
<span data-ttu-id="83332-121">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="83332-121">Specify if confirmation is required.</span></span> <span data-ttu-id="83332-122">De definir o valor do parâmetro confirme como $false para ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="83332-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="83332-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83332-123">-WhatIf</span></span>
<span data-ttu-id="83332-124">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83332-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="83332-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83332-125">CommonParameters</span></span>
<span data-ttu-id="83332-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83332-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83332-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83332-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83332-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83332-128">INPUTS</span></span>

### <span data-ttu-id="83332-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83332-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="83332-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="83332-130">OUTPUTS</span></span>

### <span data-ttu-id="83332-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="83332-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="83332-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="83332-132">NOTES</span></span>

## <span data-ttu-id="83332-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83332-133">RELATED LINKS</span></span>

[<span data-ttu-id="83332-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83332-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="83332-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83332-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="83332-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83332-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
