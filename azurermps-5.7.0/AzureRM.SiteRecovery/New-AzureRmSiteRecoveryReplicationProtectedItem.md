---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433384"
---
# <span data-ttu-id="e4577-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e4577-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="e4577-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4577-102">SYNOPSIS</span></span>
<span data-ttu-id="e4577-103">Permite a replicação para um item que pode ser protegido criando um item protegido</span><span class="sxs-lookup"><span data-stu-id="e4577-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4577-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4577-104">SYNTAX</span></span>

### <span data-ttu-id="e4577-105">Desabilitador (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4577-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4577-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e4577-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4577-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="e4577-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4577-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="e4577-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4577-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4577-109">DESCRIPTION</span></span>
<span data-ttu-id="e4577-110">O cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** cria um novo item de replicação protegida.</span><span class="sxs-lookup"><span data-stu-id="e4577-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="e4577-111">Use esse cmdlet para habilitar a replicação para um item que permite proteção.</span><span class="sxs-lookup"><span data-stu-id="e4577-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="e4577-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4577-112">EXAMPLES</span></span>

## <span data-ttu-id="e4577-113">OS</span><span class="sxs-lookup"><span data-stu-id="e4577-113">PARAMETERS</span></span>

### <span data-ttu-id="e4577-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4577-114">-DefaultProfile</span></span>
<span data-ttu-id="e4577-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4577-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4577-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4577-116">-Name</span></span>
<span data-ttu-id="e4577-117">Especifica o nome do item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e4577-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

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

### <span data-ttu-id="e4577-118">-OS</span><span class="sxs-lookup"><span data-stu-id="e4577-118">-OS</span></span>
<span data-ttu-id="e4577-119">Especifica a família do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e4577-119">Specifies the operating system family.</span></span>
<span data-ttu-id="e4577-120">Os valores aceitáveis para esse parâmetro são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="e4577-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="e4577-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="e4577-121">-OSDiskName</span></span>
<span data-ttu-id="e4577-122">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e4577-122">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="e4577-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e4577-123">-ProtectableItem</span></span>
<span data-ttu-id="e4577-124">Especifica o item que protege o Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e4577-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

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

### <span data-ttu-id="e4577-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e4577-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="e4577-126">Especifica o objeto de mapeamento de contêiner de proteção do Azure site Recovery a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="e4577-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

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

### <span data-ttu-id="e4577-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e4577-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e4577-128">Especifica a ID da conta de armazenamento do Azure à qual esse cmdlet se replica.</span><span class="sxs-lookup"><span data-stu-id="e4577-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

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

### <span data-ttu-id="e4577-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e4577-129">-WaitForCompletion</span></span>
<span data-ttu-id="e4577-130">Indica que o cmdlet aguarda a conclusão.</span><span class="sxs-lookup"><span data-stu-id="e4577-130">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="e4577-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4577-131">-Confirm</span></span>
<span data-ttu-id="e4577-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4577-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4577-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4577-133">-WhatIf</span></span>
<span data-ttu-id="e4577-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4577-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e4577-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4577-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4577-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4577-136">CommonParameters</span></span>
<span data-ttu-id="e4577-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4577-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4577-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4577-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4577-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4577-139">INPUTS</span></span>

### <span data-ttu-id="e4577-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e4577-140">ASRProtectableItem</span></span>
<span data-ttu-id="e4577-141">O parâmetro ' ProtectableItem ' aceita o valor do tipo ' ASRProtectableItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e4577-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="e4577-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4577-142">OUTPUTS</span></span>

### <span data-ttu-id="e4577-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e4577-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e4577-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4577-144">NOTES</span></span>

## <span data-ttu-id="e4577-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4577-145">RELATED LINKS</span></span>

[<span data-ttu-id="e4577-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e4577-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="e4577-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e4577-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="e4577-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e4577-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
