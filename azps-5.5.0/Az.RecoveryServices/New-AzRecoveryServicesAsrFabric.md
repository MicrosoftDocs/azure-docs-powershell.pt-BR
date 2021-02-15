---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114939"
---
# <span data-ttu-id="5d6c6-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5d6c6-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="5d6c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6c6-103">Cria uma malha de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="5d6c6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d6c6-104">SYNTAX</span></span>

### <span data-ttu-id="5d6c6-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5d6c6-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d6c6-106">Azure</span><span class="sxs-lookup"><span data-stu-id="5d6c6-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d6c6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d6c6-107">DESCRIPTION</span></span>
<span data-ttu-id="5d6c6-108">O cmdlet **New-AzRecoveryServicesAsrFabric** cria uma Malha de Recuperação de Site do Azure do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="5d6c6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d6c6-109">EXAMPLES</span></span>

### <span data-ttu-id="5d6c6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d6c6-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="5d6c6-111">Inicia a criação de malha com o nome passado e retorna o trabalho ASR usado para controlar a operação de criação de malha.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="5d6c6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5d6c6-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="5d6c6-113">Inicia a criação de malha do azure com o nome passado e retorna o trabalho ASR usado para controlar a operação de criação de malha.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="5d6c6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d6c6-114">PARAMETERS</span></span>

### <span data-ttu-id="5d6c6-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="5d6c6-115">-Azure</span></span>
<span data-ttu-id="5d6c6-116">Alternar parâmetro especifica para criar uma malha azure.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="5d6c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6c6-117">-DefaultProfile</span></span>
<span data-ttu-id="5d6c6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5d6c6-119">-Local</span><span class="sxs-lookup"><span data-stu-id="5d6c6-119">-Location</span></span>
<span data-ttu-id="5d6c6-120">Especifica a região do Azure correspondente ao objeto De malha que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="5d6c6-121">O objeto de malha recuperação do site do Azure representa uma região.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="5d6c6-122">Para máquinas virtuais que estão sendo replicadas entre duas regiões do Azure, uma malha primária representa a região principal do Azure e a malha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="5d6c6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d6c6-123">-Name</span></span>
<span data-ttu-id="5d6c6-124">Especifica o nome da Malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="5d6c6-125">-Tipo</span><span class="sxs-lookup"><span data-stu-id="5d6c6-125">-Type</span></span>
<span data-ttu-id="5d6c6-126">Especifica o Tipo de Malha de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="5d6c6-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5d6c6-127">-Confirm</span></span>
<span data-ttu-id="5d6c6-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d6c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d6c6-129">-WhatIf</span></span>
<span data-ttu-id="5d6c6-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d6c6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d6c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6c6-132">CommonParameters</span></span>
<span data-ttu-id="5d6c6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6c6-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d6c6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6c6-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="5d6c6-135">INPUTS</span></span>

### <span data-ttu-id="5d6c6-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5d6c6-136">None</span></span>

## <span data-ttu-id="5d6c6-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="5d6c6-137">OUTPUTS</span></span>

### <span data-ttu-id="5d6c6-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5d6c6-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5d6c6-139">Notas</span><span class="sxs-lookup"><span data-stu-id="5d6c6-139">NOTES</span></span>

## <span data-ttu-id="5d6c6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d6c6-140">RELATED LINKS</span></span>

[<span data-ttu-id="5d6c6-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5d6c6-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="5d6c6-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="5d6c6-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
