---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427214"
---
# <span data-ttu-id="2c694-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="2c694-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="2c694-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c694-102">SYNOPSIS</span></span>
<span data-ttu-id="2c694-103">Remove um script de implantação e seus recursos associados.</span><span class="sxs-lookup"><span data-stu-id="2c694-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="2c694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c694-104">SYNTAX</span></span>

### <span data-ttu-id="2c694-105">RemoveDeploymentScriptLogByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c694-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c694-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c694-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c694-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c694-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c694-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c694-108">DESCRIPTION</span></span>
<span data-ttu-id="2c694-109">O cmdlet **Remove-AzDeploymentScript** remove um script de implantação e seus recursos associados.</span><span class="sxs-lookup"><span data-stu-id="2c694-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="2c694-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c694-110">EXAMPLES</span></span>

### <span data-ttu-id="2c694-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c694-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="2c694-112">Exclui um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="2c694-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="2c694-113">OS</span><span class="sxs-lookup"><span data-stu-id="2c694-113">PARAMETERS</span></span>

### <span data-ttu-id="2c694-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c694-114">-Confirm</span></span>
<span data-ttu-id="2c694-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c694-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c694-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c694-116">-DefaultProfile</span></span>
<span data-ttu-id="2c694-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c694-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c694-118">-ID</span><span class="sxs-lookup"><span data-stu-id="2c694-118">-Id</span></span>
<span data-ttu-id="2c694-119">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="2c694-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="2c694-120">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="2c694-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="2c694-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c694-121">-InputObject</span></span>
<span data-ttu-id="2c694-122">O objeto do PowerShell do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="2c694-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="2c694-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c694-123">-Name</span></span>
<span data-ttu-id="2c694-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c694-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c694-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c694-125">-PassThru</span></span>
<span data-ttu-id="2c694-126">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="2c694-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2c694-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c694-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c694-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c694-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c694-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c694-129">-WhatIf</span></span>
<span data-ttu-id="2c694-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c694-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c694-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c694-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c694-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c694-132">CommonParameters</span></span>
<span data-ttu-id="2c694-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c694-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c694-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c694-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c694-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c694-135">INPUTS</span></span>

### <span data-ttu-id="2c694-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2c694-136">System.String</span></span>

### <span data-ttu-id="2c694-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="2c694-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="2c694-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c694-138">OUTPUTS</span></span>

### <span data-ttu-id="2c694-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="2c694-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="2c694-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c694-140">NOTES</span></span>

## <span data-ttu-id="2c694-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c694-141">RELATED LINKS</span></span>