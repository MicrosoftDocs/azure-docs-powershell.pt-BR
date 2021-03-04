---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: f64b839e4f13a08ed1af1e73fcf4324a98b68a7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890979"
---
# <span data-ttu-id="9da7f-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9da7f-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="9da7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9da7f-102">SYNOPSIS</span></span>
<span data-ttu-id="9da7f-103">Salva um modelo de implantação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9da7f-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="9da7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9da7f-104">SYNTAX</span></span>

### <span data-ttu-id="9da7f-105">SaveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9da7f-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da7f-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9da7f-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da7f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9da7f-107">DESCRIPTION</span></span>
<span data-ttu-id="9da7f-108">O cmdlet **Save-AzTenantDeploymentTemplate**  salva um modelo de implantação em um arquivo JSON para uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="9da7f-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="9da7f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9da7f-109">EXAMPLES</span></span>

### <span data-ttu-id="9da7f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9da7f-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="9da7f-111">Este comando obtém o modelo de implantação de TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="9da7f-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="9da7f-112">Exemplo 2: Obter uma implantação e salvar seu modelo</span><span class="sxs-lookup"><span data-stu-id="9da7f-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="9da7f-113">Este comando obtém a implantação "RolesDeployment" no escopo de locatário atual e salva seu modelo.</span><span class="sxs-lookup"><span data-stu-id="9da7f-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="9da7f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9da7f-114">PARAMETERS</span></span>

### <span data-ttu-id="9da7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da7f-115">-DefaultProfile</span></span>
<span data-ttu-id="9da7f-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9da7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da7f-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9da7f-117">-DeploymentName</span></span>
<span data-ttu-id="9da7f-118">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="9da7f-118">The deployment name.</span></span>

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

### <span data-ttu-id="9da7f-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9da7f-119">-DeploymentObject</span></span>
<span data-ttu-id="9da7f-120">O objeto deployment.</span><span class="sxs-lookup"><span data-stu-id="9da7f-120">The deployment object.</span></span>

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

### <span data-ttu-id="9da7f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9da7f-121">-Force</span></span>
<span data-ttu-id="9da7f-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9da7f-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9da7f-123">-Path</span><span class="sxs-lookup"><span data-stu-id="9da7f-123">-Path</span></span>
<span data-ttu-id="9da7f-124">O caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="9da7f-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="9da7f-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="9da7f-125">-Pre</span></span>
<span data-ttu-id="9da7f-126">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9da7f-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9da7f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9da7f-127">-Confirm</span></span>
<span data-ttu-id="9da7f-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da7f-129">-WhatIf</span></span>
<span data-ttu-id="9da7f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9da7f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da7f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9da7f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da7f-132">CommonParameters</span></span>
<span data-ttu-id="9da7f-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da7f-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9da7f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da7f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9da7f-135">INPUTS</span></span>

### <span data-ttu-id="9da7f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9da7f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9da7f-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9da7f-137">OUTPUTS</span></span>

### <span data-ttu-id="9da7f-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="9da7f-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="9da7f-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="9da7f-139">NOTES</span></span>

## <span data-ttu-id="9da7f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9da7f-140">RELATED LINKS</span></span>
