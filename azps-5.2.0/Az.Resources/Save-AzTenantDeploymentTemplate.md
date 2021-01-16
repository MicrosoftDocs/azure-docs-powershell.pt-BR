---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261338"
---
# <span data-ttu-id="128de-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="128de-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="128de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="128de-102">SYNOPSIS</span></span>
<span data-ttu-id="128de-103">Salva um modelo de implantação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="128de-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="128de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="128de-104">SYNTAX</span></span>

### <span data-ttu-id="128de-105">SaveByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="128de-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="128de-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="128de-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="128de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="128de-107">DESCRIPTION</span></span>
<span data-ttu-id="128de-108">O cmdlet **Save-AzTenantDeploymentTemplate**  salva um modelo de implantação em um arquivo JSON para uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="128de-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="128de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="128de-109">EXAMPLES</span></span>

### <span data-ttu-id="128de-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="128de-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="128de-111">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="128de-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="128de-112">Exemplo 2: obter uma implantação e salvar seu modelo</span><span class="sxs-lookup"><span data-stu-id="128de-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="128de-113">Esse comando obtém a implantação "RolesDeployment" no escopo do locatário atual e salva seu modelo.</span><span class="sxs-lookup"><span data-stu-id="128de-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="128de-114">OS</span><span class="sxs-lookup"><span data-stu-id="128de-114">PARAMETERS</span></span>

### <span data-ttu-id="128de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128de-115">-DefaultProfile</span></span>
<span data-ttu-id="128de-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="128de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128de-117">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="128de-117">-DeploymentName</span></span>
<span data-ttu-id="128de-118">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="128de-118">The deployment name.</span></span>

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

### <span data-ttu-id="128de-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="128de-119">-DeploymentObject</span></span>
<span data-ttu-id="128de-120">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="128de-120">The deployment object.</span></span>

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

### <span data-ttu-id="128de-121">-Force</span><span class="sxs-lookup"><span data-stu-id="128de-121">-Force</span></span>
<span data-ttu-id="128de-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="128de-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="128de-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="128de-123">-Path</span></span>
<span data-ttu-id="128de-124">O caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="128de-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="128de-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="128de-125">-Pre</span></span>
<span data-ttu-id="128de-126">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="128de-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="128de-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="128de-127">-Confirm</span></span>
<span data-ttu-id="128de-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="128de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="128de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="128de-129">-WhatIf</span></span>
<span data-ttu-id="128de-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="128de-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="128de-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="128de-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="128de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128de-132">CommonParameters</span></span>
<span data-ttu-id="128de-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="128de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128de-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="128de-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128de-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="128de-135">INPUTS</span></span>

### <span data-ttu-id="128de-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="128de-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="128de-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="128de-137">OUTPUTS</span></span>

### <span data-ttu-id="128de-138">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="128de-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="128de-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="128de-139">NOTES</span></span>

## <span data-ttu-id="128de-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="128de-140">RELATED LINKS</span></span>
