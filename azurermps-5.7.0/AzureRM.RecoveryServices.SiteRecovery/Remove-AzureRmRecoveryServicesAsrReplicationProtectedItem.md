---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1df32bfcf049346b3f434b252a413eef020d0b77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429735"
---
# <span data-ttu-id="e81b4-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e81b4-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="e81b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e81b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e81b4-103">Interrompe/desabilita a replicação de um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e81b4-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e81b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e81b4-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e81b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e81b4-105">DESCRIPTION</span></span>
<span data-ttu-id="e81b4-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** desabilita a replicação do item de replicação do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="e81b4-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="e81b4-107">Esta operação faz com que a duplicação pare para o item protegido.</span><span class="sxs-lookup"><span data-stu-id="e81b4-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="e81b4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e81b4-108">EXAMPLES</span></span>

### <span data-ttu-id="e81b4-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e81b4-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="e81b4-110">Inicia a operação de desabilitação de replicação para o item protegido de replicação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="e81b4-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e81b4-111">OS</span><span class="sxs-lookup"><span data-stu-id="e81b4-111">PARAMETERS</span></span>

### <span data-ttu-id="e81b4-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e81b4-112">-Confirm</span></span>
<span data-ttu-id="e81b4-113">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="e81b4-113">Specify if confirmation is required.</span></span> <span data-ttu-id="e81b4-114">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="e81b4-114">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81b4-115">-DefaultProfile</span></span>
<span data-ttu-id="e81b4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e81b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e81b4-117">-Force</span></span>
<span data-ttu-id="e81b4-118">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="e81b4-118">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e81b4-119">-InputObject</span></span>
<span data-ttu-id="e81b4-120">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao item protegido de replicação para o qual a replicação será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e81b4-120">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e81b4-121">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e81b4-121">-WaitForCompletion</span></span>
<span data-ttu-id="e81b4-122">Indica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="e81b4-122">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81b4-123">-WhatIf</span></span>
<span data-ttu-id="e81b4-124">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81b4-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81b4-125">CommonParameters</span></span>
<span data-ttu-id="e81b4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81b4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81b4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81b4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e81b4-128">INPUTS</span></span>

### <span data-ttu-id="e81b4-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e81b4-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e81b4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e81b4-130">OUTPUTS</span></span>

### <span data-ttu-id="e81b4-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e81b4-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e81b4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e81b4-132">NOTES</span></span>

## <span data-ttu-id="e81b4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e81b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="e81b4-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e81b4-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e81b4-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e81b4-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e81b4-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e81b4-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
