---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114029"
---
# <span data-ttu-id="a8c82-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a8c82-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a8c82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8c82-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c82-103">Atualiza o mapeamento de rede de recuperação de site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="a8c82-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="a8c82-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8c82-104">SYNTAX</span></span>

### <span data-ttu-id="a8c82-105">ByNetworkObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a8c82-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c82-106">ById</span><span class="sxs-lookup"><span data-stu-id="a8c82-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8c82-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8c82-107">DESCRIPTION</span></span>
<span data-ttu-id="a8c82-108">O cmdlet **Update-AzRecoveryServicesAsrNetWorkMapping** atualiza o mapeamento de rede de Recuperação de Site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="a8c82-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="a8c82-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8c82-109">EXAMPLES</span></span>

### <span data-ttu-id="a8c82-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8c82-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="a8c82-111">Inicia a operação de mapeamento de rede de atualização usando os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="a8c82-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a8c82-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8c82-112">PARAMETERS</span></span>

### <span data-ttu-id="a8c82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c82-113">-DefaultProfile</span></span>
<span data-ttu-id="a8c82-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a8c82-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8c82-115">-InputObject</span></span>
<span data-ttu-id="a8c82-116">Objeto de entrada: especifica o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a8c82-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="a8c82-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="a8c82-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a8c82-118">Especifica a ID de rede do Azure de recuperação para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="a8c82-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="a8c82-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a8c82-119">-RecoveryNetwork</span></span>
<span data-ttu-id="a8c82-120">Especifica o objeto de rede de recuperação para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="a8c82-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="a8c82-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a8c82-121">-Confirm</span></span>
<span data-ttu-id="a8c82-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8c82-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8c82-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8c82-123">-WhatIf</span></span>
<span data-ttu-id="a8c82-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a8c82-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8c82-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8c82-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8c82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c82-126">CommonParameters</span></span>
<span data-ttu-id="a8c82-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c82-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8c82-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c82-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="a8c82-129">INPUTS</span></span>

### <span data-ttu-id="a8c82-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a8c82-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="a8c82-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="a8c82-131">OUTPUTS</span></span>

### <span data-ttu-id="a8c82-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a8c82-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a8c82-133">Notas</span><span class="sxs-lookup"><span data-stu-id="a8c82-133">NOTES</span></span>

## <span data-ttu-id="a8c82-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8c82-134">RELATED LINKS</span></span>
