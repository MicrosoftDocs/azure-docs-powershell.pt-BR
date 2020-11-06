---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 3b83b18bf7a795dd8df3c93a7fd2f8b25974ce35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429133"
---
# <span data-ttu-id="66e83-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66e83-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="66e83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66e83-102">SYNOPSIS</span></span>
<span data-ttu-id="66e83-103">Captura um grupo de recursos como um modelo e salva-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="66e83-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66e83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66e83-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66e83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66e83-105">DESCRIPTION</span></span>
<span data-ttu-id="66e83-106">O cmdlet **Export-AzureRmResourceGroup** captura o grupo de recursos especificado como um modelo e salva-o em um arquivo JSON. Isso pode ser útil em cenários em que você já criou alguns recursos em seu grupo de recursos e, em seguida, deseja aproveitar as vantagens do uso de implantações com backup em modelos.</span><span class="sxs-lookup"><span data-stu-id="66e83-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="66e83-107">Esse cmdlet oferece um início fácil, gerando o modelo para seus recursos existentes no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66e83-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="66e83-108">Pode haver alguns casos em que esse cmdlet falha ao gerar algumas partes do modelo.</span><span class="sxs-lookup"><span data-stu-id="66e83-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="66e83-109">As mensagens de aviso informarão sobre os recursos que falharam.</span><span class="sxs-lookup"><span data-stu-id="66e83-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="66e83-110">O modelo ainda será gerado para as partes que foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="66e83-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="66e83-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66e83-111">EXAMPLES</span></span>

### <span data-ttu-id="66e83-112">Exemplo 1: exportar um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="66e83-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="66e83-113">Esse comando captura o grupo de recursos chamado grupo de teste como modelo e salva-o em um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="66e83-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="66e83-114">OS</span><span class="sxs-lookup"><span data-stu-id="66e83-114">PARAMETERS</span></span>

### <span data-ttu-id="66e83-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66e83-115">-ApiVersion</span></span>
<span data-ttu-id="66e83-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="66e83-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="66e83-117">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="66e83-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="66e83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="66e83-118">-Force</span></span>
<span data-ttu-id="66e83-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="66e83-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66e83-120">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="66e83-120">-IncludeComments</span></span>
<span data-ttu-id="66e83-121">Indica que essa operação exporta o modelo com comentários.</span><span class="sxs-lookup"><span data-stu-id="66e83-121">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="66e83-122">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="66e83-122">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="66e83-123">Indica que essa operação exporta o parâmetro do modelo com o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="66e83-123">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="66e83-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="66e83-124">-InformationAction</span></span>
<span data-ttu-id="66e83-125">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="66e83-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="66e83-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="66e83-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66e83-127">Contínuo</span><span class="sxs-lookup"><span data-stu-id="66e83-127">Continue</span></span>
- <span data-ttu-id="66e83-128">Ignorar</span><span class="sxs-lookup"><span data-stu-id="66e83-128">Ignore</span></span>
- <span data-ttu-id="66e83-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="66e83-129">Inquire</span></span>
- <span data-ttu-id="66e83-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="66e83-130">SilentlyContinue</span></span>
- <span data-ttu-id="66e83-131">Finaliza</span><span class="sxs-lookup"><span data-stu-id="66e83-131">Stop</span></span>
- <span data-ttu-id="66e83-132">Suspensão</span><span class="sxs-lookup"><span data-stu-id="66e83-132">Suspend</span></span>

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

### <span data-ttu-id="66e83-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="66e83-133">-InformationVariable</span></span>
<span data-ttu-id="66e83-134">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="66e83-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="66e83-135">-Caminho</span><span class="sxs-lookup"><span data-stu-id="66e83-135">-Path</span></span>
<span data-ttu-id="66e83-136">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="66e83-136">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="66e83-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="66e83-137">-Pre</span></span>
<span data-ttu-id="66e83-138">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="66e83-138">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="66e83-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e83-139">-ResourceGroupName</span></span>
<span data-ttu-id="66e83-140">Especifica o nome do grupo de recursos a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="66e83-140">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="66e83-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66e83-141">-Confirm</span></span>
<span data-ttu-id="66e83-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66e83-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e83-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e83-143">-WhatIf</span></span>
<span data-ttu-id="66e83-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66e83-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e83-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66e83-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e83-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e83-146">-DefaultProfile</span></span>
<span data-ttu-id="66e83-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66e83-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66e83-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e83-148">CommonParameters</span></span>
<span data-ttu-id="66e83-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e83-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e83-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66e83-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e83-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66e83-151">INPUTS</span></span>

## <span data-ttu-id="66e83-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66e83-152">OUTPUTS</span></span>

### <span data-ttu-id="66e83-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="66e83-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66e83-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66e83-154">NOTES</span></span>

## <span data-ttu-id="66e83-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66e83-155">RELATED LINKS</span></span>

[<span data-ttu-id="66e83-156">Localizar-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66e83-156">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)


