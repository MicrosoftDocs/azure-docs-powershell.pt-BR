---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603309"
---
# <span data-ttu-id="f81ce-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f81ce-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="f81ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f81ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f81ce-103">Define o estado de uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f81ce-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f81ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f81ce-104">SYNTAX</span></span>

### <span data-ttu-id="f81ce-105">Desabilitador (padrão)</span><span class="sxs-lookup"><span data-stu-id="f81ce-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f81ce-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f81ce-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f81ce-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f81ce-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f81ce-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="f81ce-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f81ce-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f81ce-109">DESCRIPTION</span></span>
<span data-ttu-id="f81ce-110">O cmdlet **set-AzureRmSiteRecoveryProtectionEntity** habilita ou desabilita a proteção em uma entidade de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f81ce-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="f81ce-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f81ce-111">EXAMPLES</span></span>

## <span data-ttu-id="f81ce-112">OS</span><span class="sxs-lookup"><span data-stu-id="f81ce-112">PARAMETERS</span></span>

### <span data-ttu-id="f81ce-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f81ce-113">-Force</span></span>
<span data-ttu-id="f81ce-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f81ce-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f81ce-115">-OS</span><span class="sxs-lookup"><span data-stu-id="f81ce-115">-OS</span></span>
<span data-ttu-id="f81ce-116">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f81ce-116">Specifies the operating system type.</span></span>
<span data-ttu-id="f81ce-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f81ce-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f81ce-118">Windows</span><span class="sxs-lookup"><span data-stu-id="f81ce-118">Windows</span></span>
- <span data-ttu-id="f81ce-119">Linux</span><span class="sxs-lookup"><span data-stu-id="f81ce-119">Linux</span></span>

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

### <span data-ttu-id="f81ce-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="f81ce-120">-OSDiskName</span></span>
<span data-ttu-id="f81ce-121">Especifica o nome do disco que contém o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f81ce-121">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="f81ce-122">-Política</span><span class="sxs-lookup"><span data-stu-id="f81ce-122">-Policy</span></span>
<span data-ttu-id="f81ce-123">Especifica o objeto da política de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="f81ce-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81ce-124">-Proteção</span><span class="sxs-lookup"><span data-stu-id="f81ce-124">-Protection</span></span>
<span data-ttu-id="f81ce-125">Especifica se a proteção deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f81ce-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="f81ce-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f81ce-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f81ce-127">Ativação</span><span class="sxs-lookup"><span data-stu-id="f81ce-127">Enable</span></span>
- <span data-ttu-id="f81ce-128">Desabilita</span><span class="sxs-lookup"><span data-stu-id="f81ce-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81ce-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f81ce-129">-ProtectionEntity</span></span>
<span data-ttu-id="f81ce-130">Especifica o objeto da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="f81ce-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f81ce-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f81ce-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f81ce-132">Especifica a ID da conta de armazenamento do Azure de destino.</span><span class="sxs-lookup"><span data-stu-id="f81ce-132">Specifies the ID of the target Azure Storage account.</span></span>

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

### <span data-ttu-id="f81ce-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f81ce-133">-WaitForCompletion</span></span>
<span data-ttu-id="f81ce-134">Indica que o comando aguarda a conclusão antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="f81ce-134">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="f81ce-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f81ce-135">-Confirm</span></span>
<span data-ttu-id="f81ce-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f81ce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f81ce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f81ce-137">-WhatIf</span></span>
<span data-ttu-id="f81ce-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f81ce-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f81ce-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f81ce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f81ce-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81ce-140">-DefaultProfile</span></span>
<span data-ttu-id="f81ce-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f81ce-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f81ce-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81ce-142">CommonParameters</span></span>
<span data-ttu-id="f81ce-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f81ce-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81ce-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f81ce-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81ce-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f81ce-145">INPUTS</span></span>

### <span data-ttu-id="f81ce-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f81ce-146">ASRProtectionEntity</span></span>
<span data-ttu-id="f81ce-147">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f81ce-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="f81ce-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f81ce-148">OUTPUTS</span></span>

### <span data-ttu-id="f81ce-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f81ce-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f81ce-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f81ce-150">NOTES</span></span>

## <span data-ttu-id="f81ce-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f81ce-151">RELATED LINKS</span></span>

[<span data-ttu-id="f81ce-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f81ce-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
