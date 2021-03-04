---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: bfea43fb0f27aff6405159c0174a698d9dc2298e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892044"
---
# <span data-ttu-id="143d7-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="143d7-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="143d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="143d7-102">SYNOPSIS</span></span>
<span data-ttu-id="143d7-103">Cria um Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="143d7-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="143d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="143d7-104">SYNTAX</span></span>

### <span data-ttu-id="143d7-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="143d7-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="143d7-106">Azure</span><span class="sxs-lookup"><span data-stu-id="143d7-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="143d7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="143d7-107">DESCRIPTION</span></span>
<span data-ttu-id="143d7-108">O cmdlet **New-AzRecoveryServicesAsrFabric** cria um Azure Site Recovery Fabric do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="143d7-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="143d7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="143d7-109">EXAMPLES</span></span>

### <span data-ttu-id="143d7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="143d7-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="143d7-111">Inicia a criação de malha com o nome passado e retorna o trabalho ASR usado para rastrear a operação de criação de malha.</span><span class="sxs-lookup"><span data-stu-id="143d7-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="143d7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="143d7-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="143d7-113">Inicia a criação do azure fabric com o nome passado e retorna o trabalho ASR usado para rastrear a operação de criação de malha.</span><span class="sxs-lookup"><span data-stu-id="143d7-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="143d7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="143d7-114">PARAMETERS</span></span>

### <span data-ttu-id="143d7-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="143d7-115">-Azure</span></span>
<span data-ttu-id="143d7-116">O parâmetro Switch especifica a criação do azure fabric.</span><span class="sxs-lookup"><span data-stu-id="143d7-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143d7-117">-DefaultProfile</span></span>
<span data-ttu-id="143d7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="143d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="143d7-119">-Location</span><span class="sxs-lookup"><span data-stu-id="143d7-119">-Location</span></span>
<span data-ttu-id="143d7-120">Especifica a região do Azure correspondente ao objeto Fabric que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="143d7-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="143d7-121">O objeto de malha recuperação de site do Azure representa uma região.</span><span class="sxs-lookup"><span data-stu-id="143d7-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="143d7-122">Para máquinas virtuais que estão sendo replicadas entre duas regiões do Azure, uma malha primária representa a região primária do Azure e a malha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="143d7-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143d7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="143d7-123">-Name</span></span>
<span data-ttu-id="143d7-124">Especifica o nome do Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="143d7-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="143d7-125">-Type</span><span class="sxs-lookup"><span data-stu-id="143d7-125">-Type</span></span>
<span data-ttu-id="143d7-126">Especifica o Tipo de Malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="143d7-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143d7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="143d7-127">-Confirm</span></span>
<span data-ttu-id="143d7-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="143d7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="143d7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="143d7-129">-WhatIf</span></span>
<span data-ttu-id="143d7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="143d7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="143d7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="143d7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="143d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143d7-132">CommonParameters</span></span>
<span data-ttu-id="143d7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="143d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143d7-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="143d7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143d7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="143d7-135">INPUTS</span></span>

### <span data-ttu-id="143d7-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="143d7-136">None</span></span>

## <span data-ttu-id="143d7-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="143d7-137">OUTPUTS</span></span>

### <span data-ttu-id="143d7-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="143d7-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="143d7-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="143d7-139">NOTES</span></span>

## <span data-ttu-id="143d7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="143d7-140">RELATED LINKS</span></span>

[<span data-ttu-id="143d7-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="143d7-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="143d7-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="143d7-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
