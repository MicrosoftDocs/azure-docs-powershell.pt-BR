---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 1ffdcef1bb27ec06873c12f64a135adc0e433929
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776328"
---
# <span data-ttu-id="d9107-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d9107-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="d9107-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9107-102">SYNOPSIS</span></span>
<span data-ttu-id="d9107-103">Salva um modelo de implantação de grupo de recursos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d9107-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="d9107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9107-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9107-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9107-105">DESCRIPTION</span></span>
<span data-ttu-id="d9107-106">O cmdlet **Save-AzResourceGroupDeploymentTemplate**  salva um modelo de implantação de grupo de recursos em um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="d9107-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="d9107-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9107-107">EXAMPLES</span></span>

### <span data-ttu-id="d9107-108">Exemplo 1: salvar um modelo de implantação</span><span class="sxs-lookup"><span data-stu-id="d9107-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="d9107-109">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="d9107-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="d9107-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9107-110">PARAMETERS</span></span>

### <span data-ttu-id="d9107-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9107-111">-ApiVersion</span></span>
<span data-ttu-id="d9107-112">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d9107-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9107-113">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="d9107-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="d9107-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9107-114">-DefaultProfile</span></span>
<span data-ttu-id="d9107-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d9107-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="d9107-116">-DeploymentName</span></span>
<span data-ttu-id="d9107-117">Especifica o nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="d9107-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d9107-118">-Force</span></span>
<span data-ttu-id="d9107-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9107-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9107-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d9107-120">-InformationAction</span></span>
<span data-ttu-id="d9107-121">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="d9107-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d9107-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d9107-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9107-123">Contínuo</span><span class="sxs-lookup"><span data-stu-id="d9107-123">Continue</span></span>
- <span data-ttu-id="d9107-124">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d9107-124">Ignore</span></span>
- <span data-ttu-id="d9107-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="d9107-125">Inquire</span></span>
- <span data-ttu-id="d9107-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d9107-126">SilentlyContinue</span></span>
- <span data-ttu-id="d9107-127">Finaliza</span><span class="sxs-lookup"><span data-stu-id="d9107-127">Stop</span></span>
- <span data-ttu-id="d9107-128">Suspensão</span><span class="sxs-lookup"><span data-stu-id="d9107-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d9107-129">-InformationVariable</span></span>
<span data-ttu-id="d9107-130">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="d9107-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d9107-131">-Path</span></span>
<span data-ttu-id="d9107-132">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="d9107-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9107-133">-Pre</span></span>
<span data-ttu-id="d9107-134">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="d9107-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="d9107-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9107-135">-ResourceGroupName</span></span>
<span data-ttu-id="d9107-136">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9107-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9107-137">-Confirm</span></span>
<span data-ttu-id="d9107-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9107-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9107-139">-WhatIf</span></span>
<span data-ttu-id="d9107-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9107-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9107-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9107-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9107-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9107-142">CommonParameters</span></span>
<span data-ttu-id="d9107-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9107-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9107-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9107-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9107-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9107-145">INPUTS</span></span>

## <span data-ttu-id="d9107-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9107-146">OUTPUTS</span></span>

## <span data-ttu-id="d9107-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9107-147">NOTES</span></span>

## <span data-ttu-id="d9107-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9107-148">RELATED LINKS</span></span>
