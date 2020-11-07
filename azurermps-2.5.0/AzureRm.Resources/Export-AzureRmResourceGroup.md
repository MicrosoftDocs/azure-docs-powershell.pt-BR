---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: a5390cd66e97f05e80f52685af6e43135ed64141
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785633"
---
# <span data-ttu-id="a84fa-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a84fa-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="a84fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a84fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a84fa-103">Captura um grupo de recursos como um modelo e salva-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a84fa-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a84fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a84fa-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a84fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a84fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a84fa-106">O cmdlet **Export-AzureRmResourceGroup** captura o grupo de recursos especificado como um modelo e salva-o em um arquivo JSON. Isso pode ser útil em cenários em que você já criou alguns recursos em seu grupo de recursos e, em seguida, deseja aproveitar as vantagens do uso de implantações com backup em modelos.</span><span class="sxs-lookup"><span data-stu-id="a84fa-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="a84fa-107">Esse cmdlet oferece um início fácil, gerando o modelo para seus recursos existentes no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a84fa-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="a84fa-108">Pode haver alguns casos em que esse cmdlet falha ao gerar algumas partes do modelo.</span><span class="sxs-lookup"><span data-stu-id="a84fa-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="a84fa-109">As mensagens de aviso informarão sobre os recursos que falharam.</span><span class="sxs-lookup"><span data-stu-id="a84fa-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="a84fa-110">O modelo ainda será gerado para as partes que foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="a84fa-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="a84fa-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a84fa-111">EXAMPLES</span></span>

### <span data-ttu-id="a84fa-112">Exemplo 1: exportar um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a84fa-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="a84fa-113">Esse comando captura o grupo de recursos chamado grupo de teste como modelo e salva-o em um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="a84fa-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="a84fa-114">OS</span><span class="sxs-lookup"><span data-stu-id="a84fa-114">PARAMETERS</span></span>

### <span data-ttu-id="a84fa-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a84fa-115">-ApiVersion</span></span>
<span data-ttu-id="a84fa-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a84fa-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a84fa-117">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="a84fa-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="a84fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84fa-118">-DefaultProfile</span></span>
<span data-ttu-id="a84fa-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a84fa-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a84fa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a84fa-120">-Force</span></span>
<span data-ttu-id="a84fa-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a84fa-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a84fa-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="a84fa-122">-IncludeComments</span></span>
<span data-ttu-id="a84fa-123">Indica que essa operação exporta o modelo com comentários.</span><span class="sxs-lookup"><span data-stu-id="a84fa-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="a84fa-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a84fa-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="a84fa-125">Indica que essa operação exporta o parâmetro do modelo com o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="a84fa-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="a84fa-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a84fa-126">-InformationAction</span></span>
<span data-ttu-id="a84fa-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a84fa-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a84fa-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a84fa-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a84fa-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a84fa-129">Continue</span></span>
- <span data-ttu-id="a84fa-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a84fa-130">Ignore</span></span>
- <span data-ttu-id="a84fa-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="a84fa-131">Inquire</span></span>
- <span data-ttu-id="a84fa-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a84fa-132">SilentlyContinue</span></span>
- <span data-ttu-id="a84fa-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a84fa-133">Stop</span></span>
- <span data-ttu-id="a84fa-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a84fa-134">Suspend</span></span>

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

### <span data-ttu-id="a84fa-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a84fa-135">-InformationVariable</span></span>
<span data-ttu-id="a84fa-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a84fa-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a84fa-137">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a84fa-137">-Path</span></span>
<span data-ttu-id="a84fa-138">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="a84fa-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="a84fa-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="a84fa-139">-Pre</span></span>
<span data-ttu-id="a84fa-140">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="a84fa-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="a84fa-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84fa-141">-ResourceGroupName</span></span>
<span data-ttu-id="a84fa-142">Especifica o nome do grupo de recursos a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="a84fa-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="a84fa-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a84fa-143">-Confirm</span></span>
<span data-ttu-id="a84fa-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a84fa-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a84fa-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a84fa-145">-WhatIf</span></span>
<span data-ttu-id="a84fa-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a84fa-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a84fa-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a84fa-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a84fa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84fa-148">CommonParameters</span></span>
<span data-ttu-id="a84fa-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84fa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84fa-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84fa-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84fa-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a84fa-151">INPUTS</span></span>

## <span data-ttu-id="a84fa-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a84fa-152">OUTPUTS</span></span>

## <span data-ttu-id="a84fa-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a84fa-153">NOTES</span></span>

## <span data-ttu-id="a84fa-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a84fa-154">RELATED LINKS</span></span>




