---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 813291fd0014665958dbee85be36060801b3e569
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888444"
---
# <span data-ttu-id="9b63a-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="9b63a-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="9b63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b63a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b63a-103">Remove um script de implantação e seus recursos associados.</span><span class="sxs-lookup"><span data-stu-id="9b63a-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="9b63a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b63a-104">SYNTAX</span></span>

### <span data-ttu-id="9b63a-105">RemoveDeploymentScriptLogByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9b63a-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b63a-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b63a-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b63a-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b63a-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b63a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b63a-108">DESCRIPTION</span></span>
<span data-ttu-id="9b63a-109">O cmdlet **Remove-AzDeploymentScript** remove um script de implantação e seus recursos associados.</span><span class="sxs-lookup"><span data-stu-id="9b63a-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="9b63a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b63a-110">EXAMPLES</span></span>

### <span data-ttu-id="9b63a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b63a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="9b63a-112">Exclui um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="9b63a-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="9b63a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b63a-113">PARAMETERS</span></span>

### <span data-ttu-id="9b63a-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b63a-114">-Confirm</span></span>
<span data-ttu-id="9b63a-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b63a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b63a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b63a-116">-DefaultProfile</span></span>
<span data-ttu-id="9b63a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b63a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b63a-118">-Id</span><span class="sxs-lookup"><span data-stu-id="9b63a-118">-Id</span></span>
<span data-ttu-id="9b63a-119">A ID de recurso totalmente qualificada do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="9b63a-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="9b63a-120">Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="9b63a-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b63a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b63a-121">-InputObject</span></span>
<span data-ttu-id="9b63a-122">O objeto do PowerShell de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="9b63a-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b63a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9b63a-123">-Name</span></span>
<span data-ttu-id="9b63a-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b63a-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b63a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b63a-125">-PassThru</span></span>
<span data-ttu-id="9b63a-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9b63a-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b63a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b63a-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b63a-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b63a-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b63a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b63a-129">-WhatIf</span></span>
<span data-ttu-id="9b63a-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b63a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b63a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b63a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b63a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b63a-132">CommonParameters</span></span>
<span data-ttu-id="9b63a-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b63a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9b63a-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b63a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b63a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b63a-135">INPUTS</span></span>

### <span data-ttu-id="9b63a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9b63a-136">System.String</span></span>

### <span data-ttu-id="9b63a-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="9b63a-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="9b63a-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b63a-138">OUTPUTS</span></span>

### <span data-ttu-id="9b63a-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="9b63a-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="9b63a-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b63a-140">NOTES</span></span>

## <span data-ttu-id="9b63a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b63a-141">RELATED LINKS</span></span>