---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610157"
---
# <span data-ttu-id="5378a-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5378a-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="5378a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5378a-102">SYNOPSIS</span></span>
<span data-ttu-id="5378a-103">Remove um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5378a-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5378a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5378a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5378a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5378a-105">DESCRIPTION</span></span>
<span data-ttu-id="5378a-106">O cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** remove um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5378a-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="5378a-107">Esta operação faz com que a duplicação pare para o item protegido.</span><span class="sxs-lookup"><span data-stu-id="5378a-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="5378a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5378a-108">EXAMPLES</span></span>

## <span data-ttu-id="5378a-109">OS</span><span class="sxs-lookup"><span data-stu-id="5378a-109">PARAMETERS</span></span>

### <span data-ttu-id="5378a-110">-Force</span><span class="sxs-lookup"><span data-stu-id="5378a-110">-Force</span></span>
<span data-ttu-id="5378a-111">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5378a-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5378a-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5378a-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5378a-113">Especifica o objeto de item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="5378a-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5378a-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5378a-114">-WaitForCompletion</span></span>
<span data-ttu-id="5378a-115">Indica que o cmdlet aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="5378a-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="5378a-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5378a-116">-Confirm</span></span>
<span data-ttu-id="5378a-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5378a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5378a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5378a-118">-WhatIf</span></span>
<span data-ttu-id="5378a-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5378a-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5378a-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5378a-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5378a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5378a-121">-DefaultProfile</span></span>
<span data-ttu-id="5378a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5378a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5378a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5378a-123">CommonParameters</span></span>
<span data-ttu-id="5378a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5378a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5378a-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5378a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5378a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5378a-126">INPUTS</span></span>

### <span data-ttu-id="5378a-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5378a-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="5378a-128">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5378a-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="5378a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5378a-129">OUTPUTS</span></span>

### <span data-ttu-id="5378a-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5378a-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5378a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5378a-131">NOTES</span></span>

## <span data-ttu-id="5378a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5378a-132">RELATED LINKS</span></span>

[<span data-ttu-id="5378a-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5378a-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="5378a-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5378a-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="5378a-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5378a-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
