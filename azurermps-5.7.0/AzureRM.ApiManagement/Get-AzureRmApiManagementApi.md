---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 435e167b713934962daf0cf27fc0d844caee8dcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427719"
---
# <span data-ttu-id="4f913-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="4f913-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f913-102">SYNOPSIS</span></span>
<span data-ttu-id="4f913-103">Obtém uma API.</span><span class="sxs-lookup"><span data-stu-id="4f913-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f913-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f913-104">SYNTAX</span></span>

### <span data-ttu-id="4f913-105">GetAllApis (padrão)</span><span class="sxs-lookup"><span data-stu-id="4f913-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f913-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="4f913-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f913-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="4f913-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f913-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="4f913-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f913-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f913-109">DESCRIPTION</span></span>
<span data-ttu-id="4f913-110">O cmdlet **Get-AzureRmApiManagementApi** Obtém uma ou mais APIs de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f913-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="4f913-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f913-111">EXAMPLES</span></span>

### <span data-ttu-id="4f913-112">Exemplo 1: obter todas as APIs de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4f913-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="4f913-113">Esse comando obtém todas as APIs do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="4f913-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="4f913-114">Exemplo 2: obter uma API de gerenciamento por ID</span><span class="sxs-lookup"><span data-stu-id="4f913-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="4f913-115">Este comando obtém a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="4f913-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="4f913-116">Exemplo 3: obter uma API de gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="4f913-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="4f913-117">Este comando obtém a API com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="4f913-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="4f913-118">OS</span><span class="sxs-lookup"><span data-stu-id="4f913-118">PARAMETERS</span></span>

### <span data-ttu-id="4f913-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4f913-119">-ApiId</span></span>
<span data-ttu-id="4f913-120">Especifica a ID da API a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="4f913-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByApiId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f913-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4f913-121">-Context</span></span>
<span data-ttu-id="4f913-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4f913-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f913-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f913-123">-DefaultProfile</span></span>
<span data-ttu-id="4f913-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f913-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4f913-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f913-125">-Name</span></span>
<span data-ttu-id="4f913-126">Especifica o nome da API a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="4f913-126">Specifies the name of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f913-127">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4f913-127">-ProductId</span></span>
<span data-ttu-id="4f913-128">Especifica a ID do produto para o qual obter a API.</span><span class="sxs-lookup"><span data-stu-id="4f913-128">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f913-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f913-129">CommonParameters</span></span>
<span data-ttu-id="4f913-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f913-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f913-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f913-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f913-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f913-132">INPUTS</span></span>

### <span data-ttu-id="4f913-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f913-133">None</span></span>
<span data-ttu-id="4f913-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4f913-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f913-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f913-135">OUTPUTS</span></span>

### <span data-ttu-id="4f913-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="4f913-137">Os detalhes da API em um determinado serviço do ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f913-137">The details of the Api in a given ApiManagement service</span></span>

### <span data-ttu-id="4f913-138">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="4f913-138">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>
<span data-ttu-id="4f913-139">A lista de APIs em um determinado serviço do ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4f913-139">The list of Apis in a given ApiManagement service</span></span>

## <span data-ttu-id="4f913-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f913-140">NOTES</span></span>

## <span data-ttu-id="4f913-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f913-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f913-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="4f913-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="4f913-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="4f913-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="4f913-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4f913-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


