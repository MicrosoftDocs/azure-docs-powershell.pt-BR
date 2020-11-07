---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 19a10312046a4c52ed1fad29732347f719065b95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773469"
---
# <span data-ttu-id="554ca-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="554ca-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="554ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="554ca-102">SYNOPSIS</span></span>
<span data-ttu-id="554ca-103">Interrompe/desabilita a replicação de um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="554ca-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="554ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="554ca-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="554ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="554ca-105">DESCRIPTION</span></span>
<span data-ttu-id="554ca-106">O cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** desabilita a replicação do item de replicação do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="554ca-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="554ca-107">Esta operação faz com que a duplicação pare para o item protegido.</span><span class="sxs-lookup"><span data-stu-id="554ca-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="554ca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="554ca-108">EXAMPLES</span></span>

### <span data-ttu-id="554ca-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="554ca-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="554ca-110">Inicia a operação de desabilitação de replicação para o item protegido de replicação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="554ca-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="554ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="554ca-111">PARAMETERS</span></span>

### <span data-ttu-id="554ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="554ca-112">-DefaultProfile</span></span>
<span data-ttu-id="554ca-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="554ca-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="554ca-114">-Force</span><span class="sxs-lookup"><span data-stu-id="554ca-114">-Force</span></span>
<span data-ttu-id="554ca-115">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="554ca-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="554ca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="554ca-116">-InputObject</span></span>
<span data-ttu-id="554ca-117">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao item protegido de replicação para o qual a replicação será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="554ca-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="554ca-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="554ca-118">-WaitForCompletion</span></span>
<span data-ttu-id="554ca-119">Indica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="554ca-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="554ca-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="554ca-120">-Confirm</span></span>
<span data-ttu-id="554ca-121">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="554ca-121">Specify if confirmation is required.</span></span> <span data-ttu-id="554ca-122">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="554ca-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="554ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="554ca-123">-WhatIf</span></span>
<span data-ttu-id="554ca-124">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="554ca-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="554ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="554ca-125">CommonParameters</span></span>
<span data-ttu-id="554ca-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="554ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="554ca-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="554ca-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="554ca-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="554ca-128">INPUTS</span></span>

### <span data-ttu-id="554ca-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="554ca-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="554ca-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="554ca-130">OUTPUTS</span></span>

### <span data-ttu-id="554ca-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="554ca-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="554ca-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="554ca-132">NOTES</span></span>

## <span data-ttu-id="554ca-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="554ca-133">RELATED LINKS</span></span>

[<span data-ttu-id="554ca-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="554ca-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="554ca-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="554ca-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="554ca-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="554ca-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
