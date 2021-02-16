---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113300"
---
# <span data-ttu-id="181ff-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="181ff-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="181ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="181ff-102">SYNOPSIS</span></span>
<span data-ttu-id="181ff-103">Salva um modelo de implantação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="181ff-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="181ff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="181ff-104">SYNTAX</span></span>

### <span data-ttu-id="181ff-105">SaveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="181ff-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="181ff-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="181ff-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="181ff-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="181ff-107">DESCRIPTION</span></span>
<span data-ttu-id="181ff-108">O cmdlet **Save-AzTenantDeploymentTemplate**  salva um modelo de implantação em um arquivo JSON para uma implantação no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="181ff-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="181ff-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="181ff-109">EXAMPLES</span></span>

### <span data-ttu-id="181ff-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="181ff-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="181ff-111">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="181ff-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="181ff-112">Exemplo 2: Obter uma implantação e salvar seu modelo</span><span class="sxs-lookup"><span data-stu-id="181ff-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="181ff-113">Esse comando obtém a implantação "RolesDeployment" no escopo atual do locatário e salva seu modelo.</span><span class="sxs-lookup"><span data-stu-id="181ff-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="181ff-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="181ff-114">PARAMETERS</span></span>

### <span data-ttu-id="181ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181ff-115">-DefaultProfile</span></span>
<span data-ttu-id="181ff-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="181ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181ff-117">-Nomeda Implantação</span><span class="sxs-lookup"><span data-stu-id="181ff-117">-DeploymentName</span></span>
<span data-ttu-id="181ff-118">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="181ff-118">The deployment name.</span></span>

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

### <span data-ttu-id="181ff-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="181ff-119">-DeploymentObject</span></span>
<span data-ttu-id="181ff-120">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="181ff-120">The deployment object.</span></span>

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

### <span data-ttu-id="181ff-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="181ff-121">-Force</span></span>
<span data-ttu-id="181ff-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="181ff-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="181ff-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="181ff-123">-Path</span></span>
<span data-ttu-id="181ff-124">O caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="181ff-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="181ff-125">-Pré-</span><span class="sxs-lookup"><span data-stu-id="181ff-125">-Pre</span></span>
<span data-ttu-id="181ff-126">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="181ff-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="181ff-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="181ff-127">-Confirm</span></span>
<span data-ttu-id="181ff-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="181ff-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="181ff-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="181ff-129">-WhatIf</span></span>
<span data-ttu-id="181ff-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="181ff-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="181ff-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="181ff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="181ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181ff-132">CommonParameters</span></span>
<span data-ttu-id="181ff-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181ff-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="181ff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181ff-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="181ff-135">INPUTS</span></span>

### <span data-ttu-id="181ff-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="181ff-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="181ff-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="181ff-137">OUTPUTS</span></span>

### <span data-ttu-id="181ff-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="181ff-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="181ff-139">Notas</span><span class="sxs-lookup"><span data-stu-id="181ff-139">NOTES</span></span>

## <span data-ttu-id="181ff-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="181ff-140">RELATED LINKS</span></span>
