---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427777"
---
# <span data-ttu-id="52259-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52259-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="52259-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52259-102">SYNOPSIS</span></span>
<span data-ttu-id="52259-103">Permite a replicação para um item que pode ser protegido criando um item protegido</span><span class="sxs-lookup"><span data-stu-id="52259-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52259-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52259-104">SYNTAX</span></span>

### <span data-ttu-id="52259-105">Desabilitador (padrão)</span><span class="sxs-lookup"><span data-stu-id="52259-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52259-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="52259-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52259-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="52259-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52259-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="52259-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52259-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52259-109">DESCRIPTION</span></span>
<span data-ttu-id="52259-110">O cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** cria um novo item de replicação protegida.</span><span class="sxs-lookup"><span data-stu-id="52259-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="52259-111">Use esse cmdlet para habilitar a replicação para um item que permite proteção.</span><span class="sxs-lookup"><span data-stu-id="52259-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="52259-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52259-112">EXAMPLES</span></span>

## <span data-ttu-id="52259-113">OS</span><span class="sxs-lookup"><span data-stu-id="52259-113">PARAMETERS</span></span>

### <span data-ttu-id="52259-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="52259-114">-Name</span></span>
<span data-ttu-id="52259-115">Especifica o nome do item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="52259-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-116">-OS</span><span class="sxs-lookup"><span data-stu-id="52259-116">-OS</span></span>
<span data-ttu-id="52259-117">Especifica a família do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52259-117">Specifies the operating system family.</span></span>
<span data-ttu-id="52259-118">Os valores aceitáveis para esse parâmetro são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="52259-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="52259-119">-OSDiskName</span></span>
<span data-ttu-id="52259-120">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52259-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="52259-121">-ProtectableItem</span></span>
<span data-ttu-id="52259-122">Especifica o item que protege o Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="52259-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52259-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="52259-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="52259-124">Especifica o objeto de mapeamento de contêiner de proteção do Azure site Recovery a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="52259-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="52259-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="52259-126">Especifica a ID da conta de armazenamento do Azure à qual esse cmdlet se replica.</span><span class="sxs-lookup"><span data-stu-id="52259-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="52259-127">-WaitForCompletion</span></span>
<span data-ttu-id="52259-128">Indica que o cmdlet aguarda a conclusão.</span><span class="sxs-lookup"><span data-stu-id="52259-128">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52259-129">-Confirm</span></span>
<span data-ttu-id="52259-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52259-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52259-131">-WhatIf</span></span>
<span data-ttu-id="52259-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52259-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="52259-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52259-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52259-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52259-134">-DefaultProfile</span></span>
<span data-ttu-id="52259-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52259-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52259-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52259-136">CommonParameters</span></span>
<span data-ttu-id="52259-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52259-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52259-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52259-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52259-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52259-139">INPUTS</span></span>

### <span data-ttu-id="52259-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="52259-140">ASRProtectableItem</span></span>
<span data-ttu-id="52259-141">O parâmetro ' ProtectableItem ' aceita o valor do tipo ' ASRProtectableItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="52259-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="52259-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52259-142">OUTPUTS</span></span>

### <span data-ttu-id="52259-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="52259-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="52259-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52259-144">NOTES</span></span>

## <span data-ttu-id="52259-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52259-145">RELATED LINKS</span></span>

[<span data-ttu-id="52259-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52259-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="52259-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52259-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="52259-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52259-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
