---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885975"
---
# <span data-ttu-id="ec055-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ec055-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="ec055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec055-102">SYNOPSIS</span></span>
<span data-ttu-id="ec055-103">Cria um Contêiner de Proteção de Recuperação de Site do Azure dentro do tecido especificado.</span><span class="sxs-lookup"><span data-stu-id="ec055-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="ec055-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec055-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec055-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec055-105">DESCRIPTION</span></span>
<span data-ttu-id="ec055-106">O New-AzRecoveryServicesAsrProtectionContainer cmdlet cria um Contêiner de Proteção no Azure Site Recovery Fabric especificado.</span><span class="sxs-lookup"><span data-stu-id="ec055-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="ec055-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec055-107">EXAMPLES</span></span>

### <span data-ttu-id="ec055-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec055-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="ec055-109">Inicia a criação do contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="ec055-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ec055-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec055-110">PARAMETERS</span></span>

### <span data-ttu-id="ec055-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec055-111">-DefaultProfile</span></span>
<span data-ttu-id="ec055-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec055-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec055-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec055-113">-InputObject</span></span>
<span data-ttu-id="ec055-114">Cria o contêiner de proteção de replicação no Objeto de entrada especificado (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="ec055-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec055-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ec055-115">-Name</span></span>
<span data-ttu-id="ec055-116">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="ec055-116">Name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec055-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec055-117">-Confirm</span></span>
<span data-ttu-id="ec055-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec055-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec055-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec055-119">-WhatIf</span></span>
<span data-ttu-id="ec055-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec055-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec055-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec055-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec055-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec055-122">CommonParameters</span></span>
<span data-ttu-id="ec055-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec055-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec055-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec055-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec055-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec055-125">INPUTS</span></span>

### <span data-ttu-id="ec055-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ec055-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ec055-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec055-127">OUTPUTS</span></span>

### <span data-ttu-id="ec055-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ec055-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ec055-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec055-129">NOTES</span></span>

## <span data-ttu-id="ec055-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec055-130">RELATED LINKS</span></span>
