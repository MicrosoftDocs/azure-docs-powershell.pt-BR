---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116841"
---
# <span data-ttu-id="2efe8-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2efe8-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2efe8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2efe8-102">SYNOPSIS</span></span>
<span data-ttu-id="2efe8-103">Atualiza o mapeamento de rede do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="2efe8-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="2efe8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2efe8-104">SYNTAX</span></span>

### <span data-ttu-id="2efe8-105">ByNetworkObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="2efe8-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efe8-106">ById</span><span class="sxs-lookup"><span data-stu-id="2efe8-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2efe8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2efe8-107">DESCRIPTION</span></span>
<span data-ttu-id="2efe8-108">O cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** atualiza o mapeamento de rede do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="2efe8-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="2efe8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2efe8-109">EXAMPLES</span></span>

### <span data-ttu-id="2efe8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2efe8-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="2efe8-111">Inicia a operação atualizar mapeamento de rede usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="2efe8-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2efe8-112">OS</span><span class="sxs-lookup"><span data-stu-id="2efe8-112">PARAMETERS</span></span>

### <span data-ttu-id="2efe8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efe8-113">-DefaultProfile</span></span>
<span data-ttu-id="2efe8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2efe8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2efe8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2efe8-115">-InputObject</span></span>
<span data-ttu-id="2efe8-116">Objeto de entrada: especifica o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="2efe8-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2efe8-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="2efe8-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="2efe8-118">Especifica a ID de rede de recuperação do Azure para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="2efe8-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efe8-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="2efe8-119">-RecoveryNetwork</span></span>
<span data-ttu-id="2efe8-120">Especifica o objeto de rede de recuperação para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="2efe8-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efe8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2efe8-121">-Confirm</span></span>
<span data-ttu-id="2efe8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2efe8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2efe8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efe8-123">-WhatIf</span></span>
<span data-ttu-id="2efe8-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2efe8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2efe8-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2efe8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2efe8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efe8-126">CommonParameters</span></span>
<span data-ttu-id="2efe8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2efe8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efe8-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2efe8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efe8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2efe8-129">INPUTS</span></span>

### <span data-ttu-id="2efe8-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2efe8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="2efe8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2efe8-131">OUTPUTS</span></span>

### <span data-ttu-id="2efe8-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2efe8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2efe8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2efe8-133">NOTES</span></span>

## <span data-ttu-id="2efe8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2efe8-134">RELATED LINKS</span></span>
