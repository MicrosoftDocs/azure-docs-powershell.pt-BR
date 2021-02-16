---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114017"
---
# <span data-ttu-id="1f65d-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1f65d-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="1f65d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f65d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f65d-103">Salva um modelo de implantação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1f65d-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="1f65d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f65d-104">SYNTAX</span></span>

### <span data-ttu-id="1f65d-105">SaveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f65d-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f65d-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1f65d-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f65d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f65d-107">DESCRIPTION</span></span>
<span data-ttu-id="1f65d-108">O cmdlet **Save-AzDeploymentTemplate**  salva um modelo de implantação em um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="1f65d-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="1f65d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f65d-109">EXAMPLES</span></span>

### <span data-ttu-id="1f65d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f65d-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="1f65d-111">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="1f65d-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="1f65d-112">Exemplo 2: Obter uma implantação e salvar seu modelo</span><span class="sxs-lookup"><span data-stu-id="1f65d-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="1f65d-113">Esse comando obtém a implantação "RolesDeployment" no escopo da assinatura atual e salva seu modelo.</span><span class="sxs-lookup"><span data-stu-id="1f65d-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="1f65d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f65d-114">PARAMETERS</span></span>

### <span data-ttu-id="1f65d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f65d-115">-DefaultProfile</span></span>
<span data-ttu-id="1f65d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f65d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f65d-117">-Nomeda Implantação</span><span class="sxs-lookup"><span data-stu-id="1f65d-117">-DeploymentName</span></span>
<span data-ttu-id="1f65d-118">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="1f65d-118">The deployment name.</span></span>

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

### <span data-ttu-id="1f65d-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1f65d-119">-DeploymentObject</span></span>
<span data-ttu-id="1f65d-120">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="1f65d-120">The deployment object.</span></span>

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

### <span data-ttu-id="1f65d-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1f65d-121">-Force</span></span>
<span data-ttu-id="1f65d-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1f65d-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1f65d-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1f65d-123">-Path</span></span>
<span data-ttu-id="1f65d-124">O caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="1f65d-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="1f65d-125">-Pré-</span><span class="sxs-lookup"><span data-stu-id="1f65d-125">-Pre</span></span>
<span data-ttu-id="1f65d-126">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1f65d-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1f65d-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1f65d-127">-Confirm</span></span>
<span data-ttu-id="1f65d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f65d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f65d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f65d-129">-WhatIf</span></span>
<span data-ttu-id="1f65d-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1f65d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f65d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f65d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f65d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f65d-132">CommonParameters</span></span>
<span data-ttu-id="1f65d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f65d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f65d-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f65d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f65d-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f65d-135">INPUTS</span></span>

### <span data-ttu-id="1f65d-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1f65d-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1f65d-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f65d-137">OUTPUTS</span></span>

### <span data-ttu-id="1f65d-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="1f65d-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="1f65d-139">Notas</span><span class="sxs-lookup"><span data-stu-id="1f65d-139">NOTES</span></span>

## <span data-ttu-id="1f65d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f65d-140">RELATED LINKS</span></span>
