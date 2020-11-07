---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772532"
---
# <span data-ttu-id="abfa2-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="abfa2-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="abfa2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abfa2-102">SYNOPSIS</span></span>
<span data-ttu-id="abfa2-103">Salva um modelo de implantação de grupo de recursos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="abfa2-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="abfa2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abfa2-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abfa2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abfa2-105">DESCRIPTION</span></span>
<span data-ttu-id="abfa2-106">O cmdlet **Save-AzResourceGroupDeploymentTemplate**  salva um modelo de implantação de grupo de recursos em um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="abfa2-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="abfa2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abfa2-107">EXAMPLES</span></span>

### <span data-ttu-id="abfa2-108">Exemplo 1: salvar um modelo de implantação</span><span class="sxs-lookup"><span data-stu-id="abfa2-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="abfa2-109">Esse comando obtém o modelo de implantação do TestDeployment e o salva como um arquivo JSON no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="abfa2-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="abfa2-110">OS</span><span class="sxs-lookup"><span data-stu-id="abfa2-110">PARAMETERS</span></span>

### <span data-ttu-id="abfa2-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="abfa2-111">-ApiVersion</span></span>
<span data-ttu-id="abfa2-112">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="abfa2-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="abfa2-113">Se não for especificado, a versão mais recente da API será usada.</span><span class="sxs-lookup"><span data-stu-id="abfa2-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="abfa2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abfa2-114">-DefaultProfile</span></span>
<span data-ttu-id="abfa2-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="abfa2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abfa2-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="abfa2-116">-DeploymentName</span></span>
<span data-ttu-id="abfa2-117">Especifica o nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="abfa2-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="abfa2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="abfa2-118">-Force</span></span>
<span data-ttu-id="abfa2-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="abfa2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abfa2-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="abfa2-120">-Path</span></span>
<span data-ttu-id="abfa2-121">Especifica o caminho de saída do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="abfa2-121">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="abfa2-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="abfa2-122">-Pre</span></span>
<span data-ttu-id="abfa2-123">Indica que esse cmdlet usa versões de API de pré-lançamento ao determinar automaticamente qual versão de API usar.</span><span class="sxs-lookup"><span data-stu-id="abfa2-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="abfa2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abfa2-124">-ResourceGroupName</span></span>
<span data-ttu-id="abfa2-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="abfa2-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="abfa2-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abfa2-126">-Confirm</span></span>
<span data-ttu-id="abfa2-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abfa2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abfa2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abfa2-128">-WhatIf</span></span>
<span data-ttu-id="abfa2-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abfa2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abfa2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abfa2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abfa2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abfa2-131">CommonParameters</span></span>
<span data-ttu-id="abfa2-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abfa2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abfa2-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abfa2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abfa2-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abfa2-134">INPUTS</span></span>

### <span data-ttu-id="abfa2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="abfa2-135">System.String</span></span>

## <span data-ttu-id="abfa2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abfa2-136">OUTPUTS</span></span>

### <span data-ttu-id="abfa2-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="abfa2-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="abfa2-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abfa2-138">NOTES</span></span>

## <span data-ttu-id="abfa2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abfa2-139">RELATED LINKS</span></span>