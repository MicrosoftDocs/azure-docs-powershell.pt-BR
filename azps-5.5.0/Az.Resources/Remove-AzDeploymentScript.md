---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113310"
---
# <span data-ttu-id="3f02c-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="3f02c-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="3f02c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f02c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f02c-103">Remove um script de implantação e seus recursos associados.</span><span class="sxs-lookup"><span data-stu-id="3f02c-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="3f02c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f02c-104">SYNTAX</span></span>

### <span data-ttu-id="3f02c-105">RemoveDeploymentScriptLogByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f02c-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f02c-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f02c-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f02c-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f02c-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f02c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f02c-108">DESCRIPTION</span></span>
<span data-ttu-id="3f02c-109">O **cmdlet Remove-AzDeploymentScript** remove um script de implantação e seus recursos associados.</span><span class="sxs-lookup"><span data-stu-id="3f02c-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="3f02c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f02c-110">EXAMPLES</span></span>

### <span data-ttu-id="3f02c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f02c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="3f02c-112">Exclui um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="3f02c-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="3f02c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f02c-113">PARAMETERS</span></span>

### <span data-ttu-id="3f02c-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3f02c-114">-Confirm</span></span>
<span data-ttu-id="3f02c-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f02c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f02c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f02c-116">-DefaultProfile</span></span>
<span data-ttu-id="3f02c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f02c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f02c-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3f02c-118">-Id</span></span>
<span data-ttu-id="3f02c-119">A ID de recurso totalmente qualificada do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="3f02c-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="3f02c-120">Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="3f02c-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="3f02c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f02c-121">-InputObject</span></span>
<span data-ttu-id="3f02c-122">O objeto do PowerShell de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="3f02c-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="3f02c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f02c-123">-Name</span></span>
<span data-ttu-id="3f02c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f02c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f02c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f02c-125">-PassThru</span></span>
<span data-ttu-id="3f02c-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3f02c-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f02c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f02c-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f02c-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f02c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f02c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f02c-129">-WhatIf</span></span>
<span data-ttu-id="3f02c-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3f02c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f02c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f02c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f02c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f02c-132">CommonParameters</span></span>
<span data-ttu-id="3f02c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f02c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3f02c-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f02c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f02c-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f02c-135">INPUTS</span></span>

### <span data-ttu-id="3f02c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3f02c-136">System.String</span></span>

### <span data-ttu-id="3f02c-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="3f02c-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="3f02c-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f02c-138">OUTPUTS</span></span>

### <span data-ttu-id="3f02c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="3f02c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="3f02c-140">Notas</span><span class="sxs-lookup"><span data-stu-id="3f02c-140">NOTES</span></span>

## <span data-ttu-id="3f02c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f02c-141">RELATED LINKS</span></span>