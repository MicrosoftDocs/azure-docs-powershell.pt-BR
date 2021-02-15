---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118089"
---
# <span data-ttu-id="201c0-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="201c0-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="201c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="201c0-102">SYNOPSIS</span></span>
<span data-ttu-id="201c0-103">Obter os detalhes do Backend.</span><span class="sxs-lookup"><span data-stu-id="201c0-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="201c0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="201c0-104">SYNTAX</span></span>

### <span data-ttu-id="201c0-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="201c0-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="201c0-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="201c0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="201c0-107">DESCRIPTION</span></span>
<span data-ttu-id="201c0-108">Obter os detalhes do Backend.</span><span class="sxs-lookup"><span data-stu-id="201c0-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="201c0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="201c0-109">EXAMPLES</span></span>

### <span data-ttu-id="201c0-110">Exemplo 1: Obter todos os Backends</span><span class="sxs-lookup"><span data-stu-id="201c0-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="201c0-111">Obtém uma lista de todos os Backends configurados no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="201c0-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="201c0-112">Exemplo 2: Obter o Backend especificado pelo Identificador 123</span><span class="sxs-lookup"><span data-stu-id="201c0-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="201c0-113">Obter os detalhes do Backend especificado identificado pelo Identificador '123'</span><span class="sxs-lookup"><span data-stu-id="201c0-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="201c0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="201c0-114">PARAMETERS</span></span>

### <span data-ttu-id="201c0-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="201c0-115">-BackendId</span></span>
<span data-ttu-id="201c0-116">Identificador de um back-end.</span><span class="sxs-lookup"><span data-stu-id="201c0-116">Identifier of a backend.</span></span>
<span data-ttu-id="201c0-117">Se especificado, tentará encontrar back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="201c0-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="201c0-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="201c0-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="201c0-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="201c0-119">-Context</span></span>
<span data-ttu-id="201c0-120">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="201c0-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="201c0-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="201c0-121">This parameter is required.</span></span>

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

### <span data-ttu-id="201c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201c0-122">-DefaultProfile</span></span>
<span data-ttu-id="201c0-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="201c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="201c0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="201c0-124">-ResourceId</span></span>
<span data-ttu-id="201c0-125">Arm Resource Identifier do back-end.</span><span class="sxs-lookup"><span data-stu-id="201c0-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="201c0-126">Se especificado, tentará encontrar back-end pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="201c0-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="201c0-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="201c0-127">This parameter is required.</span></span>

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

### <span data-ttu-id="201c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201c0-128">CommonParameters</span></span>
<span data-ttu-id="201c0-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201c0-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="201c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201c0-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="201c0-131">INPUTS</span></span>

### <span data-ttu-id="201c0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="201c0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="201c0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="201c0-133">System.String</span></span>

## <span data-ttu-id="201c0-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="201c0-134">OUTPUTS</span></span>

### <span data-ttu-id="201c0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="201c0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="201c0-136">Notas</span><span class="sxs-lookup"><span data-stu-id="201c0-136">NOTES</span></span>

## <span data-ttu-id="201c0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="201c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="201c0-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="201c0-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="201c0-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="201c0-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="201c0-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="201c0-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="201c0-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="201c0-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="201c0-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="201c0-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
