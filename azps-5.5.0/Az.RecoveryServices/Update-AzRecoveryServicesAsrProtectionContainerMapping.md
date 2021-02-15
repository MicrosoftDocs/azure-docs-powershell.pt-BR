---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114921"
---
# <span data-ttu-id="9cf32-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9cf32-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="9cf32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cf32-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf32-103">Atualize o mapeamento de contêineres de proteção de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf32-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="9cf32-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cf32-104">SYNTAX</span></span>

### <span data-ttu-id="9cf32-105">AzureToAzureEnableAutoUpdate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9cf32-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf32-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="9cf32-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf32-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cf32-107">DESCRIPTION</span></span>
<span data-ttu-id="9cf32-108">O cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** atualiza o mapeamento de contêiner de proteção de Recuperação de Site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="9cf32-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="9cf32-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9cf32-109">EXAMPLES</span></span>

### <span data-ttu-id="9cf32-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9cf32-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="9cf32-111">Inicie a operação para desabilitar a atualização automática do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cf32-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="9cf32-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9cf32-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="9cf32-113">Inicie a operação para desabilitar a atualização automática do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cf32-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="9cf32-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cf32-114">PARAMETERS</span></span>

### <span data-ttu-id="9cf32-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="9cf32-115">-AutomationAccountId</span></span>
<span data-ttu-id="9cf32-116">Especifica a conta de automação usada para udpate automático.</span><span class="sxs-lookup"><span data-stu-id="9cf32-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf32-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9cf32-117">-AzureToAzure</span></span>
<span data-ttu-id="9cf32-118">Especifica o Azure ao contêiner de proteção do Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf32-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf32-119">-DefaultProfile</span></span>
<span data-ttu-id="9cf32-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf32-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cf32-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="9cf32-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="9cf32-122">Alternar parâmetro para desabilitar a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="9cf32-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf32-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="9cf32-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="9cf32-124">Alternar parâmetro para habilitar a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="9cf32-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf32-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf32-125">-InputObject</span></span>
<span data-ttu-id="9cf32-126">Objeto para mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="9cf32-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf32-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9cf32-127">-Confirm</span></span>
<span data-ttu-id="9cf32-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cf32-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf32-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf32-129">-WhatIf</span></span>
<span data-ttu-id="9cf32-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9cf32-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf32-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9cf32-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf32-132">CommonParameters</span></span>
<span data-ttu-id="9cf32-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf32-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cf32-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf32-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="9cf32-135">INPUTS</span></span>

### <span data-ttu-id="9cf32-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9cf32-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="9cf32-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="9cf32-137">OUTPUTS</span></span>

### <span data-ttu-id="9cf32-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9cf32-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9cf32-139">Notas</span><span class="sxs-lookup"><span data-stu-id="9cf32-139">NOTES</span></span>

## <span data-ttu-id="9cf32-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cf32-140">RELATED LINKS</span></span>
