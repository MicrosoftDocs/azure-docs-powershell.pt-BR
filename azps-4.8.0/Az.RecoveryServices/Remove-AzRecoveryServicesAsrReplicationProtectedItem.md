---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112184"
---
# <span data-ttu-id="93396-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93396-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="93396-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93396-102">SYNOPSIS</span></span>
<span data-ttu-id="93396-103">Interrompe/desabilita a replicação de um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="93396-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="93396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93396-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93396-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93396-105">DESCRIPTION</span></span>
<span data-ttu-id="93396-106">O cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** desabilita a replicação do item de replicação do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="93396-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="93396-107">Esta operação faz com que a duplicação pare para o item protegido.</span><span class="sxs-lookup"><span data-stu-id="93396-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="93396-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93396-108">EXAMPLES</span></span>

### <span data-ttu-id="93396-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93396-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="93396-110">Inicia a operação de desabilitação de replicação para o item protegido de replicação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="93396-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="93396-111">OS</span><span class="sxs-lookup"><span data-stu-id="93396-111">PARAMETERS</span></span>

### <span data-ttu-id="93396-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93396-112">-DefaultProfile</span></span>
<span data-ttu-id="93396-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93396-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="93396-114">-Force</span><span class="sxs-lookup"><span data-stu-id="93396-114">-Force</span></span>
<span data-ttu-id="93396-115">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="93396-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="93396-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93396-116">-InputObject</span></span>
<span data-ttu-id="93396-117">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao item protegido de replicação para o qual a replicação será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="93396-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="93396-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="93396-118">-WaitForCompletion</span></span>
<span data-ttu-id="93396-119">Indica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="93396-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="93396-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93396-120">-Confirm</span></span>
<span data-ttu-id="93396-121">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="93396-121">Specify if confirmation is required.</span></span> <span data-ttu-id="93396-122">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="93396-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="93396-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93396-123">-WhatIf</span></span>
<span data-ttu-id="93396-124">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93396-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="93396-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93396-125">CommonParameters</span></span>
<span data-ttu-id="93396-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93396-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93396-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93396-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93396-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93396-128">INPUTS</span></span>

### <span data-ttu-id="93396-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93396-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="93396-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93396-130">OUTPUTS</span></span>

### <span data-ttu-id="93396-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="93396-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="93396-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93396-132">NOTES</span></span>

## <span data-ttu-id="93396-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93396-133">RELATED LINKS</span></span>

[<span data-ttu-id="93396-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93396-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="93396-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93396-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="93396-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="93396-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
