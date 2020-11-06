---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428657"
---
# <span data-ttu-id="37ea3-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="37ea3-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="37ea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="37ea3-103">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="37ea3-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37ea3-104">SYNTAX</span></span>

### <span data-ttu-id="37ea3-105">GetAllBackends (padrão)</span><span class="sxs-lookup"><span data-stu-id="37ea3-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37ea3-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="37ea3-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37ea3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37ea3-107">DESCRIPTION</span></span>
<span data-ttu-id="37ea3-108">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="37ea3-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="37ea3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37ea3-109">EXAMPLES</span></span>

### <span data-ttu-id="37ea3-110">Exemplo 1: obter todos os backends</span><span class="sxs-lookup"><span data-stu-id="37ea3-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="37ea3-111">Obtém uma lista de todos os backends configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="37ea3-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="37ea3-112">Exemplo 2: obter o back-end especificado pelo identificador 123</span><span class="sxs-lookup"><span data-stu-id="37ea3-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="37ea3-113">Obter os detalhes do back-end especificado identificado pelo identificador ' 123 '</span><span class="sxs-lookup"><span data-stu-id="37ea3-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="37ea3-114">OS</span><span class="sxs-lookup"><span data-stu-id="37ea3-114">PARAMETERS</span></span>

### <span data-ttu-id="37ea3-115">-Backid</span><span class="sxs-lookup"><span data-stu-id="37ea3-115">-BackendId</span></span>
<span data-ttu-id="37ea3-116">Identificador de um back-end.</span><span class="sxs-lookup"><span data-stu-id="37ea3-116">Identifier of a backend.</span></span>
<span data-ttu-id="37ea3-117">Se especificado, tentará localizar o back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="37ea3-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="37ea3-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="37ea3-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ea3-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="37ea3-119">-Context</span></span>
<span data-ttu-id="37ea3-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="37ea3-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="37ea3-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="37ea3-121">This parameter is required.</span></span>

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

### <span data-ttu-id="37ea3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ea3-122">-DefaultProfile</span></span>
<span data-ttu-id="37ea3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37ea3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ea3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ea3-124">CommonParameters</span></span>
<span data-ttu-id="37ea3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ea3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ea3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ea3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ea3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37ea3-127">INPUTS</span></span>

### <span data-ttu-id="37ea3-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="37ea3-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37ea3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="37ea3-129">System.String</span></span>

## <span data-ttu-id="37ea3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37ea3-130">OUTPUTS</span></span>

### <span data-ttu-id="37ea3-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="37ea3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="37ea3-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37ea3-132">NOTES</span></span>

## <span data-ttu-id="37ea3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37ea3-133">RELATED LINKS</span></span>

[<span data-ttu-id="37ea3-134">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="37ea3-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="37ea3-135">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="37ea3-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="37ea3-136">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="37ea3-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="37ea3-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="37ea3-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="37ea3-138">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="37ea3-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
