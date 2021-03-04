---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 876414b754a259d253dc56e5d92c570aa8f48318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890980"
---
# <span data-ttu-id="52719-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="52719-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="52719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52719-102">SYNOPSIS</span></span>
<span data-ttu-id="52719-103">Salva o log de uma execução de script de implantação em disco.</span><span class="sxs-lookup"><span data-stu-id="52719-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="52719-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52719-104">SYNTAX</span></span>

### <span data-ttu-id="52719-105">SaveDeploymentScriptLogByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52719-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52719-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="52719-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52719-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="52719-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52719-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52719-108">DESCRIPTION</span></span>
<span data-ttu-id="52719-109">O **Save-AzDeploymentScriptLog** salva o log de uma execução de script de implantação em disco.</span><span class="sxs-lookup"><span data-stu-id="52719-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="52719-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52719-110">EXAMPLES</span></span>

### <span data-ttu-id="52719-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52719-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="52719-112">Salva o log de um script de implantação com o nome e o grupo de recursos determinados.</span><span class="sxs-lookup"><span data-stu-id="52719-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="52719-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52719-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="52719-114">Salva as últimas 3 linhas do log de um script de implantação com o nome e o grupo de recursos determinados.</span><span class="sxs-lookup"><span data-stu-id="52719-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="52719-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52719-115">PARAMETERS</span></span>

### <span data-ttu-id="52719-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52719-116">-DefaultProfile</span></span>
<span data-ttu-id="52719-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52719-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52719-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="52719-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="52719-119">O objeto do PowerShell de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="52719-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52719-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="52719-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="52719-121">A ID de recurso totalmente qualificada do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="52719-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="52719-122">Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="52719-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52719-123">-Force</span><span class="sxs-lookup"><span data-stu-id="52719-123">-Force</span></span>
<span data-ttu-id="52719-124">Força a sobregravação do arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="52719-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="52719-125">-Name</span><span class="sxs-lookup"><span data-stu-id="52719-125">-Name</span></span>
<span data-ttu-id="52719-126">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="52719-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52719-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="52719-127">-OutputPath</span></span>
<span data-ttu-id="52719-128">O caminho do diretório para salvar o log de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="52719-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52719-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52719-129">-ResourceGroupName</span></span>
<span data-ttu-id="52719-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52719-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52719-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="52719-131">-Tail</span></span>
<span data-ttu-id="52719-132">Limitar a saída para as últimas linhas n</span><span class="sxs-lookup"><span data-stu-id="52719-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52719-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52719-133">-Confirm</span></span>
<span data-ttu-id="52719-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52719-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52719-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52719-135">-WhatIf</span></span>
<span data-ttu-id="52719-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52719-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52719-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52719-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52719-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52719-138">CommonParameters</span></span>
<span data-ttu-id="52719-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52719-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52719-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52719-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52719-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52719-141">INPUTS</span></span>

### <span data-ttu-id="52719-142">System.String</span><span class="sxs-lookup"><span data-stu-id="52719-142">System.String</span></span>

## <span data-ttu-id="52719-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52719-143">OUTPUTS</span></span>

### <span data-ttu-id="52719-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="52719-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="52719-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="52719-145">NOTES</span></span>

## <span data-ttu-id="52719-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52719-146">RELATED LINKS</span></span>
