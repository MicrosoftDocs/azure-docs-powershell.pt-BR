---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431255"
---
# <span data-ttu-id="5f366-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5f366-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="5f366-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f366-102">SYNOPSIS</span></span>
<span data-ttu-id="5f366-103">Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="5f366-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f366-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f366-104">SYNTAX</span></span>

### <span data-ttu-id="5f366-105">Todas as operações de API (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f366-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f366-106">Localizar por ID</span><span class="sxs-lookup"><span data-stu-id="5f366-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f366-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f366-107">DESCRIPTION</span></span>
<span data-ttu-id="5f366-108">**Get-AzureRmApiManagementOperation** Obtém uma lista ou uma operação de API especificada.</span><span class="sxs-lookup"><span data-stu-id="5f366-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="5f366-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f366-109">EXAMPLES</span></span>

### <span data-ttu-id="5f366-110">Exemplo 1: obter todas as operações de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="5f366-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="5f366-111">Esse comando obtém todas as operações de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5f366-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="5f366-112">Exemplo 2: obter uma operação de gerenciamento de API por ID da operação</span><span class="sxs-lookup"><span data-stu-id="5f366-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="5f366-113">Esse comando obtém uma operação de gerenciamento de API por ID de operação chamada Operation0003.</span><span class="sxs-lookup"><span data-stu-id="5f366-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="5f366-114">OS</span><span class="sxs-lookup"><span data-stu-id="5f366-114">PARAMETERS</span></span>

### <span data-ttu-id="5f366-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5f366-115">-ApiId</span></span>
<span data-ttu-id="5f366-116">Especifica o identificador da operação de API.</span><span class="sxs-lookup"><span data-stu-id="5f366-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="5f366-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5f366-117">-Context</span></span>
<span data-ttu-id="5f366-118">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5f366-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f366-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5f366-119">-OperationId</span></span>
<span data-ttu-id="5f366-120">Especifica o identificador da operação.</span><span class="sxs-lookup"><span data-stu-id="5f366-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f366-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f366-121">-DefaultProfile</span></span>
<span data-ttu-id="5f366-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f366-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f366-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f366-123">CommonParameters</span></span>
<span data-ttu-id="5f366-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f366-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f366-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f366-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f366-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f366-126">INPUTS</span></span>

## <span data-ttu-id="5f366-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f366-127">OUTPUTS</span></span>

### <span data-ttu-id="5f366-128">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="5f366-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="5f366-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f366-129">NOTES</span></span>

## <span data-ttu-id="5f366-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f366-130">RELATED LINKS</span></span>

[<span data-ttu-id="5f366-131">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5f366-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5f366-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5f366-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5f366-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5f366-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


