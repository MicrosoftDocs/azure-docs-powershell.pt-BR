---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259889"
---
# <span data-ttu-id="29632-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="29632-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="29632-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29632-102">SYNOPSIS</span></span>
<span data-ttu-id="29632-103">Cria um mapeamento de rede ASR entre duas redes.</span><span class="sxs-lookup"><span data-stu-id="29632-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="29632-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29632-104">SYNTAX</span></span>

### <span data-ttu-id="29632-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="29632-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29632-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="29632-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29632-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="29632-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29632-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29632-108">DESCRIPTION</span></span>
<span data-ttu-id="29632-109">O cmdlet **New-AzRecoveryServicesAsrNetworkMapping** inicia a operação de criação de um mapeamento de rede ASR entre duas redes e retorna o objeto de trabalho ASR para o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="29632-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="29632-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29632-110">EXAMPLES</span></span>

### <span data-ttu-id="29632-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29632-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="29632-112">Inicia a operação de criação de mapeamento de rede usando o nome, as redes primárias e de recuperação especificadas e retorna um trabalho ASR para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="29632-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="29632-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29632-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="29632-114">Inicia o mapeamento de rede para a operação de criação usando o nome especificado, redes primárias e de recuperação e retorna um trabalho ASR para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="29632-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="29632-115">OS</span><span class="sxs-lookup"><span data-stu-id="29632-115">PARAMETERS</span></span>

### <span data-ttu-id="29632-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="29632-116">-AzureToAzure</span></span>
<span data-ttu-id="29632-117">Sinalizador para criar AzureToAzure cenário.</span><span class="sxs-lookup"><span data-stu-id="29632-117">Flag to create AzureToAzure scenario.</span></span>

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

### <span data-ttu-id="29632-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29632-118">-DefaultProfile</span></span>
<span data-ttu-id="29632-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29632-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="29632-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="29632-120">-Name</span></span>
<span data-ttu-id="29632-121">Nome do mapeamento de rede ASR a ser criado.</span><span class="sxs-lookup"><span data-stu-id="29632-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="29632-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="29632-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="29632-123">Especifica a ID de rede virtual do Azure da rede principal para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="29632-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="29632-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="29632-124">-PrimaryFabric</span></span>
<span data-ttu-id="29632-125">Especifica a malha ASR na qual o mapeamento deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="29632-125">Specifies the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="29632-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="29632-126">-PrimaryNetwork</span></span>
<span data-ttu-id="29632-127">Especifica o objeto de rede principal para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="29632-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="29632-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="29632-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="29632-129">Especifica a ID de rede de recuperação do Azure para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="29632-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="29632-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="29632-130">-RecoveryFabric</span></span>
<span data-ttu-id="29632-131">O objeto de malha do Azure site Recovery correspondente à região de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="29632-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="29632-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="29632-132">-RecoveryNetwork</span></span>
<span data-ttu-id="29632-133">Especifica o objeto de rede de recuperação para o mapeamento de rede ASR.</span><span class="sxs-lookup"><span data-stu-id="29632-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="29632-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29632-134">-Confirm</span></span>
<span data-ttu-id="29632-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29632-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29632-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29632-136">-WhatIf</span></span>
<span data-ttu-id="29632-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29632-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29632-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29632-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29632-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29632-139">CommonParameters</span></span>
<span data-ttu-id="29632-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29632-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29632-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29632-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29632-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29632-142">INPUTS</span></span>

### <span data-ttu-id="29632-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="29632-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="29632-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29632-144">OUTPUTS</span></span>

### <span data-ttu-id="29632-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="29632-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29632-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29632-146">NOTES</span></span>

## <span data-ttu-id="29632-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29632-147">RELATED LINKS</span></span>

[<span data-ttu-id="29632-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="29632-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="29632-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="29632-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
