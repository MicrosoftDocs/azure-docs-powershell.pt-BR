---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431646"
---
# <span data-ttu-id="8fb93-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="8fb93-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="8fb93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fb93-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb93-103">Cria um mapeamento de rede ASR entre duas redes.</span><span class="sxs-lookup"><span data-stu-id="8fb93-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fb93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fb93-104">SYNTAX</span></span>

### <span data-ttu-id="8fb93-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="8fb93-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8fb93-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8fb93-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fb93-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8fb93-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fb93-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fb93-108">DESCRIPTION</span></span>
<span data-ttu-id="8fb93-109">O cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** inicia a operação de criação de um mapeamento de rede ASR entre duas redes e retorna o objeto de trabalho ASR para o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8fb93-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8fb93-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fb93-110">EXAMPLES</span></span>

### <span data-ttu-id="8fb93-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8fb93-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="8fb93-112">Inicia a operação de criação de mapeamento de rede usando o nome, as redes primárias e de recuperação especificadas e retorna um trabalho ASR para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8fb93-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="8fb93-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8fb93-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="8fb93-114">Inicia o mapeamento de rede para a operação de criação usando o nome especificado, redes primárias e de recuperação e retorna um trabalho ASR para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="8fb93-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="8fb93-115">OS</span><span class="sxs-lookup"><span data-stu-id="8fb93-115">PARAMETERS</span></span>

### <span data-ttu-id="8fb93-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8fb93-116">-AzureToAzure</span></span>
<span data-ttu-id="8fb93-117">Parâmetro de alternância especificando que o mapeamento de rede que está sendo criado será usado para replicar máquinas virtuais do Azure entre duas regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb93-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8fb93-118">-Confirm</span></span>
<span data-ttu-id="8fb93-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fb93-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb93-120">-DefaultProfile</span></span>
<span data-ttu-id="8fb93-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb93-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8fb93-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fb93-122">-Name</span></span>
<span data-ttu-id="8fb93-123">Nome do mapeamento de rede ASR a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8fb93-123">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-124">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="8fb93-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="8fb93-125">Especifica a ID de rede virtual do Azure da rede principal para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="8fb93-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="8fb93-126">-PrimaryFabric</span></span>
<span data-ttu-id="8fb93-127">Especifica a malha ASR na qual o mapeamento deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="8fb93-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="8fb93-128">-PrimaryNetwork</span></span>
<span data-ttu-id="8fb93-129">Especifica o objeto de rede principal para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="8fb93-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-130">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="8fb93-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="8fb93-131">Especifica a ID de rede de recuperação do Azure para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="8fb93-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8fb93-132">-RecoveryFabric</span></span>
<span data-ttu-id="8fb93-133">O objeto de malha do Azure site Recovery correspondente à região de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb93-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="8fb93-134">-RecoveryNetwork</span></span>
<span data-ttu-id="8fb93-135">Especifica o objeto de rede de recuperação para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="8fb93-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fb93-136">-WhatIf</span></span>
<span data-ttu-id="8fb93-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fb93-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fb93-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fb93-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb93-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb93-139">CommonParameters</span></span>
<span data-ttu-id="8fb93-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb93-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb93-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb93-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb93-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fb93-142">INPUTS</span></span>

### <span data-ttu-id="8fb93-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="8fb93-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="8fb93-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fb93-144">OUTPUTS</span></span>

### <span data-ttu-id="8fb93-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8fb93-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8fb93-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fb93-146">NOTES</span></span>

## <span data-ttu-id="8fb93-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fb93-147">RELATED LINKS</span></span>

[<span data-ttu-id="8fb93-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="8fb93-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="8fb93-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="8fb93-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
