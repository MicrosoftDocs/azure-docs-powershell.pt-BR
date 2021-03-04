---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 6041973d4bab91310ed213d461cf97db9cc5e720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890736"
---
# <span data-ttu-id="b77ed-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b77ed-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b77ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b77ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b77ed-103">Atualiza o mapeamento de rede de recuperação de site do azure especificado.</span><span class="sxs-lookup"><span data-stu-id="b77ed-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="b77ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b77ed-104">SYNTAX</span></span>

### <span data-ttu-id="b77ed-105">ByNetworkObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b77ed-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77ed-106">ById</span><span class="sxs-lookup"><span data-stu-id="b77ed-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77ed-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b77ed-107">DESCRIPTION</span></span>
<span data-ttu-id="b77ed-108">O cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** atualiza o mapeamento de rede de Recuperação de Site especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="b77ed-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="b77ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b77ed-109">EXAMPLES</span></span>

### <span data-ttu-id="b77ed-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b77ed-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="b77ed-111">Inicia a operação de mapeamento de rede de atualização usando os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="b77ed-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b77ed-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b77ed-112">PARAMETERS</span></span>

### <span data-ttu-id="b77ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77ed-113">-DefaultProfile</span></span>
<span data-ttu-id="b77ed-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b77ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b77ed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b77ed-115">-InputObject</span></span>
<span data-ttu-id="b77ed-116">Objeto Input: especifica o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="b77ed-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="b77ed-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="b77ed-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="b77ed-118">Especifica a ID de rede do azure de recuperação para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="b77ed-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="b77ed-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="b77ed-119">-RecoveryNetwork</span></span>
<span data-ttu-id="b77ed-120">Especifica o objeto de rede de recuperação para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="b77ed-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="b77ed-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b77ed-121">-Confirm</span></span>
<span data-ttu-id="b77ed-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b77ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77ed-123">-WhatIf</span></span>
<span data-ttu-id="b77ed-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b77ed-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b77ed-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b77ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77ed-126">CommonParameters</span></span>
<span data-ttu-id="b77ed-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77ed-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b77ed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77ed-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b77ed-129">INPUTS</span></span>

### <span data-ttu-id="b77ed-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b77ed-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="b77ed-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b77ed-131">OUTPUTS</span></span>

### <span data-ttu-id="b77ed-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b77ed-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b77ed-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="b77ed-133">NOTES</span></span>

## <span data-ttu-id="b77ed-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b77ed-134">RELATED LINKS</span></span>
