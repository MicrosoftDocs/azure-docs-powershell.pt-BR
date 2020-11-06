---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431844"
---
# <span data-ttu-id="80f0a-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80f0a-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="80f0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="80f0a-103">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="80f0a-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80f0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80f0a-104">SYNTAX</span></span>

### <span data-ttu-id="80f0a-105">Obter todos os backends (padrão)</span><span class="sxs-lookup"><span data-stu-id="80f0a-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80f0a-106">Obter por ID de back-end</span><span class="sxs-lookup"><span data-stu-id="80f0a-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f0a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80f0a-107">DESCRIPTION</span></span>
<span data-ttu-id="80f0a-108">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="80f0a-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="80f0a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80f0a-109">EXAMPLES</span></span>

### <span data-ttu-id="80f0a-110">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80f0a-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="80f0a-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="80f0a-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="80f0a-112">Obtém uma lista de todos os backends configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="80f0a-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="80f0a-113">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="80f0a-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="80f0a-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="80f0a-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="80f0a-115">Obter os detalhes do back-end especificado identificado pelo identificador ' 123 '</span><span class="sxs-lookup"><span data-stu-id="80f0a-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="80f0a-116">OS</span><span class="sxs-lookup"><span data-stu-id="80f0a-116">PARAMETERS</span></span>

### <span data-ttu-id="80f0a-117">-Backid</span><span class="sxs-lookup"><span data-stu-id="80f0a-117">-BackendId</span></span>
<span data-ttu-id="80f0a-118">Identificador de um back-end.</span><span class="sxs-lookup"><span data-stu-id="80f0a-118">Identifier of a backend.</span></span>
<span data-ttu-id="80f0a-119">Se especificado, tentará localizar o back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="80f0a-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="80f0a-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="80f0a-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f0a-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="80f0a-121">-Context</span></span>
<span data-ttu-id="80f0a-122">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="80f0a-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="80f0a-123">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="80f0a-123">This parameter is required.</span></span>

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

### <span data-ttu-id="80f0a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f0a-124">-DefaultProfile</span></span>
<span data-ttu-id="80f0a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80f0a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f0a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f0a-126">CommonParameters</span></span>
<span data-ttu-id="80f0a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f0a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f0a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f0a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f0a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80f0a-129">INPUTS</span></span>

## <span data-ttu-id="80f0a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80f0a-130">OUTPUTS</span></span>

### <span data-ttu-id="80f0a-131">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="80f0a-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="80f0a-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80f0a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="80f0a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80f0a-133">NOTES</span></span>

## <span data-ttu-id="80f0a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80f0a-134">RELATED LINKS</span></span>

[<span data-ttu-id="80f0a-135">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80f0a-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="80f0a-136">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="80f0a-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="80f0a-137">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="80f0a-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="80f0a-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80f0a-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="80f0a-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80f0a-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
