---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117890"
---
# <span data-ttu-id="20e74-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20e74-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="20e74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20e74-102">SYNOPSIS</span></span>
<span data-ttu-id="20e74-103">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="20e74-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="20e74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20e74-104">SYNTAX</span></span>

### <span data-ttu-id="20e74-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="20e74-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20e74-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e74-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20e74-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20e74-107">DESCRIPTION</span></span>
<span data-ttu-id="20e74-108">Obtenha os detalhes do back-end.</span><span class="sxs-lookup"><span data-stu-id="20e74-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="20e74-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20e74-109">EXAMPLES</span></span>

### <span data-ttu-id="20e74-110">Exemplo 1: obter todos os backends</span><span class="sxs-lookup"><span data-stu-id="20e74-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="20e74-111">Obtém uma lista de todos os backends configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="20e74-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="20e74-112">Exemplo 2: obter o back-end especificado pelo identificador 123</span><span class="sxs-lookup"><span data-stu-id="20e74-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="20e74-113">Obter os detalhes do back-end especificado identificado pelo identificador ' 123 '</span><span class="sxs-lookup"><span data-stu-id="20e74-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="20e74-114">OS</span><span class="sxs-lookup"><span data-stu-id="20e74-114">PARAMETERS</span></span>

### <span data-ttu-id="20e74-115">-Backid</span><span class="sxs-lookup"><span data-stu-id="20e74-115">-BackendId</span></span>
<span data-ttu-id="20e74-116">Identificador de um back-end.</span><span class="sxs-lookup"><span data-stu-id="20e74-116">Identifier of a backend.</span></span>
<span data-ttu-id="20e74-117">Se especificado, tentará localizar o back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="20e74-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="20e74-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="20e74-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e74-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="20e74-119">-Context</span></span>
<span data-ttu-id="20e74-120">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="20e74-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20e74-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="20e74-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20e74-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e74-122">-DefaultProfile</span></span>
<span data-ttu-id="20e74-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20e74-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20e74-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20e74-124">-ResourceId</span></span>
<span data-ttu-id="20e74-125">Identificador de recursos ARM do back-end.</span><span class="sxs-lookup"><span data-stu-id="20e74-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="20e74-126">Se especificado, tentará localizar o back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="20e74-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="20e74-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="20e74-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e74-128">CommonParameters</span></span>
<span data-ttu-id="20e74-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e74-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20e74-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e74-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20e74-131">INPUTS</span></span>

### <span data-ttu-id="20e74-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20e74-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20e74-133">System. String</span><span class="sxs-lookup"><span data-stu-id="20e74-133">System.String</span></span>

## <span data-ttu-id="20e74-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20e74-134">OUTPUTS</span></span>

### <span data-ttu-id="20e74-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20e74-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="20e74-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20e74-136">NOTES</span></span>

## <span data-ttu-id="20e74-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20e74-137">RELATED LINKS</span></span>

[<span data-ttu-id="20e74-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20e74-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="20e74-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="20e74-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="20e74-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="20e74-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="20e74-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20e74-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="20e74-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="20e74-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
