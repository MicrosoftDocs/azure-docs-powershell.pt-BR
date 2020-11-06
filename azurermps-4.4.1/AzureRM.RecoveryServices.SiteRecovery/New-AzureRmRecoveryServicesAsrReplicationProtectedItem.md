---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429160"
---
# <span data-ttu-id="bef65-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bef65-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="bef65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bef65-102">SYNOPSIS</span></span>
<span data-ttu-id="bef65-103">Permite a replicação de um item protegido contra ASR criando um item protegido de replicação</span><span class="sxs-lookup"><span data-stu-id="bef65-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bef65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bef65-104">SYNTAX</span></span>

### <span data-ttu-id="bef65-105">Desabilitador (padrão)</span><span class="sxs-lookup"><span data-stu-id="bef65-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bef65-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="bef65-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bef65-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="bef65-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bef65-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="bef65-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bef65-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bef65-109">DESCRIPTION</span></span>
<span data-ttu-id="bef65-110">O cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cria um novo item de replicação protegida.</span><span class="sxs-lookup"><span data-stu-id="bef65-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="bef65-111">Use esse cmdlet para habilitar a replicação para um item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="bef65-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="bef65-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bef65-112">EXAMPLES</span></span>

### <span data-ttu-id="bef65-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bef65-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="bef65-114">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="bef65-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bef65-115">OS</span><span class="sxs-lookup"><span data-stu-id="bef65-115">PARAMETERS</span></span>

### <span data-ttu-id="bef65-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bef65-116">-Name</span></span>
<span data-ttu-id="bef65-117">Especifica um nome para o item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="bef65-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-118">-OS</span><span class="sxs-lookup"><span data-stu-id="bef65-118">-OS</span></span>
<span data-ttu-id="bef65-119">Especifica a família do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bef65-119">Specifies the operating system family.</span></span>
<span data-ttu-id="bef65-120">Os valores aceitáveis para esse parâmetro são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="bef65-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="bef65-121">-OSDiskName</span></span>
<span data-ttu-id="bef65-122">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bef65-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bef65-123">-ProtectableItem</span></span>
<span data-ttu-id="bef65-124">Especifica o objeto de item protectable ASR para o qual a replicação está sendo habilitada.</span><span class="sxs-lookup"><span data-stu-id="bef65-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bef65-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="bef65-126">Especifica o objeto de mapeamento de contêiner de proteção ASR correspondente à política de replicação a ser usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="bef65-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bef65-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="bef65-128">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="bef65-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bef65-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="bef65-130">Especifica o identificador de braço do grupo de recursos no qual a máquina virtual será criada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="bef65-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="bef65-131">-WaitForCompletion</span></span>
<span data-ttu-id="bef65-132">Especifica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="bef65-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef65-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bef65-133">-Confirm</span></span>
<span data-ttu-id="bef65-134">Solicita confirmação antes de iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="bef65-134">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="bef65-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef65-135">-WhatIf</span></span>
<span data-ttu-id="bef65-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bef65-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bef65-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bef65-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef65-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef65-138">CommonParameters</span></span>
<span data-ttu-id="bef65-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef65-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef65-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef65-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef65-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bef65-141">INPUTS</span></span>

### <span data-ttu-id="bef65-142">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bef65-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="bef65-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bef65-143">OUTPUTS</span></span>

### <span data-ttu-id="bef65-144">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bef65-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bef65-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bef65-145">NOTES</span></span>

## <span data-ttu-id="bef65-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bef65-146">RELATED LINKS</span></span>

[<span data-ttu-id="bef65-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bef65-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="bef65-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bef65-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="bef65-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bef65-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
