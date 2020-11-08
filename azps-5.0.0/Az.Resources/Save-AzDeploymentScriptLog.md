---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125762"
---
# <span data-ttu-id="7abad-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="7abad-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="7abad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7abad-102">SYNOPSIS</span></span>
<span data-ttu-id="7abad-103">Salva o log de uma execução de script de implantação em disco.</span><span class="sxs-lookup"><span data-stu-id="7abad-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="7abad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7abad-104">SYNTAX</span></span>

### <span data-ttu-id="7abad-105">SaveDeploymentScriptLogByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7abad-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7abad-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="7abad-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abad-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="7abad-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7abad-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7abad-108">DESCRIPTION</span></span>
<span data-ttu-id="7abad-109">**Save-AzDeploymentScriptLog** salva o log de uma execução de script de implantação em disco.</span><span class="sxs-lookup"><span data-stu-id="7abad-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="7abad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7abad-110">EXAMPLES</span></span>

### <span data-ttu-id="7abad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7abad-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="7abad-112">Salva o log de um script de implantação com o nome e o grupo de recursos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7abad-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="7abad-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7abad-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="7abad-114">Salva as três últimas linhas do log de um script de implantação com o nome e o grupo de recursos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7abad-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="7abad-115">OS</span><span class="sxs-lookup"><span data-stu-id="7abad-115">PARAMETERS</span></span>

### <span data-ttu-id="7abad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abad-116">-DefaultProfile</span></span>
<span data-ttu-id="7abad-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7abad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7abad-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="7abad-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="7abad-119">O objeto do PowerShell do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="7abad-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="7abad-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="7abad-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="7abad-121">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="7abad-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="7abad-122">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="7abad-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="7abad-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7abad-123">-Force</span></span>
<span data-ttu-id="7abad-124">Força a substituição do arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="7abad-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="7abad-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7abad-125">-Name</span></span>
<span data-ttu-id="7abad-126">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="7abad-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="7abad-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="7abad-127">-OutputPath</span></span>
<span data-ttu-id="7abad-128">O caminho do diretório para salvar o log de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="7abad-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="7abad-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abad-129">-ResourceGroupName</span></span>
<span data-ttu-id="7abad-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7abad-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7abad-131">-Caudal</span><span class="sxs-lookup"><span data-stu-id="7abad-131">-Tail</span></span>
<span data-ttu-id="7abad-132">Limitar a saída às últimas n linhas</span><span class="sxs-lookup"><span data-stu-id="7abad-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="7abad-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7abad-133">-Confirm</span></span>
<span data-ttu-id="7abad-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7abad-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abad-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abad-135">-WhatIf</span></span>
<span data-ttu-id="7abad-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7abad-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7abad-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7abad-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abad-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abad-138">CommonParameters</span></span>
<span data-ttu-id="7abad-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abad-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abad-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7abad-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abad-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7abad-141">INPUTS</span></span>

### <span data-ttu-id="7abad-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7abad-142">System.String</span></span>

## <span data-ttu-id="7abad-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7abad-143">OUTPUTS</span></span>

### <span data-ttu-id="7abad-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="7abad-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="7abad-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7abad-145">NOTES</span></span>

## <span data-ttu-id="7abad-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7abad-146">RELATED LINKS</span></span>
