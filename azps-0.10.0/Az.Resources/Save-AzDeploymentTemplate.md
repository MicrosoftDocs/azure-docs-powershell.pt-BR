---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 82fd6ba15a240be208445493810551154e188e92
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776327"
---
# <span data-ttu-id="a5b94-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a5b94-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="a5b94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5b94-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b94-103">Salva um modelo de implantação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5b94-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="a5b94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5b94-104">SYNTAX</span></span>

### <span data-ttu-id="a5b94-105">SaveByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5b94-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b94-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a5b94-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b94-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5b94-107">DESCRIPTION</span></span>
<span data-ttu-id="a5b94-108">O cmdlet **Save-AzDeploymentTemplate**  salva um modelo de implantação em um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="a5b94-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="a5b94-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5b94-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b94-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5b94-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="a5b94-111">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="a5b94-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="a5b94-112">Exemplo 2: obter uma implantação e salvar seu modelo</span><span class="sxs-lookup"><span data-stu-id="a5b94-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="a5b94-113">Esse comando obtém a implantação "RolesDeployment" no escopo da assinatura atual e salva seu modelo.</span><span class="sxs-lookup"><span data-stu-id="a5b94-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="a5b94-114">OS</span><span class="sxs-lookup"><span data-stu-id="a5b94-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b94-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a5b94-115">-ApiVersion</span></span>
<span data-ttu-id="a5b94-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a5b94-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a5b94-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a5b94-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b94-118">-DefaultProfile</span></span>
<span data-ttu-id="a5b94-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b94-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b94-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="a5b94-120">-DeploymentName</span></span>
<span data-ttu-id="a5b94-121">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="a5b94-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b94-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a5b94-122">-DeploymentObject</span></span>
<span data-ttu-id="a5b94-123">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="a5b94-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b94-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a5b94-124">-Force</span></span>
<span data-ttu-id="a5b94-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a5b94-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a5b94-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a5b94-126">-Path</span></span>
<span data-ttu-id="a5b94-127">O caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="a5b94-127">The output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b94-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="a5b94-128">-Pre</span></span>
<span data-ttu-id="a5b94-129">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a5b94-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a5b94-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5b94-130">-Confirm</span></span>
<span data-ttu-id="a5b94-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b94-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b94-132">-WhatIf</span></span>
<span data-ttu-id="a5b94-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5b94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b94-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5b94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b94-135">CommonParameters</span></span>
<span data-ttu-id="a5b94-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b94-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b94-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b94-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5b94-138">INPUTS</span></span>

### <span data-ttu-id="a5b94-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b94-139">System.String</span></span>

## <span data-ttu-id="a5b94-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5b94-140">OUTPUTS</span></span>

### <span data-ttu-id="a5b94-141">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels</span><span class="sxs-lookup"><span data-stu-id="a5b94-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="a5b94-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5b94-142">NOTES</span></span>

## <span data-ttu-id="a5b94-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5b94-143">RELATED LINKS</span></span>