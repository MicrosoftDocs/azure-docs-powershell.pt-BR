---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 248cbd6f94a95a0024b9fb72c6a2d8dd896eb0f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773132"
---
# <span data-ttu-id="02557-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="02557-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="02557-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02557-102">SYNOPSIS</span></span>
<span data-ttu-id="02557-103">Cria um contêiner de proteção do Azure site Recovery dentro da malha especificada.</span><span class="sxs-lookup"><span data-stu-id="02557-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="02557-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02557-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02557-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02557-105">DESCRIPTION</span></span>
<span data-ttu-id="02557-106">O cmdlet New-AzRecoveryServicesAsrProtectionContainer cria um contêiner de proteção na malha especificada do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="02557-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="02557-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02557-107">EXAMPLES</span></span>

### <span data-ttu-id="02557-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02557-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="02557-109">Inicia a criação do contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="02557-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="02557-110">OS</span><span class="sxs-lookup"><span data-stu-id="02557-110">PARAMETERS</span></span>

### <span data-ttu-id="02557-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02557-111">-DefaultProfile</span></span>
<span data-ttu-id="02557-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02557-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02557-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02557-113">-InputObject</span></span>
<span data-ttu-id="02557-114">Cria o contêiner de proteção de replicação no objeto de entrada especificado (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="02557-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="02557-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="02557-115">-Name</span></span>
<span data-ttu-id="02557-116">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="02557-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="02557-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02557-117">-Confirm</span></span>
<span data-ttu-id="02557-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02557-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02557-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02557-119">-WhatIf</span></span>
<span data-ttu-id="02557-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02557-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02557-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02557-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02557-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02557-122">CommonParameters</span></span>
<span data-ttu-id="02557-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02557-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02557-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02557-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02557-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02557-125">INPUTS</span></span>

### <span data-ttu-id="02557-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="02557-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="02557-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02557-127">OUTPUTS</span></span>

### <span data-ttu-id="02557-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="02557-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="02557-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02557-129">NOTES</span></span>

## <span data-ttu-id="02557-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02557-130">RELATED LINKS</span></span>