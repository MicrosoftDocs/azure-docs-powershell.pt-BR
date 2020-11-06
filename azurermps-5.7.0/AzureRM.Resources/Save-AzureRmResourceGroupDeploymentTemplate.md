---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 2be6deeca64a8d167231cf7afe3b84b60f6e6c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609946"
---
# <span data-ttu-id="36ccb-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="36ccb-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="36ccb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="36ccb-103">Salva um modelo de implantação de grupo de recursos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="36ccb-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36ccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36ccb-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36ccb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="36ccb-106">O cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  salva um modelo de implantação de grupo de recursos em um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="36ccb-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="36ccb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="36ccb-108">Exemplo 1: salvar um modelo de implantação</span><span class="sxs-lookup"><span data-stu-id="36ccb-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="36ccb-109">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="36ccb-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="36ccb-110">OS</span><span class="sxs-lookup"><span data-stu-id="36ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="36ccb-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="36ccb-111">-ApiVersion</span></span>
<span data-ttu-id="36ccb-112">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="36ccb-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="36ccb-113">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="36ccb-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="36ccb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ccb-114">-DefaultProfile</span></span>
<span data-ttu-id="36ccb-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="36ccb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="36ccb-116">-DeploymentName</span></span>
<span data-ttu-id="36ccb-117">Especifica o nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="36ccb-117">Specifies the name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36ccb-118">-Force</span></span>
<span data-ttu-id="36ccb-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="36ccb-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36ccb-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="36ccb-120">-InformationAction</span></span>
<span data-ttu-id="36ccb-121">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="36ccb-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="36ccb-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36ccb-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36ccb-123">Contínuo</span><span class="sxs-lookup"><span data-stu-id="36ccb-123">Continue</span></span>
- <span data-ttu-id="36ccb-124">Ignorar</span><span class="sxs-lookup"><span data-stu-id="36ccb-124">Ignore</span></span>
- <span data-ttu-id="36ccb-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="36ccb-125">Inquire</span></span>
- <span data-ttu-id="36ccb-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="36ccb-126">SilentlyContinue</span></span>
- <span data-ttu-id="36ccb-127">Finaliza</span><span class="sxs-lookup"><span data-stu-id="36ccb-127">Stop</span></span>
- <span data-ttu-id="36ccb-128">Suspensão</span><span class="sxs-lookup"><span data-stu-id="36ccb-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="36ccb-129">-InformationVariable</span></span>
<span data-ttu-id="36ccb-130">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="36ccb-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="36ccb-131">-Path</span></span>
<span data-ttu-id="36ccb-132">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="36ccb-132">Specifies the output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="36ccb-133">-Pre</span></span>
<span data-ttu-id="36ccb-134">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="36ccb-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="36ccb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ccb-135">-ResourceGroupName</span></span>
<span data-ttu-id="36ccb-136">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36ccb-136">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36ccb-137">-Confirm</span></span>
<span data-ttu-id="36ccb-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ccb-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ccb-139">-WhatIf</span></span>
<span data-ttu-id="36ccb-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36ccb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ccb-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36ccb-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ccb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ccb-142">CommonParameters</span></span>
<span data-ttu-id="36ccb-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ccb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ccb-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ccb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ccb-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36ccb-145">INPUTS</span></span>

### <span data-ttu-id="36ccb-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="36ccb-146">None</span></span>
<span data-ttu-id="36ccb-147">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="36ccb-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36ccb-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36ccb-148">OUTPUTS</span></span>

### <span data-ttu-id="36ccb-149">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="36ccb-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="36ccb-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36ccb-150">NOTES</span></span>

## <span data-ttu-id="36ccb-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36ccb-151">RELATED LINKS</span></span>
