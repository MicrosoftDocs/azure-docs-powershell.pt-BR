---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433379"
---
# <span data-ttu-id="55aec-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55aec-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="55aec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55aec-102">SYNOPSIS</span></span>
<span data-ttu-id="55aec-103">Remove um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="55aec-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55aec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55aec-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55aec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55aec-105">DESCRIPTION</span></span>
<span data-ttu-id="55aec-106">O cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** remove um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="55aec-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="55aec-107">Esta operação faz com que a duplicação pare para o item protegido.</span><span class="sxs-lookup"><span data-stu-id="55aec-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="55aec-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55aec-108">EXAMPLES</span></span>

## <span data-ttu-id="55aec-109">OS</span><span class="sxs-lookup"><span data-stu-id="55aec-109">PARAMETERS</span></span>

### <span data-ttu-id="55aec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55aec-110">-DefaultProfile</span></span>
<span data-ttu-id="55aec-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55aec-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55aec-112">-Force</span><span class="sxs-lookup"><span data-stu-id="55aec-112">-Force</span></span>
<span data-ttu-id="55aec-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="55aec-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55aec-114">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55aec-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="55aec-115">Especifica o objeto de item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="55aec-115">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="55aec-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="55aec-116">-WaitForCompletion</span></span>
<span data-ttu-id="55aec-117">Indica que o cmdlet aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="55aec-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="55aec-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55aec-118">-Confirm</span></span>
<span data-ttu-id="55aec-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55aec-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55aec-120">-WhatIf</span></span>
<span data-ttu-id="55aec-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55aec-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="55aec-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55aec-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55aec-123">CommonParameters</span></span>
<span data-ttu-id="55aec-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55aec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55aec-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55aec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55aec-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55aec-126">INPUTS</span></span>

### <span data-ttu-id="55aec-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55aec-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="55aec-128">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="55aec-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="55aec-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55aec-129">OUTPUTS</span></span>

### <span data-ttu-id="55aec-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="55aec-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="55aec-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55aec-131">NOTES</span></span>

## <span data-ttu-id="55aec-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55aec-132">RELATED LINKS</span></span>

[<span data-ttu-id="55aec-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55aec-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="55aec-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55aec-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="55aec-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55aec-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
