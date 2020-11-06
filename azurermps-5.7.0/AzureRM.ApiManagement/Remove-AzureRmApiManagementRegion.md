---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441511"
---
# <span data-ttu-id="992af-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="992af-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="992af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="992af-102">SYNOPSIS</span></span>
<span data-ttu-id="992af-103">Remove uma região de implantação existente da instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="992af-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="992af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="992af-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="992af-105">DESCRIPTION</span></span>
<span data-ttu-id="992af-106">O cmdlet **Remove-AzureRmApiManagementRegion** remove a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** de uma coleção de **AdditionalRegions** da fornecida a instância do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="992af-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="992af-107">Esse cmdlet não modifica a implantação sozinha, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="992af-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="992af-108">Para atualizar uma implantação de um gerenciamento de API, passe a **PsApiManagementInstance** modificada para **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="992af-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="992af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="992af-109">EXAMPLES</span></span>

### <span data-ttu-id="992af-110">Exemplo 1: remover uma região de uma instância do PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="992af-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="992af-111">Esse comando Remove a região chamada leste US da instância **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="992af-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="992af-112">Exemplo 2: remover uma região de uma instância do PsApiManagement usando uma série de comandos</span><span class="sxs-lookup"><span data-stu-id="992af-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="992af-113">Esse primeiro comando obtém uma instância de **PsApiManagement** do grupo de recursos chamado contoso chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="992af-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="992af-114">Em seguida, o comando final remove a região chamada leste dos EUA dessa instância e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="992af-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="992af-115">OS</span><span class="sxs-lookup"><span data-stu-id="992af-115">PARAMETERS</span></span>

### <span data-ttu-id="992af-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="992af-116">-ApiManagement</span></span>
<span data-ttu-id="992af-117">Especifica a instância **PsApiManagement** para a qual esse cmdlet Remove a região de implantação adicional.</span><span class="sxs-lookup"><span data-stu-id="992af-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="992af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992af-118">-DefaultProfile</span></span>
<span data-ttu-id="992af-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="992af-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="992af-120">-Local</span><span class="sxs-lookup"><span data-stu-id="992af-120">-Location</span></span>
<span data-ttu-id="992af-121">Especifica o local da região que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="992af-121">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="992af-122">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="992af-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="992af-123">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="992af-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="992af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992af-124">CommonParameters</span></span>
<span data-ttu-id="992af-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992af-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992af-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="992af-127">INPUTS</span></span>

### <span data-ttu-id="992af-128">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="992af-128">PsApiManagement</span></span>
<span data-ttu-id="992af-129">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="992af-129">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="992af-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="992af-130">OUTPUTS</span></span>

### <span data-ttu-id="992af-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="992af-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="992af-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="992af-132">NOTES</span></span>

## <span data-ttu-id="992af-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="992af-133">RELATED LINKS</span></span>

[<span data-ttu-id="992af-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="992af-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="992af-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="992af-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

