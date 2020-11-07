---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941787"
---
# <span data-ttu-id="b5051-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b5051-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="b5051-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5051-102">SYNOPSIS</span></span>
<span data-ttu-id="b5051-103">Salva o log de uma execução de script de implantação em disco.</span><span class="sxs-lookup"><span data-stu-id="b5051-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b5051-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5051-104">SYNTAX</span></span>

### <span data-ttu-id="b5051-105">SaveDeploymentScriptLogByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b5051-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5051-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5051-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5051-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5051-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5051-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5051-108">DESCRIPTION</span></span>
<span data-ttu-id="b5051-109">**Save-AzDeploymentScriptLog** salva o log de uma execução de script de implantação em disco.</span><span class="sxs-lookup"><span data-stu-id="b5051-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b5051-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5051-110">EXAMPLES</span></span>

### <span data-ttu-id="b5051-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5051-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="b5051-112">Salva o log de um script de implantação com o nome e o grupo de recursos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="b5051-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="b5051-113">OS</span><span class="sxs-lookup"><span data-stu-id="b5051-113">PARAMETERS</span></span>

### <span data-ttu-id="b5051-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b5051-114">-Confirm</span></span>
<span data-ttu-id="b5051-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5051-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5051-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5051-116">-DefaultProfile</span></span>
<span data-ttu-id="b5051-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5051-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5051-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="b5051-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="b5051-119">O objeto do PowerShell do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b5051-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5051-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="b5051-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="b5051-121">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b5051-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b5051-122">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b5051-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5051-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b5051-123">-Force</span></span>
<span data-ttu-id="b5051-124">Força a substituição do arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="b5051-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="b5051-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5051-125">-Name</span></span>
<span data-ttu-id="b5051-126">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b5051-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5051-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b5051-127">-OutputPath</span></span>
<span data-ttu-id="b5051-128">O caminho do diretório para salvar o log de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b5051-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5051-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5051-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5051-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5051-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5051-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5051-131">-WhatIf</span></span>
<span data-ttu-id="b5051-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5051-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5051-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5051-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5051-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5051-134">CommonParameters</span></span>
<span data-ttu-id="b5051-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5051-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b5051-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5051-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5051-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5051-137">INPUTS</span></span>

### <span data-ttu-id="b5051-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b5051-138">System.String</span></span>

## <span data-ttu-id="b5051-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5051-139">OUTPUTS</span></span>

### <span data-ttu-id="b5051-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="b5051-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="b5051-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5051-141">NOTES</span></span>

## <span data-ttu-id="b5051-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5051-142">RELATED LINKS</span></span>
