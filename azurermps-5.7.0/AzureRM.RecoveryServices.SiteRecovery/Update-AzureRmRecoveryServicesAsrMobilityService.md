---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: de9e07da334e252db4af87819d2719b5251b576c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426640"
---
# <span data-ttu-id="3adb1-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="3adb1-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="3adb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3adb1-102">SYNOPSIS</span></span>
<span data-ttu-id="3adb1-103">Atualizações do agente de serviço de mobilidade por push para computadores protegidos.</span><span class="sxs-lookup"><span data-stu-id="3adb1-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3adb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3adb1-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3adb1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3adb1-105">DESCRIPTION</span></span>
<span data-ttu-id="3adb1-106">O cmdlet **Update-AzureRmRecoveryServicesAsrMobilityService** tenta enviar por push atualizações de agente de serviço de mobilidade para computadores protegidos (se houver uma atualização disponível.)</span><span class="sxs-lookup"><span data-stu-id="3adb1-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="3adb1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3adb1-107">EXAMPLES</span></span>

### <span data-ttu-id="3adb1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3adb1-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="3adb1-109">Trabalho para acompanhar o agente de serviço do item Moblility protegido de replicação de atualização.</span><span class="sxs-lookup"><span data-stu-id="3adb1-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="3adb1-110">OS</span><span class="sxs-lookup"><span data-stu-id="3adb1-110">PARAMETERS</span></span>

### <span data-ttu-id="3adb1-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="3adb1-111">-Account</span></span>
<span data-ttu-id="3adb1-112">A ID da conta Executar como a ser usada para enviar a atualização.</span><span class="sxs-lookup"><span data-stu-id="3adb1-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="3adb1-113">Deve ser um na lista de contas Executar como da malha ASR correspondente ao computador que está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="3adb1-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adb1-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3adb1-114">-Confirm</span></span>
<span data-ttu-id="3adb1-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3adb1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3adb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3adb1-116">-DefaultProfile</span></span>
<span data-ttu-id="3adb1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3adb1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3adb1-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3adb1-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3adb1-119">Item protegido de replicação do Azure site Recovery a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3adb1-119">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3adb1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3adb1-120">-WhatIf</span></span>
<span data-ttu-id="3adb1-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3adb1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3adb1-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3adb1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3adb1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adb1-123">CommonParameters</span></span>
<span data-ttu-id="3adb1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adb1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adb1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3adb1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adb1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3adb1-126">INPUTS</span></span>

### <span data-ttu-id="3adb1-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3adb1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3adb1-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3adb1-128">OUTPUTS</span></span>

### <span data-ttu-id="3adb1-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3adb1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3adb1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3adb1-130">NOTES</span></span>

## <span data-ttu-id="3adb1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3adb1-131">RELATED LINKS</span></span>
