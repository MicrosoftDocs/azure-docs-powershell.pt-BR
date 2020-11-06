---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427021"
---
# <span data-ttu-id="6d44a-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="6d44a-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="6d44a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d44a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d44a-103">Remove uma região de implantação existente da instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6d44a-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d44a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d44a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d44a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d44a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d44a-106">O cmdlet **Remove-AzureRmApiManagementRegion** remove a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** de uma coleção de **AdditionalRegions** da fornecida a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="6d44a-107">Esse cmdlet não modifica a implantação sozinha, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="6d44a-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="6d44a-108">Para atualizar uma implantação de um gerenciamento de API, passe a **PsApiManagementInstance** modificada para **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="6d44a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d44a-109">EXAMPLES</span></span>

### <span data-ttu-id="6d44a-110">Exemplo 1: remover uma região de uma instância do PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d44a-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="6d44a-111">Esse comando Remove a região chamada leste US da instância **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="6d44a-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="6d44a-112">Exemplo 2: remover uma região de uma instância do PsApiManagement usando uma série de comandos</span><span class="sxs-lookup"><span data-stu-id="6d44a-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="6d44a-113">Esse primeiro comando obtém uma instância de **PsApiManagement** do grupo de recursos chamado contoso chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="6d44a-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="6d44a-114">Em seguida, o comando final remove a região chamada leste dos EUA dessa instância e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="6d44a-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="6d44a-115">OS</span><span class="sxs-lookup"><span data-stu-id="6d44a-115">PARAMETERS</span></span>

### <span data-ttu-id="6d44a-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d44a-116">-ApiManagement</span></span>
<span data-ttu-id="6d44a-117">Especifica a instância **PsApiManagement** para a qual esse cmdlet Remove a região de implantação adicional.</span><span class="sxs-lookup"><span data-stu-id="6d44a-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d44a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="6d44a-118">-Location</span></span>
<span data-ttu-id="6d44a-119">Especifica o local da região que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6d44a-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="6d44a-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6d44a-120">Valid values are:</span></span> 

- <span data-ttu-id="6d44a-121">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="6d44a-121">North Central US</span></span>
- <span data-ttu-id="6d44a-122">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="6d44a-122">South Central US</span></span>
- <span data-ttu-id="6d44a-123">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="6d44a-123">Central US</span></span>
- <span data-ttu-id="6d44a-124">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="6d44a-124">West Europe</span></span>
- <span data-ttu-id="6d44a-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="6d44a-125">North Europe</span></span>
- <span data-ttu-id="6d44a-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="6d44a-126">West US</span></span>
- <span data-ttu-id="6d44a-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="6d44a-127">East US</span></span>
- <span data-ttu-id="6d44a-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="6d44a-128">East US 2</span></span>
- <span data-ttu-id="6d44a-129">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="6d44a-129">Japan East</span></span>
- <span data-ttu-id="6d44a-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="6d44a-130">Japan West</span></span>
- <span data-ttu-id="6d44a-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="6d44a-131">Brazil South</span></span>
- <span data-ttu-id="6d44a-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="6d44a-132">Southeast Asia</span></span>
- <span data-ttu-id="6d44a-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="6d44a-133">East Asia</span></span>
- <span data-ttu-id="6d44a-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="6d44a-134">Australia East</span></span>
- <span data-ttu-id="6d44a-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="6d44a-135">Australia Southeast</span></span>

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

### <span data-ttu-id="6d44a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d44a-136">-DefaultProfile</span></span>
<span data-ttu-id="6d44a-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d44a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d44a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d44a-138">CommonParameters</span></span>
<span data-ttu-id="6d44a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d44a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d44a-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d44a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d44a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d44a-141">INPUTS</span></span>

### <span data-ttu-id="6d44a-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d44a-142">PsApiManagement</span></span>
<span data-ttu-id="6d44a-143">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6d44a-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="6d44a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d44a-144">OUTPUTS</span></span>

### <span data-ttu-id="6d44a-145">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d44a-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="6d44a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d44a-146">NOTES</span></span>

## <span data-ttu-id="6d44a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d44a-147">RELATED LINKS</span></span>

[<span data-ttu-id="6d44a-148">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="6d44a-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="6d44a-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="6d44a-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


