---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e9aadbc8eae9703340043dc640f4cb9759b919d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601958"
---
# <span data-ttu-id="8ac10-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="8ac10-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="8ac10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ac10-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac10-103">Cria um mapeamento de rede ASR entre duas redes.</span><span class="sxs-lookup"><span data-stu-id="8ac10-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ac10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ac10-104">SYNTAX</span></span>

### <span data-ttu-id="8ac10-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ac10-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ac10-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8ac10-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac10-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8ac10-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ac10-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ac10-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac10-109">O cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** inicia a operação de criação de um mapeamento de rede ASR entre duas redes e retorna o objeto de trabalho ASR para o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8ac10-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8ac10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ac10-110">EXAMPLES</span></span>

### <span data-ttu-id="8ac10-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ac10-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="8ac10-112">Inicia a operação de criação de mapeamento de rede usando o nome, as redes primárias e de recuperação especificadas e retorna um trabalho ASR para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8ac10-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="8ac10-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8ac10-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="8ac10-114">Inicia o mapeamento de rede para a operação de criação usando o nome especificado, redes primárias e de recuperação e retorna um trabalho ASR para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="8ac10-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="8ac10-115">OS</span><span class="sxs-lookup"><span data-stu-id="8ac10-115">PARAMETERS</span></span>

### <span data-ttu-id="8ac10-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8ac10-116">-AzureToAzure</span></span>
<span data-ttu-id="8ac10-117">Parâmetro de alternância especificando que o mapeamento de rede que está sendo criado será usado para replicar máquinas virtuais do Azure entre duas regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac10-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="8ac10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac10-118">-DefaultProfile</span></span>
<span data-ttu-id="8ac10-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac10-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ac10-120">-Name</span></span>
<span data-ttu-id="8ac10-121">Nome do mapeamento de rede ASR a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8ac10-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="8ac10-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="8ac10-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="8ac10-123">Especifica a ID de rede virtual do Azure da rede principal para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="8ac10-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="8ac10-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="8ac10-124">-PrimaryFabric</span></span>
<span data-ttu-id="8ac10-125">Especifica a malha ASR na qual o mapeamento deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="8ac10-125">Specifes the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="8ac10-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="8ac10-126">-PrimaryNetwork</span></span>
<span data-ttu-id="8ac10-127">Especifica o objeto de rede principal para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="8ac10-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="8ac10-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="8ac10-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="8ac10-129">Especifica a ID de rede de recuperação do Azure para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="8ac10-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="8ac10-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="8ac10-130">-RecoveryFabric</span></span>
<span data-ttu-id="8ac10-131">O objeto de malha do Azure site Recovery correspondente à região de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac10-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="8ac10-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="8ac10-132">-RecoveryNetwork</span></span>
<span data-ttu-id="8ac10-133">Especifica o objeto de rede de recuperação para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="8ac10-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="8ac10-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ac10-134">-Confirm</span></span>
<span data-ttu-id="8ac10-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac10-136">-WhatIf</span></span>
<span data-ttu-id="8ac10-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ac10-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ac10-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ac10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac10-139">CommonParameters</span></span>
<span data-ttu-id="8ac10-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac10-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac10-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac10-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ac10-142">INPUTS</span></span>

### <span data-ttu-id="8ac10-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="8ac10-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="8ac10-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ac10-144">OUTPUTS</span></span>

### <span data-ttu-id="8ac10-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8ac10-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8ac10-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ac10-146">NOTES</span></span>

## <span data-ttu-id="8ac10-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ac10-147">RELATED LINKS</span></span>

[<span data-ttu-id="8ac10-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="8ac10-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="8ac10-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="8ac10-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
