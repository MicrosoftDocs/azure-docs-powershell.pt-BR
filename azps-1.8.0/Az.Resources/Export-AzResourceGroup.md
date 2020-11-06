---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93611168"
---
# <span data-ttu-id="046ae-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="046ae-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="046ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="046ae-102">SYNOPSIS</span></span>
<span data-ttu-id="046ae-103">Captura um grupo de recursos como um modelo e salva-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="046ae-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="046ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="046ae-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="046ae-105">DESCRIPTION</span></span>
<span data-ttu-id="046ae-106">O cmdlet **Export-AzResourceGroup** captura o grupo de recursos especificado como um modelo e salva-o em um arquivo JSON. Isso pode ser útil em cenários em que você já criou alguns recursos em seu grupo de recursos e, em seguida, deseja aproveitar as vantagens do uso de implantações com backup em modelos.</span><span class="sxs-lookup"><span data-stu-id="046ae-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="046ae-107">Esse cmdlet oferece um início fácil, gerando o modelo para seus recursos existentes no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="046ae-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="046ae-108">Pode haver alguns casos em que esse cmdlet falha ao gerar algumas partes do modelo.</span><span class="sxs-lookup"><span data-stu-id="046ae-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="046ae-109">As mensagens de aviso informarão sobre os recursos que falharam.</span><span class="sxs-lookup"><span data-stu-id="046ae-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="046ae-110">O modelo ainda será gerado para as partes que foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="046ae-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="046ae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="046ae-111">EXAMPLES</span></span>

### <span data-ttu-id="046ae-112">Exemplo 1: exportar um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="046ae-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="046ae-113">Esse comando captura o grupo de recursos chamado grupo de teste como modelo e salva-o em um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="046ae-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="046ae-114">OS</span><span class="sxs-lookup"><span data-stu-id="046ae-114">PARAMETERS</span></span>

### <span data-ttu-id="046ae-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="046ae-115">-ApiVersion</span></span>
<span data-ttu-id="046ae-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="046ae-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="046ae-117">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="046ae-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="046ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046ae-118">-DefaultProfile</span></span>
<span data-ttu-id="046ae-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="046ae-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="046ae-120">-Force</span><span class="sxs-lookup"><span data-stu-id="046ae-120">-Force</span></span>
<span data-ttu-id="046ae-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="046ae-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="046ae-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="046ae-122">-IncludeComments</span></span>
<span data-ttu-id="046ae-123">Indica que essa operação exporta o modelo com comentários.</span><span class="sxs-lookup"><span data-stu-id="046ae-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="046ae-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="046ae-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="046ae-125">Indica que essa operação exporta o parâmetro do modelo com o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="046ae-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="046ae-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="046ae-126">-Path</span></span>
<span data-ttu-id="046ae-127">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="046ae-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="046ae-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="046ae-128">-Pre</span></span>
<span data-ttu-id="046ae-129">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="046ae-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="046ae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046ae-130">-ResourceGroupName</span></span>
<span data-ttu-id="046ae-131">Especifica o nome do grupo de recursos a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="046ae-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="046ae-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="046ae-132">-Confirm</span></span>
<span data-ttu-id="046ae-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="046ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046ae-134">-WhatIf</span></span>
<span data-ttu-id="046ae-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="046ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046ae-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="046ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046ae-137">CommonParameters</span></span>
<span data-ttu-id="046ae-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046ae-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046ae-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046ae-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="046ae-140">INPUTS</span></span>

### <span data-ttu-id="046ae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="046ae-141">System.String</span></span>

## <span data-ttu-id="046ae-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="046ae-142">OUTPUTS</span></span>

### <span data-ttu-id="046ae-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="046ae-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="046ae-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="046ae-144">NOTES</span></span>

## <span data-ttu-id="046ae-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="046ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="046ae-146">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="046ae-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


