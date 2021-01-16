---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258199"
---
# <span data-ttu-id="deff7-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="deff7-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="deff7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deff7-102">SYNOPSIS</span></span>
<span data-ttu-id="deff7-103">Atualize o mapeamento de contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="deff7-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="deff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deff7-104">SYNTAX</span></span>

### <span data-ttu-id="deff7-105">AzureToAzureEnableAutoUpdate (padrão)</span><span class="sxs-lookup"><span data-stu-id="deff7-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deff7-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="deff7-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="deff7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deff7-107">DESCRIPTION</span></span>
<span data-ttu-id="deff7-108">O cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** atualiza o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="deff7-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="deff7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deff7-109">EXAMPLES</span></span>

### <span data-ttu-id="deff7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="deff7-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="deff7-111">Inicie a operação para desabilitar a atualização automática do contêiner.</span><span class="sxs-lookup"><span data-stu-id="deff7-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="deff7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="deff7-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="deff7-113">Inicie a operação para desabilitar a atualização automática do contêiner.</span><span class="sxs-lookup"><span data-stu-id="deff7-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="deff7-114">OS</span><span class="sxs-lookup"><span data-stu-id="deff7-114">PARAMETERS</span></span>

### <span data-ttu-id="deff7-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="deff7-115">-AutomationAccountId</span></span>
<span data-ttu-id="deff7-116">Especifica a conta de automação usada para a udpate automática.</span><span class="sxs-lookup"><span data-stu-id="deff7-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="deff7-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="deff7-117">-AzureToAzure</span></span>
<span data-ttu-id="deff7-118">Especifica o contêiner de proteção do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="deff7-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="deff7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deff7-119">-DefaultProfile</span></span>
<span data-ttu-id="deff7-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deff7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deff7-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="deff7-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="deff7-122">Parâmetro de opção para desabilitar a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="deff7-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="deff7-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="deff7-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="deff7-124">Parâmetro de alternância para habilitar a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="deff7-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="deff7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deff7-125">-InputObject</span></span>
<span data-ttu-id="deff7-126">Objeto para mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="deff7-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="deff7-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="deff7-127">-Confirm</span></span>
<span data-ttu-id="deff7-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deff7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deff7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deff7-129">-WhatIf</span></span>
<span data-ttu-id="deff7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="deff7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deff7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="deff7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deff7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deff7-132">CommonParameters</span></span>
<span data-ttu-id="deff7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deff7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deff7-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deff7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deff7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deff7-135">INPUTS</span></span>

### <span data-ttu-id="deff7-136">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="deff7-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="deff7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deff7-137">OUTPUTS</span></span>

### <span data-ttu-id="deff7-138">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="deff7-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="deff7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deff7-139">NOTES</span></span>

## <span data-ttu-id="deff7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deff7-140">RELATED LINKS</span></span>
