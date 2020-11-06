---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433425"
---
# <span data-ttu-id="4fdca-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4fdca-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="4fdca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fdca-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdca-103">Valida uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fdca-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fdca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fdca-104">SYNTAX</span></span>

### <span data-ttu-id="4fdca-105">ByTemplateFileWithNoParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fdca-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4fdca-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4fdca-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4fdca-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4fdca-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4fdca-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4fdca-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdca-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4fdca-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fdca-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fdca-113">DESCRIPTION</span></span>
<span data-ttu-id="4fdca-114">O cmdlet **Test-AzureRmResourceGroupDeployment** determina se um modelo de implantação do grupo de recursos do Azure e seus valores de parâmetro são válidos.</span><span class="sxs-lookup"><span data-stu-id="4fdca-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4fdca-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fdca-115">EXAMPLES</span></span>

## <span data-ttu-id="4fdca-116">OS</span><span class="sxs-lookup"><span data-stu-id="4fdca-116">PARAMETERS</span></span>

### <span data-ttu-id="4fdca-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4fdca-117">-ApiVersion</span></span>
<span data-ttu-id="4fdca-118">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fdca-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4fdca-119">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="4fdca-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4fdca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdca-120">-DefaultProfile</span></span>
<span data-ttu-id="4fdca-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4fdca-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fdca-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="4fdca-122">-Mode</span></span>
<span data-ttu-id="4fdca-123">Especifica o modo de implantação.</span><span class="sxs-lookup"><span data-stu-id="4fdca-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="4fdca-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4fdca-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fdca-125">Adicionais</span><span class="sxs-lookup"><span data-stu-id="4fdca-125">Incremental</span></span>
- <span data-ttu-id="4fdca-126">Assuma</span><span class="sxs-lookup"><span data-stu-id="4fdca-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="4fdca-127">-Pre</span></span>
<span data-ttu-id="4fdca-128">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4fdca-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4fdca-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fdca-129">-ResourceGroupName</span></span>
<span data-ttu-id="4fdca-130">Especifica o nome do grupo de recursos para testar.</span><span class="sxs-lookup"><span data-stu-id="4fdca-130">Specifies the name of the resource group to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4fdca-131">-TemplateFile</span></span>
<span data-ttu-id="4fdca-132">Especifica o caminho completo de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="4fdca-132">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4fdca-133">-TemplateParameterFile</span></span>
<span data-ttu-id="4fdca-134">Especifica o caminho completo de um arquivo JSON que contém os nomes e os valores dos parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="4fdca-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4fdca-135">-TemplateParameterObject</span></span>
<span data-ttu-id="4fdca-136">Especifica uma tabela de hash de nomes e valores de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="4fdca-136">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4fdca-137">-TemplateParameterUri</span></span>
<span data-ttu-id="4fdca-138">Especifica o URI de um arquivo de parâmetros de modelo.</span><span class="sxs-lookup"><span data-stu-id="4fdca-138">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4fdca-139">-TemplateUri</span></span>
<span data-ttu-id="4fdca-140">Especifica o URI de um arquivo de modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="4fdca-140">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdca-141">CommonParameters</span></span>
<span data-ttu-id="4fdca-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdca-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fdca-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdca-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fdca-144">INPUTS</span></span>

### <span data-ttu-id="4fdca-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4fdca-145">None</span></span>
<span data-ttu-id="4fdca-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4fdca-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fdca-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fdca-147">OUTPUTS</span></span>

### <span data-ttu-id="4fdca-148">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="4fdca-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="4fdca-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fdca-149">NOTES</span></span>

## <span data-ttu-id="4fdca-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fdca-150">RELATED LINKS</span></span>

[<span data-ttu-id="4fdca-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4fdca-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="4fdca-152">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4fdca-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="4fdca-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4fdca-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="4fdca-154">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4fdca-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


