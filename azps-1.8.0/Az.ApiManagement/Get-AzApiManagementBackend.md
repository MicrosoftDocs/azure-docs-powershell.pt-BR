---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 88a48edf3ae7e576aa78e989a5fda7515499a7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595687"
---
# <span data-ttu-id="7fd77-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fd77-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="7fd77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fd77-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd77-103">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="7fd77-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="7fd77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fd77-104">SYNTAX</span></span>

### <span data-ttu-id="7fd77-105">GetAllBackends (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fd77-105">GetAllBackends (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd77-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="7fd77-106">GetByBackendId</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd77-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fd77-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd77-108">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="7fd77-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="7fd77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fd77-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd77-110">Exemplo 1: obter todos os backends</span><span class="sxs-lookup"><span data-stu-id="7fd77-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="7fd77-111">Obtém uma lista de todos os backends configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="7fd77-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="7fd77-112">Exemplo 2: obter o back-end especificado pelo identificador 123</span><span class="sxs-lookup"><span data-stu-id="7fd77-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="7fd77-113">Obter os detalhes do back-end especificado identificado pelo identificador ' 123 '</span><span class="sxs-lookup"><span data-stu-id="7fd77-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="7fd77-114">OS</span><span class="sxs-lookup"><span data-stu-id="7fd77-114">PARAMETERS</span></span>

### <span data-ttu-id="7fd77-115">-Backid</span><span class="sxs-lookup"><span data-stu-id="7fd77-115">-BackendId</span></span>
<span data-ttu-id="7fd77-116">Identificador de um back-end.</span><span class="sxs-lookup"><span data-stu-id="7fd77-116">Identifier of a backend.</span></span>
<span data-ttu-id="7fd77-117">Se especificado, tentará localizar o back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="7fd77-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="7fd77-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fd77-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7fd77-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7fd77-119">-Context</span></span>
<span data-ttu-id="7fd77-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7fd77-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7fd77-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7fd77-121">This parameter is required.</span></span>

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

### <span data-ttu-id="7fd77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd77-122">-DefaultProfile</span></span>
<span data-ttu-id="7fd77-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd77-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd77-124">CommonParameters</span></span>
<span data-ttu-id="7fd77-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd77-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd77-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd77-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd77-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fd77-127">INPUTS</span></span>

### <span data-ttu-id="7fd77-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7fd77-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7fd77-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7fd77-129">System.String</span></span>

## <span data-ttu-id="7fd77-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fd77-130">OUTPUTS</span></span>

### <span data-ttu-id="7fd77-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fd77-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="7fd77-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fd77-132">NOTES</span></span>

## <span data-ttu-id="7fd77-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fd77-133">RELATED LINKS</span></span>

[<span data-ttu-id="7fd77-134">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fd77-134">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="7fd77-135">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7fd77-135">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="7fd77-136">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7fd77-136">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="7fd77-137">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fd77-137">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="7fd77-138">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7fd77-138">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
