---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610722"
---
# <span data-ttu-id="5bcd2-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="5bcd2-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="5bcd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bcd2-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcd2-103">Salva um modelo de implantação de grupo de recursos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bcd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bcd2-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bcd2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bcd2-105">DESCRIPTION</span></span>
<span data-ttu-id="5bcd2-106">O cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  salva um modelo de implantação de grupo de recursos em um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="5bcd2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bcd2-107">EXAMPLES</span></span>

### <span data-ttu-id="5bcd2-108">Exemplo 1: salvar um modelo de implantação</span><span class="sxs-lookup"><span data-stu-id="5bcd2-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="5bcd2-109">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="5bcd2-110">OS</span><span class="sxs-lookup"><span data-stu-id="5bcd2-110">PARAMETERS</span></span>

### <span data-ttu-id="5bcd2-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5bcd2-111">-ApiVersion</span></span>
<span data-ttu-id="5bcd2-112">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5bcd2-113">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="5bcd2-114">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="5bcd2-114">-DeploymentName</span></span>
<span data-ttu-id="5bcd2-115">Especifica o nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="5bcd2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5bcd2-116">-Force</span></span>
<span data-ttu-id="5bcd2-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5bcd2-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5bcd2-118">-InformationAction</span></span>
<span data-ttu-id="5bcd2-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5bcd2-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5bcd2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bcd2-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="5bcd2-121">Continue</span></span>
- <span data-ttu-id="5bcd2-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="5bcd2-122">Ignore</span></span>
- <span data-ttu-id="5bcd2-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="5bcd2-123">Inquire</span></span>
- <span data-ttu-id="5bcd2-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5bcd2-124">SilentlyContinue</span></span>
- <span data-ttu-id="5bcd2-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="5bcd2-125">Stop</span></span>
- <span data-ttu-id="5bcd2-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="5bcd2-126">Suspend</span></span>

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

### <span data-ttu-id="5bcd2-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5bcd2-127">-InformationVariable</span></span>
<span data-ttu-id="5bcd2-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5bcd2-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="5bcd2-129">-Path</span></span>
<span data-ttu-id="5bcd2-130">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="5bcd2-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bcd2-131">-Pre</span></span>
<span data-ttu-id="5bcd2-132">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="5bcd2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcd2-133">-ResourceGroupName</span></span>
<span data-ttu-id="5bcd2-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5bcd2-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5bcd2-135">-Confirm</span></span>
<span data-ttu-id="5bcd2-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bcd2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bcd2-137">-WhatIf</span></span>
<span data-ttu-id="5bcd2-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bcd2-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bcd2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcd2-140">-DefaultProfile</span></span>
<span data-ttu-id="5bcd2-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bcd2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcd2-142">CommonParameters</span></span>
<span data-ttu-id="5bcd2-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bcd2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcd2-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bcd2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcd2-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bcd2-145">INPUTS</span></span>

## <span data-ttu-id="5bcd2-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bcd2-146">OUTPUTS</span></span>

### <span data-ttu-id="5bcd2-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5bcd2-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5bcd2-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bcd2-148">NOTES</span></span>

## <span data-ttu-id="5bcd2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bcd2-149">RELATED LINKS</span></span>

