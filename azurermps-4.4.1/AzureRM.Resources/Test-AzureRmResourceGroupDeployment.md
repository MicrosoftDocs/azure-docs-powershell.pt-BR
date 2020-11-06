---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430662"
---
# <span data-ttu-id="f9bcf-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9bcf-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f9bcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bcf-103">Valida uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9bcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9bcf-104">SYNTAX</span></span>

### <span data-ttu-id="f9bcf-105">Implantação via arquivo de modelo sem parâmetros (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9bcf-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-106">Implantação via arquivo de modelo e objeto de parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="f9bcf-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-107">Implantação via URI de modelo e objeto de parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="f9bcf-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-108">Implantação via arquivo de modelo e arquivo de parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="f9bcf-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-109">Implantação via URI de modelo e arquivo de parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="f9bcf-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-110">Implantação via URI dos parâmetros do modelo de arquivo de modelo</span><span class="sxs-lookup"><span data-stu-id="f9bcf-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-111">Implantação via URI de modelo e URI de parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="f9bcf-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bcf-112">Implantação via URI de modelo sem parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9bcf-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9bcf-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9bcf-113">DESCRIPTION</span></span>
<span data-ttu-id="f9bcf-114">O cmdlet **Test-AzureRmResourceGroupDeployment** determina se um modelo de implantação do grupo de recursos do Azure e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f9bcf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9bcf-115">EXAMPLES</span></span>

## <span data-ttu-id="f9bcf-116">OS</span><span class="sxs-lookup"><span data-stu-id="f9bcf-116">PARAMETERS</span></span>

### <span data-ttu-id="f9bcf-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f9bcf-117">-ApiVersion</span></span>
<span data-ttu-id="f9bcf-118">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f9bcf-119">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f9bcf-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="f9bcf-120">-Mode</span></span>
<span data-ttu-id="f9bcf-121">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="f9bcf-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f9bcf-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9bcf-123">Adicionais</span><span class="sxs-lookup"><span data-stu-id="f9bcf-123">Incremental</span></span>
- <span data-ttu-id="f9bcf-124">Assuma</span><span class="sxs-lookup"><span data-stu-id="f9bcf-124">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="f9bcf-125">-Pre</span></span>
<span data-ttu-id="f9bcf-126">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f9bcf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9bcf-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9bcf-128">Especifica o nome do grupo de recursos para testar.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-128">Specifies the name of the resource group to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f9bcf-129">-TemplateFile</span></span>
<span data-ttu-id="f9bcf-130">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f9bcf-131">-TemplateParameterFile</span></span>
<span data-ttu-id="f9bcf-132">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f9bcf-133">-TemplateParameterObject</span></span>
<span data-ttu-id="f9bcf-134">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f9bcf-135">-TemplateParameterUri</span></span>
<span data-ttu-id="f9bcf-136">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f9bcf-137">-TemplateUri</span></span>
<span data-ttu-id="f9bcf-138">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bcf-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9bcf-139">-DefaultProfile</span></span>
<span data-ttu-id="f9bcf-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9bcf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9bcf-141">CommonParameters</span></span>
<span data-ttu-id="f9bcf-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9bcf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9bcf-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9bcf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9bcf-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9bcf-144">INPUTS</span></span>

## <span data-ttu-id="f9bcf-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9bcf-145">OUTPUTS</span></span>

### <span data-ttu-id="f9bcf-146">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="f9bcf-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="f9bcf-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9bcf-147">NOTES</span></span>

## <span data-ttu-id="f9bcf-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9bcf-148">RELATED LINKS</span></span>

[<span data-ttu-id="f9bcf-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9bcf-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f9bcf-150">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9bcf-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f9bcf-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9bcf-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f9bcf-152">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9bcf-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


