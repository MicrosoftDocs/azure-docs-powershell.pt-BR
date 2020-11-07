---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 0af3ffc25571273ebe572ee315b4e3c97de8f116
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772980"
---
# <span data-ttu-id="031fd-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="031fd-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="031fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="031fd-102">SYNOPSIS</span></span>
<span data-ttu-id="031fd-103">Cria um mapeamento de rede ASR entre duas redes.</span><span class="sxs-lookup"><span data-stu-id="031fd-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="031fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="031fd-104">SYNTAX</span></span>

### <span data-ttu-id="031fd-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="031fd-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="031fd-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="031fd-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="031fd-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="031fd-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="031fd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="031fd-108">DESCRIPTION</span></span>
<span data-ttu-id="031fd-109">O cmdlet **New-AzRecoveryServicesAsrNetworkMapping** inicia a operação de criação de um mapeamento de rede ASR entre duas redes e retorna o objeto de trabalho ASR para o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="031fd-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="031fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="031fd-110">EXAMPLES</span></span>

### <span data-ttu-id="031fd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="031fd-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="031fd-112">Inicia a operação de criação de mapeamento de rede usando o nome, as redes primárias e de recuperação especificadas e retorna um trabalho ASR para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="031fd-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="031fd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="031fd-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="031fd-114">Inicia o mapeamento de rede para a operação de criação usando o nome especificado, redes primárias e de recuperação e retorna um trabalho ASR para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="031fd-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="031fd-115">OS</span><span class="sxs-lookup"><span data-stu-id="031fd-115">PARAMETERS</span></span>

### <span data-ttu-id="031fd-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="031fd-116">-AzureToAzure</span></span>
<span data-ttu-id="031fd-117">{{Fill AzureToAzure descrição}}</span><span class="sxs-lookup"><span data-stu-id="031fd-117">{{Fill AzureToAzure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031fd-118">-DefaultProfile</span></span>
<span data-ttu-id="031fd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="031fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="031fd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="031fd-120">-Name</span></span>
<span data-ttu-id="031fd-121">Nome do mapeamento de rede ASR a ser criado.</span><span class="sxs-lookup"><span data-stu-id="031fd-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="031fd-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="031fd-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="031fd-123">Especifica a ID de rede virtual do Azure da rede principal para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="031fd-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="031fd-124">-PrimaryFabric</span></span>
<span data-ttu-id="031fd-125">Especifica a malha ASR na qual o mapeamento deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="031fd-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="031fd-126">-PrimaryNetwork</span></span>
<span data-ttu-id="031fd-127">Especifica o objeto de rede principal para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="031fd-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="031fd-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="031fd-129">Especifica a ID de rede de recuperação do Azure para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="031fd-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="031fd-130">-RecoveryFabric</span></span>
<span data-ttu-id="031fd-131">O objeto de malha do Azure site Recovery correspondente à região de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="031fd-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="031fd-132">-RecoveryNetwork</span></span>
<span data-ttu-id="031fd-133">Especifica o objeto de rede de recuperação para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="031fd-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031fd-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="031fd-134">-Confirm</span></span>
<span data-ttu-id="031fd-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="031fd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="031fd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="031fd-136">-WhatIf</span></span>
<span data-ttu-id="031fd-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="031fd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="031fd-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="031fd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="031fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031fd-139">CommonParameters</span></span>
<span data-ttu-id="031fd-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="031fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031fd-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="031fd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031fd-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="031fd-142">INPUTS</span></span>

### <span data-ttu-id="031fd-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="031fd-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="031fd-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="031fd-144">OUTPUTS</span></span>

### <span data-ttu-id="031fd-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="031fd-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="031fd-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="031fd-146">NOTES</span></span>

## <span data-ttu-id="031fd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="031fd-147">RELATED LINKS</span></span>

[<span data-ttu-id="031fd-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="031fd-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="031fd-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="031fd-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)