---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 29c996036705e3fc71f1c6a04ead16c24b1b3bca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885261"
---
# <span data-ttu-id="56666-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="56666-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="56666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56666-102">SYNOPSIS</span></span>
<span data-ttu-id="56666-103">Atualize o mapeamento de contêineres de proteção de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="56666-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="56666-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56666-104">SYNTAX</span></span>

### <span data-ttu-id="56666-105">AzureToAzureEnableAutoUpdate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56666-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56666-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="56666-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56666-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56666-107">DESCRIPTION</span></span>
<span data-ttu-id="56666-108">O cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** atualiza o mapeamento especificado do contêiner de proteção de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="56666-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="56666-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56666-109">EXAMPLES</span></span>

### <span data-ttu-id="56666-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56666-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="56666-111">Inicie a operação para desabilitar a atualização automática do contêiner.</span><span class="sxs-lookup"><span data-stu-id="56666-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="56666-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="56666-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="56666-113">Inicie a operação para desabilitar habilitar a atualização automática para contêiner.</span><span class="sxs-lookup"><span data-stu-id="56666-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="56666-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56666-114">PARAMETERS</span></span>

### <span data-ttu-id="56666-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="56666-115">-AutomationAccountId</span></span>
<span data-ttu-id="56666-116">Especifica a conta de automaçãoId usada para udpate automático.</span><span class="sxs-lookup"><span data-stu-id="56666-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="56666-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="56666-117">-AzureToAzure</span></span>
<span data-ttu-id="56666-118">Especifica o Azure para o contêiner de proteção do Azure.</span><span class="sxs-lookup"><span data-stu-id="56666-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="56666-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56666-119">-DefaultProfile</span></span>
<span data-ttu-id="56666-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56666-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56666-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="56666-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="56666-122">Alternar parâmetro para desabilitar a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="56666-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="56666-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="56666-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="56666-124">Parâmetro Switch para habilitar a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="56666-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="56666-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56666-125">-InputObject</span></span>
<span data-ttu-id="56666-126">Objeto para mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="56666-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="56666-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56666-127">-Confirm</span></span>
<span data-ttu-id="56666-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56666-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56666-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56666-129">-WhatIf</span></span>
<span data-ttu-id="56666-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56666-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56666-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56666-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56666-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56666-132">CommonParameters</span></span>
<span data-ttu-id="56666-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56666-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56666-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56666-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56666-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56666-135">INPUTS</span></span>

### <span data-ttu-id="56666-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="56666-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="56666-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56666-137">OUTPUTS</span></span>

### <span data-ttu-id="56666-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="56666-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56666-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="56666-139">NOTES</span></span>

## <span data-ttu-id="56666-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56666-140">RELATED LINKS</span></span>
