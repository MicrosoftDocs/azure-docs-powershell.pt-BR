---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432988"
---
# <span data-ttu-id="631a7-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="631a7-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="631a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="631a7-102">SYNOPSIS</span></span>
<span data-ttu-id="631a7-103">Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="631a7-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="631a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="631a7-104">SYNTAX</span></span>

### <span data-ttu-id="631a7-105">GetAllApiOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="631a7-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="631a7-106">GetById</span><span class="sxs-lookup"><span data-stu-id="631a7-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="631a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="631a7-107">DESCRIPTION</span></span>
<span data-ttu-id="631a7-108">**Get-AzureRmApiManagementOperation** Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="631a7-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="631a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="631a7-109">EXAMPLES</span></span>

### <span data-ttu-id="631a7-110">Exemplo 1: obter todas as operações de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="631a7-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="631a7-111">Esse comando obtém todas as operações de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="631a7-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="631a7-112">Exemplo 2: obter uma operação de gerenciamento de API por ID da operação</span><span class="sxs-lookup"><span data-stu-id="631a7-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="631a7-113">Esse comando obtém uma operação de gerenciamento de API por ID de operação chamada Operation0003.</span><span class="sxs-lookup"><span data-stu-id="631a7-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="631a7-114">OS</span><span class="sxs-lookup"><span data-stu-id="631a7-114">PARAMETERS</span></span>

### <span data-ttu-id="631a7-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="631a7-115">-ApiId</span></span>
<span data-ttu-id="631a7-116">Especifica o identificador da operação de API.</span><span class="sxs-lookup"><span data-stu-id="631a7-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="631a7-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="631a7-117">-Context</span></span>
<span data-ttu-id="631a7-118">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="631a7-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="631a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631a7-119">-DefaultProfile</span></span>
<span data-ttu-id="631a7-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="631a7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="631a7-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="631a7-121">-OperationId</span></span>
<span data-ttu-id="631a7-122">Especifica o identificador da operação.</span><span class="sxs-lookup"><span data-stu-id="631a7-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="631a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631a7-123">CommonParameters</span></span>
<span data-ttu-id="631a7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631a7-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="631a7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631a7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="631a7-126">INPUTS</span></span>

### <span data-ttu-id="631a7-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="631a7-127">None</span></span>
<span data-ttu-id="631a7-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="631a7-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="631a7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="631a7-129">OUTPUTS</span></span>

### <span data-ttu-id="631a7-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="631a7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="631a7-131">Os detalhes da operação da API no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="631a7-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="631a7-132">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="631a7-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="631a7-133">A lista de operações de API no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="631a7-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="631a7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="631a7-134">NOTES</span></span>

## <span data-ttu-id="631a7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="631a7-135">RELATED LINKS</span></span>

[<span data-ttu-id="631a7-136">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="631a7-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="631a7-137">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="631a7-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="631a7-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="631a7-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


