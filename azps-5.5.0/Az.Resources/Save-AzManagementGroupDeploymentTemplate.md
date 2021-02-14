---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117172"
---
# <span data-ttu-id="3e90a-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3e90a-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="3e90a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e90a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e90a-103">Salva um modelo de implantação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3e90a-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="3e90a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e90a-104">SYNTAX</span></span>

### <span data-ttu-id="3e90a-105">SaveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e90a-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e90a-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3e90a-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e90a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e90a-107">DESCRIPTION</span></span>
<span data-ttu-id="3e90a-108">O cmdlet **Save-AzManagementGroupDeploymentTemplate**  salva um modelo de implantação em um arquivo JSON para uma implantação em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="3e90a-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="3e90a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e90a-109">EXAMPLES</span></span>

### <span data-ttu-id="3e90a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e90a-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="3e90a-111">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="3e90a-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="3e90a-112">Exemplo 2: Obter uma implantação e salvar seu modelo</span><span class="sxs-lookup"><span data-stu-id="3e90a-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="3e90a-113">Esse comando obtém a implantação "RolesDeployment" no grupo de gerenciamento "myMG" e salva seu modelo.</span><span class="sxs-lookup"><span data-stu-id="3e90a-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="3e90a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e90a-114">PARAMETERS</span></span>

### <span data-ttu-id="3e90a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e90a-115">-DefaultProfile</span></span>
<span data-ttu-id="3e90a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e90a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e90a-117">-Nomeda Implantação</span><span class="sxs-lookup"><span data-stu-id="3e90a-117">-DeploymentName</span></span>
<span data-ttu-id="3e90a-118">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="3e90a-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e90a-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3e90a-119">-DeploymentObject</span></span>
<span data-ttu-id="3e90a-120">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="3e90a-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e90a-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3e90a-121">-Force</span></span>
<span data-ttu-id="3e90a-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e90a-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e90a-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3e90a-123">-ManagementGroupId</span></span>
<span data-ttu-id="3e90a-124">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="3e90a-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e90a-125">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3e90a-125">-Path</span></span>
<span data-ttu-id="3e90a-126">O caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="3e90a-126">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e90a-127">-Pré-</span><span class="sxs-lookup"><span data-stu-id="3e90a-127">-Pre</span></span>
<span data-ttu-id="3e90a-128">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3e90a-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3e90a-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e90a-129">-Confirm</span></span>
<span data-ttu-id="3e90a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e90a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e90a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e90a-131">-WhatIf</span></span>
<span data-ttu-id="3e90a-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e90a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e90a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e90a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e90a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e90a-134">CommonParameters</span></span>
<span data-ttu-id="3e90a-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e90a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e90a-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e90a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e90a-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e90a-137">INPUTS</span></span>

### <span data-ttu-id="3e90a-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3e90a-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3e90a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e90a-139">OUTPUTS</span></span>

### <span data-ttu-id="3e90a-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="3e90a-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="3e90a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="3e90a-141">NOTES</span></span>

## <span data-ttu-id="3e90a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e90a-142">RELATED LINKS</span></span>
