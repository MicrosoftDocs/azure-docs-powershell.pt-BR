---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113371"
---
# <span data-ttu-id="5789f-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5789f-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="5789f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5789f-102">SYNOPSIS</span></span>
<span data-ttu-id="5789f-103">Cria um Contêiner de Proteção de Recuperação de Site do Azure dentro da malha especificada.</span><span class="sxs-lookup"><span data-stu-id="5789f-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="5789f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5789f-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5789f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5789f-105">DESCRIPTION</span></span>
<span data-ttu-id="5789f-106">O New-AzRecoveryServicesAsrProtectionContainer cmdlet cria um Contêiner de Proteção sob a Malha de Recuperação de Site do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="5789f-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="5789f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5789f-107">EXAMPLES</span></span>

### <span data-ttu-id="5789f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5789f-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="5789f-109">Inicia a criação do contêiner de proteção com os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="5789f-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5789f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5789f-110">PARAMETERS</span></span>

### <span data-ttu-id="5789f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5789f-111">-DefaultProfile</span></span>
<span data-ttu-id="5789f-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5789f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5789f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5789f-113">-InputObject</span></span>
<span data-ttu-id="5789f-114">Cria o contêiner de proteção de replicação no Objeto de entrada especificado (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="5789f-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="5789f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5789f-115">-Name</span></span>
<span data-ttu-id="5789f-116">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="5789f-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="5789f-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5789f-117">-Confirm</span></span>
<span data-ttu-id="5789f-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5789f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5789f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5789f-119">-WhatIf</span></span>
<span data-ttu-id="5789f-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5789f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5789f-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5789f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5789f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5789f-122">CommonParameters</span></span>
<span data-ttu-id="5789f-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5789f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5789f-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5789f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5789f-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="5789f-125">INPUTS</span></span>

### <span data-ttu-id="5789f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5789f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5789f-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="5789f-127">OUTPUTS</span></span>

### <span data-ttu-id="5789f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5789f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5789f-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5789f-129">NOTES</span></span>

## <span data-ttu-id="5789f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5789f-130">RELATED LINKS</span></span>
