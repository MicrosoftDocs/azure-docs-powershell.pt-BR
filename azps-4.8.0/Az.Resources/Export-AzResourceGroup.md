---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948058"
---
# <span data-ttu-id="528f1-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="528f1-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="528f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="528f1-102">SYNOPSIS</span></span>
<span data-ttu-id="528f1-103">Captura um grupo de recursos como um modelo e salva-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="528f1-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="528f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="528f1-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="528f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="528f1-105">DESCRIPTION</span></span>
<span data-ttu-id="528f1-106">O cmdlet **Export-AzResourceGroup** captura o grupo de recursos especificado como um modelo e salva-o em um arquivo JSON. Isso pode ser útil em cenários em que você já criou alguns recursos em seu grupo de recursos e, em seguida, deseja aproveitar as vantagens do uso de implantações com backup em modelos.</span><span class="sxs-lookup"><span data-stu-id="528f1-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="528f1-107">Esse cmdlet oferece um início fácil, gerando o modelo para seus recursos existentes no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="528f1-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="528f1-108">Pode haver alguns casos em que esse cmdlet falha ao gerar algumas partes do modelo.</span><span class="sxs-lookup"><span data-stu-id="528f1-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="528f1-109">As mensagens de aviso informarão sobre os recursos que falharam.</span><span class="sxs-lookup"><span data-stu-id="528f1-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="528f1-110">O modelo ainda será gerado para as partes que foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="528f1-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="528f1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="528f1-111">EXAMPLES</span></span>

### <span data-ttu-id="528f1-112">Exemplo 1: exportar um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="528f1-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="528f1-113">Esse comando captura o grupo de recursos chamado grupo de teste como modelo e salva-o em um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="528f1-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="528f1-114">Exemplo 2: exportar um único recurso de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="528f1-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="528f1-115">Esse comando captura o recurso de máquina virtual chamado "TestVirtualMachine" do grupo de recursos "grupo de teste" como modelo e salva-o em um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="528f1-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="528f1-116">Exemplo 3: exportar uma seleção de recursos de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="528f1-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="528f1-117">Esse comando captura dois recursos do grupo de recursos "grupo de teste" como um modelo e salva-os em um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="528f1-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="528f1-118">O modelo gerado não conterá nenhum parâmetro gerado.</span><span class="sxs-lookup"><span data-stu-id="528f1-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="528f1-119">OS</span><span class="sxs-lookup"><span data-stu-id="528f1-119">PARAMETERS</span></span>

### <span data-ttu-id="528f1-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="528f1-120">-ApiVersion</span></span>
<span data-ttu-id="528f1-121">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="528f1-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="528f1-122">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="528f1-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="528f1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528f1-123">-DefaultProfile</span></span>
<span data-ttu-id="528f1-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="528f1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="528f1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="528f1-125">-Force</span></span>
<span data-ttu-id="528f1-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="528f1-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="528f1-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="528f1-127">-IncludeComments</span></span>
<span data-ttu-id="528f1-128">Indica que essa operação exporta o modelo com comentários.</span><span class="sxs-lookup"><span data-stu-id="528f1-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="528f1-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="528f1-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="528f1-130">Indica que essa operação exporta o parâmetro do modelo com o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="528f1-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="528f1-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="528f1-131">-Path</span></span>
<span data-ttu-id="528f1-132">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="528f1-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="528f1-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="528f1-133">-Pre</span></span>
<span data-ttu-id="528f1-134">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="528f1-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="528f1-135">-Recurso</span><span class="sxs-lookup"><span data-stu-id="528f1-135">-Resource</span></span>
<span data-ttu-id="528f1-136">Uma lista de ResourceId para filtrar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="528f1-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="528f1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="528f1-137">-ResourceGroupName</span></span>
<span data-ttu-id="528f1-138">Especifica o nome do grupo de recursos a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="528f1-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="528f1-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="528f1-139">-SkipAllParameterization</span></span>
<span data-ttu-id="528f1-140">Ignorar toda a parametrização.</span><span class="sxs-lookup"><span data-stu-id="528f1-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="528f1-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="528f1-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="528f1-142">Pule a parametrização do nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="528f1-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="528f1-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="528f1-143">-Confirm</span></span>
<span data-ttu-id="528f1-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="528f1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="528f1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="528f1-145">-WhatIf</span></span>
<span data-ttu-id="528f1-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="528f1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="528f1-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="528f1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="528f1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528f1-148">CommonParameters</span></span>
<span data-ttu-id="528f1-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="528f1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528f1-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="528f1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528f1-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="528f1-151">INPUTS</span></span>

### <span data-ttu-id="528f1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="528f1-152">System.String</span></span>

## <span data-ttu-id="528f1-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="528f1-153">OUTPUTS</span></span>

### <span data-ttu-id="528f1-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="528f1-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="528f1-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="528f1-155">NOTES</span></span>

## <span data-ttu-id="528f1-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="528f1-156">RELATED LINKS</span></span>

[<span data-ttu-id="528f1-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="528f1-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


